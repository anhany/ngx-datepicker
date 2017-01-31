# ct-ngx-datepticker

## Introduction

A single and dual date picker, written for angular 2+ projects.

## Code Samples

Usage Example 
```
<ct-date-picker [(date)]="date1" zIndex="100" formControlName="singlePicker">
    <input #date class="form-control" />
</ct-date-picker>
```
```
<ct-dual-picker [(dateFrom)]="date2" [(dateTo)]="date3" zIndex="100" formControlName="dualPicker">
    <input #dateFrom class="form-control" />
    <input #dateTo class="form-control" />
 </ct-dual-picker>
```

## Installation

```
npm install --save ct-ng2-datepicker    
```

## Usage
### Single datepicker
```
<ct-date-picker [(date)]="date1" zIndex="100" formControlName="singlePicker">
    <input #date class="form-control" />
</ct-date-picker>
```
Wrap a input field in the <ct-date-picker> element. Mark the input field with #date

#### Single datepicker parameters
 * date - date model
 * dateChanged - Event emitter for notification of date changes
 * zIndex - Allows specification of a custom z-index for the picker.
 * minDate - Minimum allowed date.
 * maxDate - Maximum allowed date.

### Dual Date Picker
```
<ct-dual-picker [(dateFrom)]="date2" [(dateTo)]="date3" zIndex="100" formControlName="dualPicker">
    <input #dateFrom class="form-control" />
    <input #dateTo class="form-control" />
 </ct-dual-picker>
```
Wrap two input fields in the <ct-dual-picker> element. Mark each input #dateFrom and #dateTo respectively.

#### Dual datepicker parameters
 * dateFrom - date model
 * dateTo - date model
 * dateChanged - Event emitter for notification of date changes
 * zIndex - Allows specification of a custom z-index for the picker.
 * minDate - Minimum allowed date.
 * maxDate - Maximum allowed date.


## Requirements
- Angular 2+ (common, core, forms)
- jQuery 3+ (see note below)
- moment 2

### Why jQuery?
I have already implemented the datepicker using the renderer class to support Angular Universal Apps, and avoid needing jQuery. However at this time renderer is experimental. When it is no longer experimental the code will be updated.

### Why moment?
Because the datepicker returns a moment date, not a string.



## Release Notes
 - 2.1.0 -- Added ability to validate dates on range, and moment.isValid
 - 2.0.0 -- Removed unused api parameters. Added basic validation for reactive forms.
 - 1.0.2 -- Notice about new repo. 
 - 1.0.1 -- Unspecified bug fixes (sorry, just starting to do this right)
 - 1.0.0 -- Initial Release

 ## Migration Notes
 * From 1.x to 2.x
 ..* Remove references to ctDisabled and inputClass from the datepickers. Instead apply those directly to the transcluded input.