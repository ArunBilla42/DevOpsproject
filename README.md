<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>School Application Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f7fb;
      margin: 0;
      padding: 0;
    }

    .container {
      max-width: 800px;
      margin: 30px auto;
      background: #ffffff;
      padding: 20px 30px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      border-radius: 8px;
    }

    h1 {
      text-align: center;
      margin-bottom: 10px;
    }

    p.subtitle {
      text-align: center;
      margin-top: 0;
      font-size: 14px;
      color: #555;
    }

    fieldset {
      border: 1px solid #ddd;
      border-radius: 6px;
      margin-bottom: 15px;
      padding: 15px 20px;
    }

    legend {
      font-weight: bold;
      padding: 0 5px;
    }

    .form-row {
      display: flex;
      flex-wrap: wrap;
      margin-bottom: 10px;
    }

    .form-group {
      flex: 1;
      min-width: 220px;
      margin-right: 10px;
      margin-bottom: 10px;
    }

    .form-group:last-child {
      margin-right: 0;
    }

    label {
      display: block;
      font-size: 14px;
      margin-bottom: 4px;
    }

    input[type="text"],
    input[type="date"],
    input[type="email"],
    input[type="tel"],
    select,
    textarea {
      width: 100%;
      padding: 7px 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 14px;
      box-sizing: border-box;
    }

    textarea {
      resize: vertical;
      min-height: 70px;
    }

    .radio-group {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-top: 4px;
      flex-wrap: wrap;
    }

    .buttons {
      text-align: center;
      margin-top: 15px;
    }

    button {
      padding: 8px 18px;
      font-size: 14px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      margin: 0 5px;
    }

    button[type="submit"] {
      background-color: #007bff;
      color: #fff;
    }

    button[type="reset"] {
      background-color: #e0e0e0;
    }

    @media (max-width: 600px) {
      .form-group {
        min-width: 100%;
        margin-right: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>School Application Form</h1>
    <p class="subtitle">Please fill in all required (*) fields</p>

    <form action="#" method="post">
      <!-- Student Details -->
      <fieldset>
        <legend>Student Details</legend>

        <div class="form-row">
          <div class="form-group">
            <label for="firstName">First Name *</label>
            <input type="text" id="firstName" name="firstName" required />
          </div>
          <div class="form-group">
            <label for="lastName">Last Name *</label>
            <input type="text" id="lastName" name="lastName" required />
          </div>
        </div>

        <div class="form-row">
          <div class="form-group">
            <label for="dob">Date of Birth *</label>
            <input type="date" id="dob" name="dob" required />
          </div>
          <div class="form-group">
            <label>Gender *</label>
            <div class="radio-group">
              <label><input type="radio" name="gender" value="Male" required /> Male</label>
              <label><input type="radio" name="gender" value="Female" /> Female</label>
              <label><input type="radio" name="gender" value="Other" /> Other</label>
            </div>
          </div>
        </div>

        <div class="form-row">
          <div class="form-group">
            <label for="classApply">Class Applying For *</label>
            <select id="classApply" name="classApply" required>
              <option value="">-- Select Class --</option>
              <option value="LKG">LKG</option>
              <option value="UKG">UKG</option>
              <option value="1">Class 1</option>
              <option value="2">Class 2</option>
              <option value="3">Class 3</option>
              <option value="4">Class 4</option>
              <option value="5">Class 5</option>
              <option value="6">Class 6</option>
              <option value="7">Class 7</option>
              <option value="8">Class 8</option>
              <option value="9">Class 9</option>
              <option value="10">Class 10</option>
              <option value="11">Class 11</option>
              <option value="12">Class 12</option>
            </select>
          </div>

          <div class="form-group">
            <label for="prevSchool">Previous School (if any)</label>
            <input type="text" id="prevSchool" name="prevSchool" />
          </div>
        </div>
      </fieldset>

      <!-- Contact Details -->
      <fieldset>
        <legend>Contact Details</legend>

        <div class="form-group">
          <label for="address">Residential Address *</label>
          <textarea id="address" name="address" required></textarea>
        </div>

        <div class="form-row">
          <div class="form-group">
            <label for="city">City *</label>
            <input type="text" id="city" name="city" required />
          </div>
          <div class="form-group">
            <label for="state">State *</label>
            <input type="text" id="state" name="state" required />
          </div>
          <div class="form-group">
            <label for="pincode">Pincode *</label>
            <input type="text" id="pincode" name="pincode" required />
          </div>
        </div>
      </fieldset>

      <!-- Parent / Guardian Details -->
      <fieldset>
        <legend>Parent / Guardian Details</legend>

        <div class="form-row">
          <div class="form-group">
            <label for="fatherName">Father's Name *</label>
            <input type="text" id="fatherName" name="fatherName" required />
          </div>
          <div class="form-group">
            <label for="motherName">Mother's Name *</label>
            <input type="text" id="motherName" name="motherName" required />
          </div>
        </div>

        <div class="form-row">
          <div class="form-group">
            <label for="guardianPhone">Contact Number *</label>
            <input
              type="tel"
              id="guardianPhone"
              name="guardianPhone"
              pattern="[0-9]{10}"
              placeholder="10-digit number"
              required
            />
          </div>
          <div class="form-group">
            <label for="guardianEmail">Email ID</label>
            <input type="email" id="guardianEmail" name="guardianEmail" />
          </div>
        </div>

        <div class="form-group">
          <label for="occupation">Parent / Guardian Occupation</label>
          <input type="text" id="occupation" name="occupation" />
        </div>
      </fieldset>

      <!-- Other Information -->
      <fieldset>
        <legend>Other Information</legend>

        <div class="form-group">
          <label for="languages">Languages Known (Student)</label>
          <input
            type="text"
            id="languages"
            name="languages"
            placeholder="e.g., English, Telugu, Hindi"
          />
        </div>

        <div class="form-group">
          <label for="remarks">Any Medical Conditions / Remarks</label>
          <textarea
            id="remarks"
            name="remarks"
            placeholder="Mention allergies, medical conditions, or any special needs."
          ></textarea>
        </div>
      </fieldset>

      <!-- Declaration -->
      <fieldset>
        <legend>Declaration</legend>
        <p style="font-size: 14px;">
          I hereby declare that the information provided above is true and correct to the best of my
          knowledge. I understand that any false information may lead to cancellation of admission.
        </p>
        <div class="radio-group">
          <label>
            <input type="checkbox" name="declaration" required />
            I agree to the above declaration. *
          </label>
        </div>
      </fieldset>

      <div class="buttons">
        <button type="submit">Submit Application</button>
        <button type="reset">Reset Form</button>
      </div>
    </form>
  </div>
</body>
</html>
