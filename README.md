# Nas To Adls


# Execute the following Steps on LINUX servers:

This document outlines the steps to execute on Linux servers to download and use AzCopy for copying files to Azure Blob Storage.

## Prerequisites
- A valid Azure Blob Storage account and storage container

## Steps

1. Download AzCopy by running the following command in the Linux terminal:

    wget https://aka.ms/downloadazcopy-v10-linux

2. Extract the downloaded archive using the following command:

    tar xvf downloadazcopy-v10-linux

3. Navigate to the extracted directory using the following command:

    cd azcopy_linux_amd64_10.18.1

4. Verify that AzCopy is working by running the following command:

    ./azcopy

5. Copy files from the local directory `/MyTestDir/` to Azure Blob Storage using the following command:

    ./azcopy cp /MyTestDir/ "https://adls.blob.core.windows.net/mystorage/MyTestDir?sp=rw&st=2023-05-12T16:48:38Z&se=2100-05-13T00:48:38Z&spr=https&sv=2022-11-02&sr=d&sig=kQazdd=1" --recursive=true


Note: Replace the `URL` with your own Azure Blob Storage URL.
