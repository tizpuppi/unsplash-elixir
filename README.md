# Unsplash

Unsplash API in Elixir.


## To Use

* `Unsplash.photos`
* `Unsplash.me`
...

more examples coming soon.

## Authorization

Get Auth code by directing user to the url generated by this command (replace the scope with what you would like):
`Unsplash.OAuth.authorize_url! scope: "public read_user write_user read_photos write_photos"`

After the user grants access, she will be redirected back to your redirect_uri whith a `code` query paramater, which you then set like this:
`Unsplash.OAuth.authorize!(code: auth_code_from_the_callback)`

Now every API call will use the access_code gerenated in the above step automatically.

## Todo

* Start the agent automatially with Application
* Documentation
* Tests

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed as:

  1. Add unsplash to your list of dependencies in `mix.exs`:

        def deps do
          [{:unsplash, "~> 0.0.1"}]
        end

  2. Ensure unsplash is started before your application:

        def application do
          [applications: [:unsplash]]
        end
