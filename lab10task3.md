```mermaid
flowchart TD
    Start([Start]) --> Input[/Receive num1, num2/]
    Input --> CheckType{Are both inputs int or float?}
    CheckType -- No --> RaiseError[/Raise ValueError: \"Both inputs must be numbers\"/]
    CheckType -- Yes --> Add[Add num1 + num2]
    Add --> ReturnSum["Return sum"]
    RaiseError --> End([End])
    ReturnSum --> End
