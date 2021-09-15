---
description: transfert d’une Image ou d’un fichier Musique sur l’appareil
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: transfert d’une Image ou d’un fichier Musique sur l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522873"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a>transfert d’une Image ou d’un fichier Musique sur l’appareil

L’une des opérations les plus courantes accomplies par une application est le transfert de contenu vers un appareil connecté.

Les transferts de contenu sont effectués à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                | Description                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Fournit l’accès aux méthodes spécifiques au contenu.               |
| [**Interface IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | Utilisé lors de l’écriture du contenu sur l’appareil.                   |
| [**Interface IPortableDeviceValues**](iportabledevicevalues.md)         | Utilisé pour récupérer des propriétés qui décrivent le contenu.         |
| IStream, interface                                                        | Utilisé pour simplifier la lecture du contenu et l’écriture sur l’appareil. |



 

La `TransferContentToDevice` fonction dans le module ContentTransfer. cpp de l’exemple d’application montre comment une application peut transférer le contenu d’un PC vers un appareil connecté. Dans cet exemple, le contenu transféré peut être un fichier contenant une image, une musique ou des informations de contact.

La première tâche accomplie par la `TransferContentToDevice` fonction consiste à inviter l’utilisateur à entrer un identificateur d’objet, qui identifie l’objet à transférer.


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



La deuxième tâche accomplie par la `TransferContentToDevice` fonction consiste à créer un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) en appelant la méthode [**IPortableDevice :: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



La tâche suivante accomplie par la `TransferContentToDevice` fonction est la création d’une boîte de dialogue **FileOpen** avec laquelle l’utilisateur peut spécifier l’emplacement et le nom du fichier à transférer.


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



La `TransferContentToDevice` fonction passe une chaîne de filtre ( `wszFileTypeFilter` ) à la méthode GetOpenFileName, qui détermine le type de fichiers que l’utilisateur peut choisir. Reportez-vous à la `DoMenu` fonction dans le module WpdApiSample. cpp pour obtenir des exemples des trois filtres différents autorisés par l’exemple.

Une fois que l’utilisateur a identifié un fichier particulier à transférer sur l’appareil, la `TransferContentToDevice` fonction ouvre ce fichier en tant qu’objet IStream et récupère les propriétés requises pour effectuer le transfert.


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



Les propriétés requises sont récupérées en appelant la `GetRequiredPropertiesForContentType` fonction Helper, qui opère sur l’objet IStream. La `GetRequiredPropertiesForContentType` fonction d’assistance crée un objet [**IPortableDeviceValues**](iportabledevicevalues.md) , récupère les propriétés de la liste suivante et les ajoute à cet objet.

-   Identificateur de l’objet parent
-   Taille du flux en octets
-   Nom du fichier de contenu
-   Nom du contenu (nom de fichier sans extension)
-   Type de contenu (image, audio ou contact)
-   Format du contenu (JFIF, WMA ou vCard2)

L’exemple d’application utilise les propriétés récupérées pour créer le nouveau contenu sur l’appareil. Cette opération s’effectue en trois phases :

1.  L’application appelle la méthode [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) pour créer un nouvel objet IStream sur l’appareil.
2.  L’application utilise cet objet pour obtenir un objet [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) à partir du pilote wpd.
3.  L’application utilise le nouvel objet **IPortableDeviceDataStream** pour écrire le contenu sur l’appareil (à l’aide de la fonction d’assistance StreamCopy). La fonction d’assistance écrit les données du fichier source dans le flux retourné par [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).
4.  L’application termine l’opération en appelant la méthode Commit sur le flux de destination.


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



