category_id = models.AutoField(primary_key=True)
category_name = models.CharField(max_length=512)
category_description = models.CharField(max_length=1024)

INCOME = 'I'
EXPENSE = 'E'
CATEGORY_TYPE_CHOICES = [(INCOME, 'Income'), (EXPENSE, 'Expense'), ]

category_type = models.CharField(max_length=1, choices=CATEGORY_TYPE_CHOICES)
category_group = models.CharField(max_length=512)



<template>
  <div id="app">
  </div>

  <div class="home">
    <h1 class="title">VBS (Vazarkar Budget System)</h1>

    <hr>
    <div class="columns">
      <div class="column is-3 is-offset-3">
        <form>
          <h2 class="subtitle">Add category</h2>

          <div class="field">
            <label class="label">Name</label>
            <div class="control">
              <input class="input" type="text">
            </div>
          </div>
          <div class="field">
            <label class="label">Description</label>
            <div class="control">
              <input class="input" type="text">
            </div>
          </div>
          <div class="field">
            <label class="label">Type</label>
            <div class="control">
              <div class="select">
                <select>
                  <option value="Income">Income</option>
                  <option value="Expense">Expense</option>
                </select>
              </div>
            </div>
          </div>
          <div class="field">
            <label class="label">Group</label>
            <div class="control">
              <input class="input" type="text">
            </div>
          </div>
          <div class="field">
            <div class="control">
              <button class="button is-link">Submit</button>
            </div>
          </div>
        </form>
      </div>
    </div>
    <div class="columns">
      <div class="column is-6">
        <h2 class="subtitle"></h2>
      </div>
    </div>
  </div>
</template>
