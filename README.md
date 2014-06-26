job app

#user
email
password

#job
title
company
category
url
salary_bottom
salary_top

#job_application
job
user
status: default => "applied"

#company
name
size
industry
has_many :jobs



users add jobs
jobs have fields-categories (bizdev, sales, marketing, dev, devops, etc)
jobs are then surfaced by field (jobs.where :category => /cat/)

we also give advice on how to jobsearch
user can track number of jobs submitted
user can track which companies they applied to
user submits app
company gets +1 app (join table: job-application)
user gets +1 app (job-application)

can give live feed of companies
all applications are surfaced by user (/kam/ just applied to /Heroku/!)

can set goal of companies or applications/day
feature: /tracking?/ or /goal?/
when activate feature, adds db query for applications where submitted_at is on DATE

can seemost popular companies
company with most applications: query Job.where(:company => /company/)

users can get offers
can mark application status; status options include: 'applied', 'phone screened', 'interviewed', 'offered', 'accepted', 'rejected'

Companies can see which users have many offers; companies can see which users have applied to many companies; companies can be suggested to users

users can indicate interest in companies
join table :user_interest

companies can create pages
companies can upload logo, description

companies can upload jobs
jobs create a new page
jobs have title, description, salary, contact_info

users can filter offers
filter job_applications by company, salary, company size, location, and application status
