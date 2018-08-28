- Start Date: 2018-05-16
- RFC PR: (leave this empty)
- ReactiveUI Issue: (leave this empty)

# Minimum supported version of Xamarin Forms

## Summary

As part of `v8.4.0` ReactiveUI the target platform and minimum version of Xamarin Forms was changed to be `3.0.0.561731` aka Fall Creators Update. I picked this as it felt like a reasonable baseline to us and it helps reduce the amount of SDK's one needs to have installed to be contribute to ReactiveUI. 

After some digging and discussions it appears that RS3 aka `16299` is the min version supported by `netstandard20` so this was the correct choice for now. It's not the correct choice going forward however.

I'm proposing that going forward we change our support matrix for Xamarin Forms to be as follows:

* the target platform will be wildcarded to the current major version of Xamarin.Forms.
* the min version is oldest possible that feels reasonable to maintain.


## Motivation

* https://docs.microsoft.com/en-us/nuget/reference/package-versioning#version-ranges-and-wildcards

## How we teach this

* Update https://reactiveui.net/docs/guidelines/platform/xamarin-forms with guidance of what we support
* Create https://reactiveui.net/contribute/maintainers/platform-knowledge/xamarin-forms/ with instructions for maintainers how/when to adjust these numbers