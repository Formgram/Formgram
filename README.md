# Formgram
Use this set of web services to create forms and form fields in a free database then display the form and save information typed into those fields back into the free database.

    int multipageFormGroupInstanceId = [self AddFormInstance:18 myUsername:@"guest"];

    NSString *urlWithFormIds = [NSString stringWithFormat:@"http://formgram5.azurewebsites.net/m/openform.aspx?multipage_form_id=%d&navigation=0&multipage_form_group_instance_id=%d&username=guest", 18, multipageFormGroupInstanceId];

    NSURL *url = [NSURL URLWithString:urlWithFormIds];

    NSURLRequest *urlRequest = [NSURLRequest requestWithURL:url];

    [self.formgramWebView loadRequest:urlRequest];

The number 18 is the identifier for an example appointment form.

<h1>Select the form you want to use</h1>
Change this number to any other identifier to show a different form.

You can see the list of all the currently available forms at http://formgram5.azurewebsites.net/m/Forms.aspx?formListEnum=1&username=guest

Once you find the form you'd like to use, get the multipage_form_id of that form from the URL that shows up on your browser. For example, multipage_form_id of this example Appointment form at
http://formgram5.azurewebsites.net/m/OpenForm.aspx?multipage_form_id=18&username=guest
is 18.

Update that multipage_form_id in this Formgram Example XCode then build and run.

You'll see an example appointment form show up and your users will be able to fill out this sample form.

To see what your user has filled out in this form, go to the URL that's composed in XCode in the NSString urlWithFormIds.

Alternatively, you can use any computer/mobile device to go to http://formgram5.azurewebsites.net/m/report.aspx?form_version_id=66&username=guest
to see all the entries that users entered into this form.

In the next release, you'll be able to create your own forms and other apps/people can use your new forms too.

In the meantime, fell free to email me at henry@formgram.com with an example of a form you'd like created and I'll create it for you to use.
