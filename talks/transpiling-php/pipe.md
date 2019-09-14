https://wiki.php.net/rfc/pipe-operator




function read_password_from_config()
{

    return "/path/config.json"
            |> read_file_content()
            |> decode_json()
            |> get_value("password")
}
function read_file_content(string $filePath): string{
    ..
}
function decode_json(string $content): array{
    ..
}
function get_value(array $data): string{
    ..
}

function read_password_from_config()
{
    $file_path = "/path/config.json";

    $content = read_file_content($file_path);

    $data = decode_json($content);

    return get_value($data,["password"]);
}



function read_password_from_config()
{

    return get_value(
        decode_json(
            read_file_content(
                "/path/config.json"
            )
        )
        ,"password"
    );

}