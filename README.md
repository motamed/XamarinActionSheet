# How display Action Sheet in Xamarin.Forms

``` cs
 DisplayActionSheet("Title","Cancel","Destruction","Button1","Button2","Button3",...);
```

### The DisplayAlert method can also be used to capture a user's response by presenting two buttons and returning a boolean. To get a response from an alert, supply text for both buttons and await the method. After the user selects one of the options the answer will be returned to your code. Note the async and await keywords in the sample code below:

``` cs
        private async void displayActionSheetBtn_Clicked(object sender, EventArgs e)
        {
            var actionSheet = await DisplayActionSheet("Title","Cancel", null, "Button1","Button2","Button3");

            switch (actionSheet)
            {
                case "Cancel":
                
                    // Do Something when 'Cancel' Button is pressed
                
                    break;

                case "Button1":

                    // Do Something when 'Button1' Button is pressed

                    break;

                case "Button2":

                    // Do Something when 'Button2' Button is pressed

                    break;
                case "Button3":

                    // Do Something when 'Button3' Button is pressed

                    break;

            }
            
        }

```
<img src="actionsheet.png"/>


<br/>
<br/>
<br/>

>### The destroy button is rendered differently than the others, and can be left null or specified as the third string parameter. The following example uses the destroy button:

``` cs

 var actionSheet = await DisplayActionSheet("Title","Cancel","Destruction","Button1","Button2","Button3");

            switch (actionSheet)
            {
                case "Cancel":
                
                    // Do Something when 'Cancel' Button is pressed
                
                    break;

                case "Destruction":

                    // Do Something when 'Destruction' Button is pressed

                                        .
                                        .
                                        .                    

```

<img src="actionsheet2.png"/>