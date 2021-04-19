---
description: Transfert d’une image ou d’un fichier musical vers l’appareil
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Transfert d’une image ou d’un fichier musical vers l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524382"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a><span data-ttu-id="28b9d-103">Transfert d’une image ou d’un fichier musical vers l’appareil</span><span class="sxs-lookup"><span data-stu-id="28b9d-103">Transferring an Image or Music File to the Device</span></span>

<span data-ttu-id="28b9d-104">L’une des opérations les plus courantes accomplies par une application est le transfert de contenu vers un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="28b9d-104">One of the most common operations accomplished by an application is the transfer of content to a connected device.</span></span>

<span data-ttu-id="28b9d-105">Les transferts de contenu sont effectués à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="28b9d-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="28b9d-106">Interface</span><span class="sxs-lookup"><span data-stu-id="28b9d-106">Interface</span></span>                                                                | <span data-ttu-id="28b9d-107">Description</span><span class="sxs-lookup"><span data-stu-id="28b9d-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="28b9d-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="28b9d-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="28b9d-109">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="28b9d-109">Provides access to the content-specific methods.</span></span>               |
| [<span data-ttu-id="28b9d-110">**Interface IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="28b9d-110">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | <span data-ttu-id="28b9d-111">Utilisé lors de l’écriture du contenu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="28b9d-111">Used when writing the content to the device.</span></span>                   |
| [<span data-ttu-id="28b9d-112">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="28b9d-112">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="28b9d-113">Utilisé pour récupérer des propriétés qui décrivent le contenu.</span><span class="sxs-lookup"><span data-stu-id="28b9d-113">Used to retrieve properties that describe the content.</span></span>         |
| <span data-ttu-id="28b9d-114">IStream, interface</span><span class="sxs-lookup"><span data-stu-id="28b9d-114">IStream Interface</span></span>                                                        | <span data-ttu-id="28b9d-115">Utilisé pour simplifier la lecture du contenu et l’écriture sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="28b9d-115">Used to simplify reading of content and writing to the device.</span></span> |



 

<span data-ttu-id="28b9d-116">La `TransferContentToDevice` fonction dans le module ContentTransfer. cpp de l’exemple d’application montre comment une application peut transférer le contenu d’un PC vers un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="28b9d-116">The `TransferContentToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer content from a PC to a connected device.</span></span> <span data-ttu-id="28b9d-117">Dans cet exemple, le contenu transféré peut être un fichier contenant une image, une musique ou des informations de contact.</span><span class="sxs-lookup"><span data-stu-id="28b9d-117">In this particular sample, the transferred content can be a file containing an image, music, or contact information.</span></span>

<span data-ttu-id="28b9d-118">La première tâche accomplie par la `TransferContentToDevice` fonction consiste à inviter l’utilisateur à entrer un identificateur d’objet, qui identifie l’objet à transférer.</span><span class="sxs-lookup"><span data-stu-id="28b9d-118">The first task accomplished by the `TransferContentToDevice` function is to prompt the user to enter an object identifier, which identifies the object to be transferred.</span></span>


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



<span data-ttu-id="28b9d-119">La deuxième tâche accomplie par la `TransferContentToDevice` fonction consiste à créer un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) en appelant la méthode [**IPortableDevice :: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="28b9d-119">The second task accomplished by the `TransferContentToDevice` function is to create an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


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



<span data-ttu-id="28b9d-120">La tâche suivante accomplie par la `TransferContentToDevice` fonction est la création d’une boîte de dialogue **FileOpen** avec laquelle l’utilisateur peut spécifier l’emplacement et le nom du fichier à transférer.</span><span class="sxs-lookup"><span data-stu-id="28b9d-120">The next task accomplished by the `TransferContentToDevice` function is the creation of a **FileOpen** dialog with which the user can specify the location and name of the file to be transferred.</span></span>


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



<span data-ttu-id="28b9d-121">La `TransferContentToDevice` fonction passe une chaîne de filtre ( `wszFileTypeFilter` ) à la méthode GetOpenFileName, qui détermine le type de fichiers que l’utilisateur peut choisir.</span><span class="sxs-lookup"><span data-stu-id="28b9d-121">The `TransferContentToDevice` function passes a filter string (`wszFileTypeFilter`) to the GetOpenFileName method, which determines the type of files that the user can choose.</span></span> <span data-ttu-id="28b9d-122">Reportez-vous à la `DoMenu` fonction dans le module WpdApiSample. cpp pour obtenir des exemples des trois filtres différents autorisés par l’exemple.</span><span class="sxs-lookup"><span data-stu-id="28b9d-122">Refer to the `DoMenu` function in the WpdApiSample.cpp module for examples of the three different filters allowed by the sample.</span></span>

<span data-ttu-id="28b9d-123">Une fois que l’utilisateur a identifié un fichier particulier à transférer sur l’appareil, la `TransferContentToDevice` fonction ouvre ce fichier en tant qu’objet IStream et récupère les propriétés requises pour effectuer le transfert.</span><span class="sxs-lookup"><span data-stu-id="28b9d-123">After the user identifies a particular file for transfer to the device, the `TransferContentToDevice` function opens that file as an IStream object and retrieves properties that are required to complete the transfer.</span></span>


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



<span data-ttu-id="28b9d-124">Les propriétés requises sont récupérées en appelant la `GetRequiredPropertiesForContentType` fonction Helper, qui opère sur l’objet IStream.</span><span class="sxs-lookup"><span data-stu-id="28b9d-124">The required properties are retrieved by calling the`GetRequiredPropertiesForContentType` helper-function, which operates on the IStream object.</span></span> <span data-ttu-id="28b9d-125">La `GetRequiredPropertiesForContentType` fonction d’assistance crée un objet [**IPortableDeviceValues**](iportabledevicevalues.md) , récupère les propriétés de la liste suivante et les ajoute à cet objet.</span><span class="sxs-lookup"><span data-stu-id="28b9d-125">The `GetRequiredPropertiesForContentType` helper-function creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, retrieves the properties in the following list, and adds them to this object.</span></span>

-   <span data-ttu-id="28b9d-126">Identificateur de l’objet parent</span><span class="sxs-lookup"><span data-stu-id="28b9d-126">Parent-object identifier</span></span>
-   <span data-ttu-id="28b9d-127">Taille du flux en octets</span><span class="sxs-lookup"><span data-stu-id="28b9d-127">Stream size in bytes</span></span>
-   <span data-ttu-id="28b9d-128">Nom du fichier de contenu</span><span class="sxs-lookup"><span data-stu-id="28b9d-128">Content file name</span></span>
-   <span data-ttu-id="28b9d-129">Nom du contenu (nom de fichier sans extension)</span><span class="sxs-lookup"><span data-stu-id="28b9d-129">Content name (the file name without the extension)</span></span>
-   <span data-ttu-id="28b9d-130">Type de contenu (image, audio ou contact)</span><span class="sxs-lookup"><span data-stu-id="28b9d-130">Content type (image, audio, or contact)</span></span>
-   <span data-ttu-id="28b9d-131">Format du contenu (JFIF, WMA ou vCard2)</span><span class="sxs-lookup"><span data-stu-id="28b9d-131">Content format (JFIF, WMA, or vCard2)</span></span>

<span data-ttu-id="28b9d-132">L’exemple d’application utilise les propriétés récupérées pour créer le nouveau contenu sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="28b9d-132">The sample application uses the retrieved properties to create the new content on the device.</span></span> <span data-ttu-id="28b9d-133">Cette opération s’effectue en trois phases :</span><span class="sxs-lookup"><span data-stu-id="28b9d-133">This is done in three phases:</span></span>

1.  <span data-ttu-id="28b9d-134">L’application appelle la méthode [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) pour créer un nouvel objet IStream sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="28b9d-134">The application calls [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) method to create a new IStream object on the device.</span></span>
2.  <span data-ttu-id="28b9d-135">L’application utilise cet objet pour obtenir un objet [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) à partir du pilote wpd.</span><span class="sxs-lookup"><span data-stu-id="28b9d-135">The application uses this object to obtain an [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) object from the WPD driver.</span></span>
3.  <span data-ttu-id="28b9d-136">L’application utilise le nouvel objet **IPortableDeviceDataStream** pour écrire le contenu sur l’appareil (à l’aide de la fonction d’assistance StreamCopy).</span><span class="sxs-lookup"><span data-stu-id="28b9d-136">The application uses the new **IPortableDeviceDataStream** object to write the content to the device (via the StreamCopy helper function).</span></span> <span data-ttu-id="28b9d-137">La fonction d’assistance écrit les données du fichier source dans le flux retourné par [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="28b9d-137">The helper function writes the data from the source file to the stream returned by [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span>
4.  <span data-ttu-id="28b9d-138">L’application termine l’opération en appelant la méthode Commit sur le flux de destination.</span><span class="sxs-lookup"><span data-stu-id="28b9d-138">The application completes the operation by calling the Commit method on the destination stream.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="28b9d-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28b9d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28b9d-140">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="28b9d-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="28b9d-141">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="28b9d-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="28b9d-142">**Interface IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="28b9d-142">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[<span data-ttu-id="28b9d-143">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="28b9d-143">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="28b9d-144">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="28b9d-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



