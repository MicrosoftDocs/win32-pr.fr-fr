---
description: Ajout d’une ressource à un objet
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: Ajout d’une ressource à un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869b5cdcf172c4b8f27f7081bfce8e6f05073789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319610"
---
# <a name="adding-a-resource-to-an-object"></a><span data-ttu-id="2b849-103">Ajout d’une ressource à un objet</span><span class="sxs-lookup"><span data-stu-id="2b849-103">Adding a Resource to an Object</span></span>

<span data-ttu-id="2b849-104">En plus de transférer des objets sur un appareil, il est également possible d’ajouter des ressources aux objets.</span><span class="sxs-lookup"><span data-stu-id="2b849-104">In addition to transferring objects to a device, it's also possible to add resources to objects.</span></span> <span data-ttu-id="2b849-105">Par exemple, une application peut ajouter une photo à des informations existantes pour un contact donné.</span><span class="sxs-lookup"><span data-stu-id="2b849-105">For example, an application could add a photo to existing information for a given contact.</span></span>

<span data-ttu-id="2b849-106">Les ressources sont ajoutées à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2b849-106">Resources are added using the interfaces described in the following table.</span></span>



| <span data-ttu-id="2b849-107">Interface</span><span class="sxs-lookup"><span data-stu-id="2b849-107">Interface</span></span>                                                              | <span data-ttu-id="2b849-108">Description</span><span class="sxs-lookup"><span data-stu-id="2b849-108">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="2b849-109">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="2b849-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | <span data-ttu-id="2b849-110">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="2b849-110">Provides access to the content-specific methods.</span></span>                  |
| [<span data-ttu-id="2b849-111">**Interface IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="2b849-111">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | <span data-ttu-id="2b849-112">Utilisé lors de l’écriture des propriétés de ressource et des données sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b849-112">Used when writing the resource properties and data to the device.</span></span> |
| [<span data-ttu-id="2b849-113">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="2b849-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)       | <span data-ttu-id="2b849-114">Utilisé pour écrire des propriétés qui décrivent la ressource.</span><span class="sxs-lookup"><span data-stu-id="2b849-114">Used to write properties that describe the resource.</span></span>              |
| <span data-ttu-id="2b849-115">IStream, interface</span><span class="sxs-lookup"><span data-stu-id="2b849-115">IStream Interface</span></span>                                                      | <span data-ttu-id="2b849-116">Utilisé pour simplifier l’écriture de la ressource sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b849-116">Used to simplify writing the resource to the device.</span></span>              |



 

<span data-ttu-id="2b849-117">La fonction CreateContactPhotoResourceOnDevice dans le module ContentTransfer. cpp de l’exemple d’application montre comment une application peut ajouter une ressource photo à un objet contact.</span><span class="sxs-lookup"><span data-stu-id="2b849-117">The CreateContactPhotoResourceOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application could add a photo resource to a contact object.</span></span> <span data-ttu-id="2b849-118">Cette fonction invite l’utilisateur à indiquer l’identificateur d’objet du contact sur l’appareil, auquel la ressource de photo sera ajoutée.</span><span class="sxs-lookup"><span data-stu-id="2b849-118">This function prompts the user for the object identifier of the contact on the device, to which the photo resource will be added.</span></span> <span data-ttu-id="2b849-119">Ensuite, il affiche une boîte de dialogue FileOpen qui permet à l’utilisateur de sélectionner l’image à ajouter.</span><span class="sxs-lookup"><span data-stu-id="2b849-119">Then it displays a FileOpen dialog box so that the user can select the image to be added.</span></span> <span data-ttu-id="2b849-120">Une fois ces données collectées, l’application écrit la ressource sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b849-120">Once this data is collected, the application writes the resource to the device.</span></span>

<span data-ttu-id="2b849-121">La première tâche accomplie par la fonction CreateContactPhotoResourceOnDevice consiste à inviter l’utilisateur à entrer un identificateur d’objet pour le contact auquel la photo sera ajoutée.</span><span class="sxs-lookup"><span data-stu-id="2b849-121">The first task accomplished by the CreateContactPhotoResourceOnDevice function is to prompt the user to enter an object identifier for the contact to which the photo will be added.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
printf("Enter the identifer of the object to which we will add an Audio annotation.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting resource creation\n");
}do
```



<span data-ttu-id="2b849-122">L’étape suivante est la récupération d’un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , qui à son tour est utilisé pour obtenir un objet [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) .</span><span class="sxs-lookup"><span data-stu-id="2b849-122">The next step is the retrieval of an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which in turn is used to obtain an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object.</span></span> <span data-ttu-id="2b849-123">(L’application utilise ce dernier objet pour créer et écrire la nouvelle ressource.)</span><span class="sxs-lookup"><span data-stu-id="2b849-123">(The application uses this latter object to create and write the new resource.)</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}





if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="2b849-124">Après cela, l’exemple affiche la boîte de dialogue **FileOpen** , qui permet à l’utilisateur de spécifier le nom du fichier image qui contient la photo qu’il souhaite ajouter aux informations de contact.</span><span class="sxs-lookup"><span data-stu-id="2b849-124">After this, the sample displays the **FileOpen** dialog box, which allows the user to specify the name of the image file that contains the photo they want to add to the contact information.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = wszFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(wszFilePath);
    OpenFileNameInfo.lpstrFilter    = L"JPEG (*.JPG)\0*.JPG\0JPEG (*.JPEG)\0*.JPEG\0JPG (*.JPE)\0*.JPE\0JPG (*.JFIF)\0*.JFIF\0\0";;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = L"JPG";

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was cancelled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="2b849-125">Une fois que l’exemple a un objet [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) et le nom du fichier image, il effectue les opérations suivantes pour préparer le transfert de données vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b849-125">Once the sample has an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object and the name of the image file, it does the following in preparation for actually transferring data to the device.</span></span>

1.  <span data-ttu-id="2b849-126">Il ouvre un objet IStream sur le fichier sélectionné pour les opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="2b849-126">It opens an IStream object on the selected file for read operations.</span></span>
2.  <span data-ttu-id="2b849-127">Il crée un objet [**IPortableDeviceValues**](iportabledevicevalues.md) , qui contient des informations telles que la taille et le format de l’image.</span><span class="sxs-lookup"><span data-stu-id="2b849-127">It creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, which will contain information such as the image size and format.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(wszFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // CoCreate the IPortableDeviceValues to hold the resource attributes
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pResourceAttributes);
        if (SUCCEEDED(hr))
        {
            // Fill in the necessary information regarding this resource

            // Set the WPD_OBJECT_ID.  This informs the driver which object this request is intended for.
            hr = pResourceAttributes->SetStringValue(WPD_OBJECT_ID, wszSelection);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID when creating a resource, hr = 0x%lx\n",hr);
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetKeyValue(WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY, WPD_RESOURCE_CONTACT_PHOTO);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE by requesting the total size of the
            // data stream.
            if (SUCCEEDED(hr))
            {
                STATSTG statstg = {0};
                hr = pFileStream->Stat(&statstg, STATFLAG_NONAME);
                if (SUCCEEDED(hr))
                {
                    hr = pResourceAttributes->SetUnsignedLargeIntegerValue(WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, statstg.cbSize.QuadPart);
                    if (FAILED(hr))
                    {
                        printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to get file's total size, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF because we are
            // creating a contact photo resource with JPG image data.
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetGuidValue(WPD_RESOURCE_ATTRIBUTE_FORMAT, WPD_OBJECT_FORMAT_JFIF);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF, hr = 0x%lx\n",hr);
                }
            }
        }

    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",wszFilePath, hr);
    }
}
```



<span data-ttu-id="2b849-128">Après avoir préparé les objets IStream et [**IPortableDeviceValues**](iportabledevicevalues.md) pour l’opération d’écriture, l’exemple transfère l’image sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b849-128">After preparing the IStream and [**IPortableDeviceValues**](iportabledevicevalues.md) objects for the write operation, the sample transfers the image to the device.</span></span> <span data-ttu-id="2b849-129">L’exemple termine le transfert en trois étapes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="2b849-129">The sample completes the transfer in three steps, as follows:</span></span>

1.  <span data-ttu-id="2b849-130">Il crée la ressource sur l’appareil en appelant la méthode [**IPortableDeviceResources :: CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) .</span><span class="sxs-lookup"><span data-stu-id="2b849-130">It creates the resource on the device by calling the [**IPortableDeviceResources::CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) method.</span></span>
2.  <span data-ttu-id="2b849-131">Elle appelle une fonction d’assistance StreamCopy pour copier le flux source dans le flux de destination.</span><span class="sxs-lookup"><span data-stu-id="2b849-131">It calls a StreamCopy helper function to copy the source stream to the destination stream.</span></span>
3.  <span data-ttu-id="2b849-132">Il informe le pilote de périphérique que le transfert est terminé en appelant la méthode IPortableDeviceDataStream :: Commit.</span><span class="sxs-lookup"><span data-stu-id="2b849-132">It informs the device driver that the transfer is complete by calling the IPortableDeviceDataStream::Commit method.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pResources->CreateResource(pResourceAttributes,    // Properties describing this resource
                                    &pResourceStream,       // Returned resource data stream (to transfer the data to)
                                    &cbOptimalTransferSize, // Returned optimal buffer size to use during transfer
                                    NULL);


    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pResourceStream,        // Destination (The resource to transfer to)
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
        hr = pResourceStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit resource to device, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="2b849-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b849-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b849-134">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="2b849-134">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="2b849-135">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="2b849-135">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="2b849-136">**Interface IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="2b849-136">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[<span data-ttu-id="2b849-137">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="2b849-137">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2b849-138">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="2b849-138">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



