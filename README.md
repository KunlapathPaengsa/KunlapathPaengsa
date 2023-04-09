### Hi there 👋

<!--**KunlapathPaengsa/KunlapathPaengsa** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->


### GitHub Languages
![KunlapathPaengsa's Streak](https://github-readme-stats.vercel.app/api/top-langs/?username=KunlapathPaengsa&theme=tokyonight&show_icons=true&hide_border=false&layout=compact)

### GitHub Stats
![KunlapathPaengsa's Streak](https://github-readme-stats.vercel.app/api?username=KunlapathPaengsa&theme=tokyonight&show_icons=true&hide_border=false&count_private=true)


![KunlapathPaengsa's Streak](https://github-readme-streak-stats.herokuapp.com/?user=KunlapathPaengsa&theme=tokyonight&hide_border=false)

## Example Code ##
```csharp
    public static void FindStep(int input, int currentIndex, int[] currectClimb, int[] vals)
    {
        if (input < 0)
            return;

        if (input == 0)
        {
            _ = vals.Append(currentIndex);
            int last = 0;
            for (int i = currentIndex - 1; i >= 0; i--)
            {
                int current = currectClimb[i];
                int res = current - last;
                last = current;
                Console.Write($"{res}{(i > input ? "," : "")} ");
            }
            Console.WriteLine();
            return;
        }

        currectClimb[currentIndex] = input;
        FindStep(input - 1, currentIndex + 1, currectClimb, vals);
        FindStep(input - 2, currentIndex + 1, currectClimb, vals);
    }
    
```

## Example API ##
```csharp
            app.MapGet("/hello", () => new { Message = "Hello World" });//Json
            app.MapGet("/user", async (IMediator mediator, [AsParameters] GetUserQuery request) => Results.Ok(await mediator.Send(request)));
```
