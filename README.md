# NPM - Package
## A simple age calculator

```javascript
    let dob = new Date(getDate);
    let birthDate = dob.getDate();
    let birthMonth = dob.getMonth() + 1;
    let birthYear = dob.getFullYear();

    let today = new Date();
    let todayDate = today.getDate();
    let todayMonth = today.getMonth() + 1;
    let todayYear = today.getFullYear();

    let ageDate, ageMonth, ageYear;

    ageYear = todayYear - birthYear;

    if(todayMonth >= birthMonth) {
        ageMonth = todayMonth - birthMonth;
    } else {
        ageYear--;
        ageMonth = 12 + todayMonth - birthMonth;
    }

    if(todayDate >= birthDate) {
        ageDate = todayDate - birthDate;
    } else {
        ageMonth--;
        ageDate = this.getDaysInMonth(birthYear, birthMonth) + todayDate - birthDate;
    }

    if(ageMonth < 0) {
        ageMonth = 11;
        ageYear--;
    }

    return `${ageYear} Years, ${ageMonth} Months, ${ageDate} Days`;
```

## Install

```javascript
    npm i arindam-age-calculator
```

## Example

```javascript
    const arindamAgeCalculator = require('arindam-age-calculator');
    console.log("Age is = ", arindamAgeCalculator.calculateAge('1987/01/14'));
```

### Thanks!