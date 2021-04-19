---
description: Déplacement du contenu sur l’appareil
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: Déplacement du contenu sur l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb4a9638e656d5cab8437448d64b79947df337b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533948"
---
# <a name="moving-content-on-the-device"></a><span data-ttu-id="51e5b-103">Déplacement du contenu sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="51e5b-103">Moving Content on the Device</span></span>

<span data-ttu-id="51e5b-104">Une autre opération courante accomplie par une application WPD est le transfert de contenu d’un emplacement à un autre sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="51e5b-104">Another common operation accomplished by a WPD application is the transfer of content from one location on the device to another.</span></span>

<span data-ttu-id="51e5b-105">Les opérations de déplacement de contenu sont effectuées à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="51e5b-105">Content move operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="51e5b-106">Interface</span><span class="sxs-lookup"><span data-stu-id="51e5b-106">Interface</span></span>                                                                                      | <span data-ttu-id="51e5b-107">Description</span><span class="sxs-lookup"><span data-stu-id="51e5b-107">Description</span></span>                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="51e5b-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="51e5b-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="51e5b-109">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="51e5b-109">Provides access to the content-specific methods.</span></span>  |
| [<span data-ttu-id="51e5b-110">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="51e5b-110">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="51e5b-111">Fournit l’accès aux méthodes spécifiques à la propriété.</span><span class="sxs-lookup"><span data-stu-id="51e5b-111">Provides access to the property-specific methods.</span></span> |



 

<span data-ttu-id="51e5b-112">La fonction MoveContentAlreadyOnDevice dans le module ContentTransfer. cpp de l’exemple d’application montre comment une application peut déplacer le contenu d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="51e5b-112">The MoveContentAlreadyOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application can move content from one location to another.</span></span>

<span data-ttu-id="51e5b-113">La première tâche accomplie par la fonction MoveContentAlreadyOnDevice consiste à interroger le pilote de périphérique pour voir s’il prend en charge le déplacement du contenu.</span><span class="sxs-lookup"><span data-stu-id="51e5b-113">The first task accomplished by the MoveContentAlreadyOnDevice function is to query the device driver to see whether it supports content movement.</span></span> <span data-ttu-id="51e5b-114">Pour ce faire, vous devez appeler la fonction d’assistance SupportsCommand et passer la \_ gestion des objets de commande wpd déplacer les \_ \_ \_ \_ objets en tant que deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="51e5b-114">This is accomplished by calling the SupportsCommand helper function and passing WPD\_COMMAND\_OBJECT\_MANAGEMENT\_MOVE\_OBJECTS as the second argument.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SupportsCommand(pDevice, WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS) == FALSE)
{
    printf("! This device does not support the move operation (i.e. The WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS command)\n");
    return;
}
```



<span data-ttu-id="51e5b-115">L’étape suivante consiste à inviter l’utilisateur à entrer deux identificateurs d’objet.</span><span class="sxs-lookup"><span data-stu-id="51e5b-115">The next step entails prompting the user to enter two object identifiers.</span></span> <span data-ttu-id="51e5b-116">La première est l’identificateur du contenu qui sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="51e5b-116">The first is the identifier for the content that will be moved.</span></span> <span data-ttu-id="51e5b-117">Le deuxième est l’identificateur de l’emplacement vers lequel l’application doit déplacer ce contenu.</span><span class="sxs-lookup"><span data-stu-id="51e5b-117">The second is the identifier for the location to which the application should move this content.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
printf("Enter the identifer of the object you wish to move.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}

// Prompt user to enter an object identifier on the device to move.
printf("Enter the identifer of the object you wish to move '%ws' to.\n>", wszSelection);
hr = StringCbGetsW(wszDestinationFolderObjectID,sizeof(wszDestinationFolderObjectID));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}
```



<span data-ttu-id="51e5b-118">Ensuite, l’exemple récupère un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) qui est utilisé pour accéder à la méthode [**IPortableDeviceContent :: Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) .</span><span class="sxs-lookup"><span data-stu-id="51e5b-118">Next, the sample retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object that is used to access the [**IPortableDeviceContent::Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="51e5b-119">Enfin, le contenu est déplacé.</span><span class="sxs-lookup"><span data-stu-id="51e5b-119">Finally, the content is moved.</span></span> <span data-ttu-id="51e5b-120">Ce processus implique les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="51e5b-120">This process involves the following:</span></span>

1.  <span data-ttu-id="51e5b-121">Création d’un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui reçoit une structure PROPVARIANT pour l’objet à déplacer.</span><span class="sxs-lookup"><span data-stu-id="51e5b-121">Creating an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that receives a PROPVARIANT structure for the object to be moved.</span></span>
2.  <span data-ttu-id="51e5b-122">Ajout de PROPVARIANT à l’objet IPortableDevicePropVariantCollection.</span><span class="sxs-lookup"><span data-stu-id="51e5b-122">Adding the PROPVARIANT to the IPortableDevicePropVariantCollection object.</span></span>
3.  <span data-ttu-id="51e5b-123">Appel de la méthode IPortableDeviceContent :: Move.</span><span class="sxs-lookup"><span data-stu-id="51e5b-123">Invoking the IPortableDeviceContent::Move method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDevicePropVariantCollection,
                          (VOID**) &pObjectsToMove);
    if (SUCCEEDED(hr))
    {
        if (pObjectsToMove != NULL)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);

            // Initialize a PROPVARIANT structure with the object identifier string
            // that the user selected above. Notice we are allocating memory for the
            // LPWSTR value.  This memory will be freed when PropVariantClear() is
            // called below.
            pv.vt      = VT_LPWSTR;
            pv.pwszVal = AtlAllocTaskWideString(wszSelection);
            if (pv.pwszVal != NULL)
            {
                // Add the object identifier to the objects-to-move list
                // (We are only moving 1 in this example)
                hr = pObjectsToMove->Add(&pv);
                if (SUCCEEDED(hr))
                {
                    // Attempt to move the object on the device
                    hr = pContent->Move(pObjectsToMove,               // Object(s) to move
                                        wszDestinationFolderObjectID, // Folder to move to
                                        NULL);                        // Object(s) that failed to delete (we are only moving 1, so we can pass NULL here)
                    if (SUCCEEDED(hr))
                    {
                        // An S_OK return lets the caller know that the deletion was successful
                        if (hr == S_OK)
                        {
                            printf("The object '%ws' was moved on the device.\n", wszSelection);
                        }

                        // An S_FALSE return lets the caller know that the move failed.
                        // The caller should check the returned IPortableDevicePropVariantCollection
                        // for a list of object identifiers that failed to be moved.
                        else
                        {
                            printf("The object '%ws' failed to be moved on the device.\n", wszSelection);
                        }
                    }
                    else
                    {
                        printf("! Failed to move an object on the device, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to move an object on the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
                printf("! Failed to move an object on the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
            }

            // Free any allocated values in the PROPVARIANT before exiting
            PropVariantClear(&pv);
        }
        else
        {
            printf("! Failed to move an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="51e5b-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51e5b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e5b-125">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="51e5b-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="51e5b-126">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="51e5b-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="51e5b-127">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="51e5b-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="51e5b-128">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="51e5b-128">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



