# Outwards legitimacy application for REI3
This [REI3](https://rei.de) application consists of a very simple and useful feature for those scenarios in which there is call a third party API. In this case, the API could need to check the call legitimacy prior to execution. That is, the call to the outer API originated from a user within REI3 needs to attach a token that could be validate from the API against REI3 in order to proccess legitimately the call.

The next diagram tries to show a typical use case:

![imagen](https://github.com/fmvalsera/rei3_outwards_legitimacy_app/assets/71846781/0acc5f0b-92af-42d7-b291-ac367190ad46)

Basically these are the steps followed:

1. A user working on a REI3 application launch a function that calls a Third Party API attaching a issued token by the "Outwards legitimacy" application.
2. Before executing the call, the Third Party API checks the provided token asking back REI3 about its legitimacy.
3. If the token exists in REI3 the Third Party API will go on with the call execution, otherwise an error will be returned.
