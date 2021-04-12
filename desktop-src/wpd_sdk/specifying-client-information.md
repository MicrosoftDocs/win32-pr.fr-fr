---
description: Spécification des informations sur le client
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Spécification des informations sur le client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f6ca094b627b6c2cee16ec587a8c850cd17f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209758"
---
# <a name="specifying-client-information"></a><span data-ttu-id="382cc-103">Spécification des informations sur le client</span><span class="sxs-lookup"><span data-stu-id="382cc-103">Specifying Client Information</span></span>

<span data-ttu-id="382cc-104">Les informations client fournies dans le deuxième argument sont utilisées par certains pilotes de périphérique pour optimiser les performances de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="382cc-104">The client information supplied in the second argument is used by some device drivers to optimize device performance.</span></span> <span data-ttu-id="382cc-105">Au minimum, votre application doit fournir une chaîne contenant son nom, un numéro de version principale, un numéro de version mineure et un numéro de révision.</span><span class="sxs-lookup"><span data-stu-id="382cc-105">At a minimum, your application should provide a string containing its name, a major version number, a minor version number, and a revision number.</span></span> <span data-ttu-id="382cc-106">Il s’agit des champs fournis par l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="382cc-106">These are the fields supplied by the sample application.</span></span>


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



<span data-ttu-id="382cc-107">La `GetClientInformation` fonction dans l’exemple d’application crée et remplit une interface **IPortableDeviceValues** avec les informations du client.</span><span class="sxs-lookup"><span data-stu-id="382cc-107">The `GetClientInformation` function in the sample application creates and populates an **IPortableDeviceValues** interface with client information.</span></span> <span data-ttu-id="382cc-108">Cette fonction comporte deux parties principales.</span><span class="sxs-lookup"><span data-stu-id="382cc-108">This function has two primary parts.</span></span> <span data-ttu-id="382cc-109">La première partie crée une instance d’un objet Device-values portable en appelant la fonction CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="382cc-109">The first part creates an instance of a portable device-values object by calling the CoCreateInstance function.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



<span data-ttu-id="382cc-110">La deuxième partie définit les informations du client dans l’objet portable Device-values.</span><span class="sxs-lookup"><span data-stu-id="382cc-110">The second part sets the client information in the portable device-values object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a><span data-ttu-id="382cc-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="382cc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="382cc-112">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="382cc-112">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="382cc-113">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="382cc-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="382cc-114">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="382cc-114">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



