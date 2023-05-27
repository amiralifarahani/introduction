# introduction
mobile HW1
The part where the welcome message appears on the screen:

Toast toast = Toast.makeText(getApplicationContext(), "Welcome Message", Toast.LENGTH_LONG);
toast.setGravity(Gravity.CENTER_HORIZONTAL | Gravity.BOTTOM, 0, 0);
toast.show();

The part where code handels the Gmail app(or any default at for sending email) calling.

Button mailButton = findViewById(R.id.mail_button);
mailButton.setOnClickListener(v -> {
            Intent intent = new Intent(Intent.ACTION_VIEW);
            startActivity(intent);
        });

The part where code handels the mobile app calling.

Button phoneButton = findViewById(R.id.phone_button);
        phoneButton.setOnClickListener(v -> {
            Intent intent = new Intent(Intent.ACTION_DIAL);
            intent.setData(Uri.parse("tel:1234567890"));
            startActivity(intent);
        });
 
The part where the app theme switches from dark mode to light mode.

Switch themeSwitch = findViewById(R.id.theme_switch);
        themeSwitch.setOnCheckedChangeListener((buttonView, isChecked) -> {
            if (isChecked) {
                // Set dark theme
                AppCompatDelegate.setDefaultNightMode(AppCompatDelegate.MODE_NIGHT_YES);
            } else {
                // Set light theme
                AppCompatDelegate.setDefaultNightMode(AppCompatDelegate.MODE_NIGHT_NO);
            }
        });
