
# Rapport

**Skriv din rapport här!**

I screens har jag skapat en second acitivity för att skicka information mellan det olika aktiviteterna. 
med intent får man detta att fungera, i intent finns olika sätt att skicka information, jag har använt mig av bundles och extras. Informationen/texten jag skickar
är Louise, detta kommer att sparas även när jag stänger ned. 


** kod ** 

Button och findViewbyId har en sån här kod, sen en till med close iställer för start. denna starta och stänger second activity.
intent.putExtras talar om vad som ska skrivas ifall name hittas. 
```
     Button button = findViewById(R.id.start_second_activity);
        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MainActivity.this, SecondActivity.class);
                intent.putExtra("name", "Louise");
                startActivity(intent);

            }
        });
    }
       
```
   I denna koden talar jag om att i typen Textview med varibeln textview ska vi finna id name.
    denna kommer med extras.getString att ge oss de namnet vi skrivit.
    public void onClick... finish(); talar om att nu är det klart. 
```
        TextView textView = findViewById(R.id.name);

        Bundle extras = getIntent().getExtras();
        if (extras!= null) {
            String name = extras.getString("name");
            int number =extras.getInt("number");
            textView.setText(name + "," + number );
        }
        Button close = findViewById(R.id.close_second_activity);
        close.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                finish();
            }
        });
```

Bilder läggs i samma mapp som markdown-filen.

![](android.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
