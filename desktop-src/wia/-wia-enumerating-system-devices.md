---
description: 'Utilisez la méthode IWiaDevMgr :: EnumDeviceInfo (ou IWiaDevMgr2 :: EnumDeviceInfo) pour énumérer les périphériques WIA (Windows Image Acquisition) installés sur un système.'
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Énumération des périphériques système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952072"
---
# <a name="enumerating-system-devices"></a><span data-ttu-id="31b3d-103">Énumération des périphériques système</span><span class="sxs-lookup"><span data-stu-id="31b3d-103">Enumerating System Devices</span></span>

<span data-ttu-id="31b3d-104">Utilisez la méthode [**IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2 :: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) pour énumérer les périphériques WIA (Windows Image Acquisition) installés sur un système.</span><span class="sxs-lookup"><span data-stu-id="31b3d-104">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method to enumerate the Windows Image Acquisition (WIA) devices installed on a system.</span></span> <span data-ttu-id="31b3d-105">Cette méthode crée un objet d’énumération pour les propriétés des appareils et retourne un pointeur vers l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) que l’objet d’énumération prend en charge.</span><span class="sxs-lookup"><span data-stu-id="31b3d-105">This method creates an enumeration object for the properties of the devices, and returns a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface that the enumeration object supports.</span></span>

<span data-ttu-id="31b3d-106">Vous pouvez ensuite utiliser les méthodes de l’interface [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pour obtenir un pointeur d’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pour chaque périphérique installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="31b3d-106">You can then use the methods of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointer for each device installed on the system.</span></span>

<span data-ttu-id="31b3d-107">Le code suivant de l’exemple d’application WiaSSamp montre comment créer un objet d’énumération pour les périphériques sur un système et comment itérer au sein de ces périphériques :</span><span class="sxs-lookup"><span data-stu-id="31b3d-107">The following code from the WiaSSamp sample application demonstrates how to create an enumeration object for the devices on a system and iterate through those devices:</span></span>


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



<span data-ttu-id="31b3d-108">WIA \_ DevInfo \_ enum \_ local est une constante WIA qui représente la seule valeur valide pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="31b3d-108">WIA\_DEVINFO\_ENUM\_LOCAL is a WIA constant that represents the only valid value for this parameter.</span></span>

<span data-ttu-id="31b3d-109">Dans l’exemple, le paramètre **pWiaDevMgr** pointe vers une instance de l’interface [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) après un appel précédent à [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="31b3d-109">In the example, the parameter **pWiaDevMgr** points to an instance of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface after a previous call to [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="31b3d-110">L’application appelle la [**méthode IWiaDevMgr :: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (ou [**IWiaDevMgr2 :: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md) [**) du pointeur IWiaDevMgr (**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) ou [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) qui remplit **pWiaDevMgr** avec l’adresse d' **un pointeur vers** l’interface [**pWiaEnumDevInfo \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="31b3d-110">The application calls the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) pointer **pWiaDevMgr** that fills **pWiaEnumDevInfo** with the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

<span data-ttu-id="31b3d-111">Si l’appel a échoué, l’application appelle ensuite la méthode [**IEnumWIA \_ dev \_ info :: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) du pointeur d' [**\_ \_ informations de développement IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="31b3d-111">If the call succeeds, the application then calls the [**IEnumWIA\_DEV\_INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer.</span></span> <span data-ttu-id="31b3d-112">La variable **pWiaEnumDevInfo** garantit que l’énumération commence au début.</span><span class="sxs-lookup"><span data-stu-id="31b3d-112">The **pWiaEnumDevInfo** variable ensures that the enumeration starts at the beginning.</span></span>

<span data-ttu-id="31b3d-113">Si cet appel réussit, l’application itère au sein des appareils du système en appelant à plusieurs reprises la méthode [**IEnumWIA \_ dev \_ info :: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) du pointeur [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** jusqu’à ce que la méthode ne retourne plus la valeur \_ OK, indiquant ainsi que l’énumération est terminée.</span><span class="sxs-lookup"><span data-stu-id="31b3d-113">If this call succeeds, the application iterates through the devices on the system by repeatedly calling the [**IEnumWIA\_DEV\_INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer **pWiaEnumDevInfo** until the method no longer returns S\_OK, indicating that the enumeration is complete.</span></span>

<span data-ttu-id="31b3d-114">Chaque appel à **pWiaEnumDevInfo->remplit ensuite** **pWiaPropertyStorage** avec un pointeur vers l’interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) qui contient les informations de propriété pour un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="31b3d-114">Each call to **pWiaEnumDevInfo->Next** fills **pWiaPropertyStorage** with a pointer to the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface that contains property information for a specific device.</span></span>

 

 
