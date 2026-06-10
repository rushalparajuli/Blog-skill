Msty Claw 0.9.0: What This Release Is Really About


We built Msty Claw for people who want an AI assistant that can work with real files, real chats, and real tasks without getting in the way. It is a local-first desktop app meant to help people get useful work done faster, while keeping control close to the user.

Version 0.8.0 helped lay the groundwork for that direction. It strengthened the core experience and set the stage for the bigger changes that arrived in 0.9.0.

With 0.9.0, we focused on three things that matter in daily use: clearer insight, stronger automation, and better local document handling. If you are new to Msty Claw, this release is a good snapshot of what the app is becoming.
It is more useful for people already working in the app, and easier to understand for people who are just getting started.

Better visibility into usage

One of the biggest additions in 0.9.0 is the new usage stats board.

It gives you a clear view of how the app is being used over time. You can see:


- total token usage
- input and output token counts
- tool usage
- failed tool calls
- daily activity trends

You can also filter the data by provider or model and group it in different ways. That makes it easier to see which model is used most, where token usage comes from, and how activity changes over time.

The heatmap view is useful because it turns a long history into something you can scan quickly. Instead of reading through a raw list, you can spot patterns at a glance.

Folder changes can now drive work

0.9.0 also adds folder change triggers for tasks and playbooks.

This means a task or playbook can run when files in a chosen folder change. It is a useful step beyond scheduled runs because it lets Msty Claw react to work as it happens.

You can choose:


- the folder to watch
- which file types should count
- which change types should trigger a run
- how long the app should wait before firing
- how much quiet time should pass before another run

In practice, that makes the app better for document workflows, note cleanup, file-based review loops, and other repeated jobs where new or edited files should kick off action automatically.

This feature is careful about noise too. Common system and build folders are ignored, so the app stays focused on real work instead of background clutter.

Local files are easier to work with

Another important addition in 0.9.0 is the local document parsing tool.

This gives Msty Claw a direct way to read files from your local workspace and turn them into something the assistant can work with. It can extract text, return structured output, and save page screenshots when needed.

It is especially useful for:


- PDFs
- scanned documents
- files that need OCR
- document review tasks
- turning local content into something the assistant can summarize or inspect

That matters because it keeps the workflow local and practical. Instead of moving between tools or copying content by hand, you can point the app at a document and let it do the reading. For people working with reports, notes, forms, or reference material, that saves time and reduces friction.

More polish across the app

0.9.0 is not only about the headline features. It also tightens a lot of everyday behavior.

The update includes better app update controls, clearer sign-in and sync progress, improved sidebar keyboard navigation, and a cleaner setup and settings experience. It also improves PDF handling, including OCR cleanup and orientation support, so document work is more reliable.

A number of bugs were fixed too:


- refresh behavior is clearer
- folder selection works better
- scheduled tasks are more stable
- the rules view is cleaner
- usage stats now read more clearly on smaller screens

These changes may not be the biggest headline features, but they improve how the app behaves in actual use and make the whole experience feel more finished.

Why 0.9.0 matters

Msty Claw 0.9.0 pushes the app in a more complete direction.

It gives users better visibility into what the app is doing, gives tasks and playbooks a smarter trigger model, and makes local document work much more useful. At the same time, it smooths out a lot of the rough edges that get in the way of daily use.

If you already use Msty Claw, this release gives you more control and better feedback. If you are new to it, 0.9.0 shows what the app is for: a local-first assistant that can work with your files, your workflows, and your tools without getting in the way.

Update to 0.9.0 and try the new usage stats board, folder triggers, and local document parsing for yourself.
