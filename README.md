-# This is a basic workflow to help you get started with Actions

name: CI

# Controls when the workflow will run
on:
  # Triggers the workflow on push or pull request events but only for the "main" branch
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v3

      # Runs a single command using the runners shell
      - name: Run a one-line script
        run: echo Hello, world!

      # Runs a set of commands using the runners shell
      - name: Run a multi-line script
        run: |
          echo Add other actions to build,
          echo test, and deploy your project.
👋 Hi, I’m @franklinquinones
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
franklinquinones/franklinquinones is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";
var options = new RequestOptions
{
  ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF"
};
var service = new ChargeService();
Charge charge = service.Get(
  "ch_3LiLgOEevvHdcOhJ0D72VAZy",
  options
);
var options = new RequestOptions
{
  StripeAccount = "acct_1LiL8VEevvHdcOhJ"
};
var service = new ChargeService();
Charge charge = service.Get(
  "ch_3LiLgOEevvHdcOhJ0D72VAZy",
  options
);
try {
  // Use Stripe's library to make request
} catch (StripeException e) {
  switch (e.StripeError.Type)
  {
    case "card_error":
      Console.WriteLine("Code: " + e.StripeError.Code);
      Console.WriteLine("Message: " + e.StripeError.Message);
      break;
    case "api_connection_error":
      break;
    case "api_error":
      break;
    case "authentication_error":
      break;
    case "invalid_request_error":
      break;
    case "rate_limit_error":
      break;
    case "validation_error":
      break;
    default:
      // Unknown Error Type
      break;
  }
}
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

var options = new ChargeCreateOptions
{
  Amount = 2000,
  Currency = "usd",
  Source = "tok_amex", // obtained with Stripe.js
  Description = "My First Test Charge (created for API docs at https://www.stripe.com/docs/api)",
};
var service = new ChargeService();
service.Create(options, new RequestOptions
{
  IdempotencyKey = "7Q4EmQr5EIvbvaOA",
});
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

var options = new ChargeCreateOptions()
{
    Amount = 2000,
    Currency = "usd",
    Source = "tok_amex",
    Metadata = new Dictionary<string, string>
    {
        { "OrderId", "6735" },
    }
};

var service = new ChargeService();
Charge charge = service.Create(options);
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

var service = new CustomerService();
var options = new CustomerListOptions {
  Limit = 3
};

// Synchronously paginate
foreach (var customer in service.ListAutoPaging(options)) {
  // Do something with customer
}

// Asynchronously paginate
await foreach (var customer in service.ListAutoPagingAsync(options)) {
  // Do something with customer
}
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

Customer customer = new CustomerService().Create(null);
Console.WriteLine(customer.RequestId);
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";
// Since C# is strongly typed,
// the version is fixed in the library.
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

var service = new BalanceService();
Balance balance = service.Get();
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

var service = new BalanceService();
Balance balance = service.Get();
StripeConfiguration.ApiKey = "sk_test_51LiL8VEevvHdcOhJjDqgee5P7M8wexGR1q3ODX5chqe96TBWc9jpuVCbSksdGlvJFVohsNX8FAvXoMtCZlnA15Aq00kPbCQ6GF";

var options = new PayoutCreateOptions
{
  Amount = 408,
  Currency = "usd",
};
var service = new PayoutService();
service.Create(options);
