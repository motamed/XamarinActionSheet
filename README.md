# How display Action Sheet in Xamarin.Forms

``` cs
 DisplayActionSheet("Title","Cancel","Destruction","Button1","Button2","Button3",...);
```

### The UIActionSheet is a common UI element in iOS. The Xamarin.Forms DisplayActionSheet method lets you include this control in cross-platforms apps, rendering native alternatives in Android and Windows Phone.

>To display an action sheet, await DisplayActionSheet in any Page, passing the message and button labels as strings. The method returns the string label of the button that was clicked by the user. A simple example is shown here:

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


<br/>
<br/>
<br/>

## Complete Code

`MainPage.xaml`
```html

<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:DisplayActionSheet"
             x:Class="DisplayActionSheet.MainPage">


    <StackLayout VerticalOptions="Center">
        <Button Text="Display Action Sheet" x:Name="displayActionSheetBtn" Clicked="displayActionSheetBtn_Clicked"></Button>
    </StackLayout>

</ContentPage>

```

<br/>
<br/>

`MainPage.xaml.cs`

``` cs

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Xamarin.Forms;

namespace DisplayActionSheet
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
        }

        private async void displayActionSheetBtn_Clicked(object sender, EventArgs e)
        {
            var actionSheet = await DisplayActionSheet("Title","Cancel","Destruction","Button1","Button2","Button3");

            switch (actionSheet)
            {
                case "Cancel":
                
                    // Do Something when 'Cancel' Button is pressed
                
                    break;

                case "Destruction":

                    // Do Something when 'Destruction' Button is pressed

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
    }
}


```
