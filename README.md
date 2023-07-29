# ipfsPython
upload files to ipfs in python

API Endpoints and Gateway URL: The code defines the api_url and gateway_url, which are the URLs for the IPFS API and the IPFS gateway, respectively. The IPFS API is used to interact with the IPFS network programmatically, while the IPFS gateway allows users to access files in IPFS through HTTP.

Add a File to IPFS: The add_file function takes the filename of a file you want to add to IPFS. It opens the file in binary read mode ('rb'), constructs a dictionary containing the file as data, and sends a POST request to the IPFS API endpoint /add to add the file to the IPFS network. The response contains a JSON with the CID of the added file, which is extracted and returned by the function.

Retrieve a File from IPFS: The get_file function takes the file hash (CID) of a file stored in IPFS and an output_file where you want to save the retrieved content. It sends a GET request to the IPFS gateway, using the /ipfs/ route followed by the CID, to retrieve the content of the file. The content is then written to the specified output_file.

Test the Functions: The code tests the functions by adding a file named 'myfile.txt' to IPFS and then retrieving it using the generated CID. The retrieved content is saved as 'output.txt'.

Before running the code, make sure that you have an IPFS node running locally, and the API and gateway URLs (api_url and gateway_url) are correct based on your IPFS configuration. Additionally, ensure that 'myfile.txt' exists in the same directory as the script.

Please note that IPFS is a peer-to-peer network, and to access files added to IPFS using the gateway_url, you may need to have access to the IPFS network or use a public IPFS gateway. If you are running an IPFS node locally, you can use localhost as the gateway URL. However, if you want to share the files with others, you may need to use a public gateway URL instead.
