https://wiki.php.net/rfc/pipe-operator





class InvoiceController{
    

    function create_invoice(Framework\Request $request){

        return $request
                |> create_invoice_from_request()
                |> save_invoice()
                |> build_response()

    }
}


function read_password_from_config()
{

    return "/path/config.json"
            |> read_file_content()
            |> decode_json()
            |> get_value("password");
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