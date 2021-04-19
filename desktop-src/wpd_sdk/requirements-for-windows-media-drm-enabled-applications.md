---
description: Configuration requise pour les applications Windows Media DRM-Enabled
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Configuration requise pour les applications Windows Media DRM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535112"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="d6764-103">Configuration requise pour les applications Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="d6764-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="d6764-104">Pour créer une application compatible avec Windows Media Digital Rights Management (DRM), vous devez disposer des en-têtes et des bibliothèques décrits dans la section [configuration générale requise pour le développement d’applications](general-requirements-for-application-development.md) de ce document.</span><span class="sxs-lookup"><span data-stu-id="d6764-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="d6764-105">En outre, l’application doit fournir des propriétés supplémentaires dans les informations du client lors de l’ouverture de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d6764-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="d6764-106">Les deux propriétés supplémentaires requises pour activer les transferts de contenu protégés par DRM Windows Media sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6764-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="d6764-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="d6764-107">Property</span></span>                                      | <span data-ttu-id="d6764-108">Description</span><span class="sxs-lookup"><span data-stu-id="d6764-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="d6764-109">\_ \_ \_ clé privée d’application \_ WMDRM \_ du client wpd</span><span class="sxs-lookup"><span data-stu-id="d6764-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="d6764-110">Spécifie la clé privée de l’application.</span><span class="sxs-lookup"><span data-stu-id="d6764-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="d6764-111">\_certificat d' \_ \_ application WMDRM du client \_ wpd</span><span class="sxs-lookup"><span data-stu-id="d6764-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="d6764-112">Spécifie le certificat de l’application.</span><span class="sxs-lookup"><span data-stu-id="d6764-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="d6764-113">Ces propriétés doivent être fournies dans les informations du client de l’application lorsque l’appareil est ouvert à l’aide de la méthode [**IPortableDevice :: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .</span><span class="sxs-lookup"><span data-stu-id="d6764-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="d6764-114">Lorsque ces propriétés sont fournies, l’API WPD autorise les transferts de contenu protégés.</span><span class="sxs-lookup"><span data-stu-id="d6764-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="d6764-115">Si l’application a fourni un certificat et une clé privée, l’API crée un canal sécurisé pour transférer le contenu WMDRM protégé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d6764-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="d6764-116">Pour plus d’informations sur la création et la distribution d’applications Windows qui prennent en charge la gestion des droits numériques Windows Media, consultez la rubrique suivante sur la [licence des applications Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d6764-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="d6764-117">Transfert de contenu</span><span class="sxs-lookup"><span data-stu-id="d6764-117">Transferring Content</span></span>

<span data-ttu-id="d6764-118">Pour transférer le contenu protégé WMDRM, utilisez [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="d6764-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="d6764-119">Cette méthode peut être utilisée pour le contenu protégé et en clair sans options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d6764-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="d6764-120">L’API WPD sélectionne automatiquement le canal protégé ou en clair, selon que le contenu est protégé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="d6764-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="d6764-121">Il interagit avec le fournisseur de contenu sécurisé WMDRM pour traiter les licences WMDRM.</span><span class="sxs-lookup"><span data-stu-id="d6764-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="d6764-122">Transfert de contenu clair connu</span><span class="sxs-lookup"><span data-stu-id="d6764-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="d6764-123">Si vous avez activé votre application pour gérer le contenu protégé, mais que vous savez qu’un fichier spécifique n’est pas protégé, vous pouvez indiquer à WPD d’ignorer le traitement DRM en définissant l' **option d’API WPD utiliser l’option d' \_ \_ \_ \_ effacement des \_ \_ flux de données** avec la valeur true dans le **IPortableDeviceValues** d’entrée lors de l’appel de [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) pour effacer le contenu.</span><span class="sxs-lookup"><span data-stu-id="d6764-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="d6764-124">Accès aux opérations de contrôle à l’aide de IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="d6764-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="d6764-125">WPD fournit un mécanisme permettant d’accéder aux API **IWMDRMDeviceApp** pour les mises à jour de licence et la récupération des données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d6764-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="d6764-126">Pour accéder à cette API via WPD, appelez **QueryInterface** sur **IID \_ IWMDRMDeviceApp** à partir de l' **IStream** retourné par [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="d6764-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="d6764-127">Cette instance **IWMDRMDeviceApp** est liée à la connexion **IPortableDevice** à votre appareil compatible WMDRM, et non au contenu spécifique dans lequel l' **IStream** a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="d6764-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="d6764-128">WPD encapsule en interne les API de contrôle et les rend accessibles à votre application.</span><span class="sxs-lookup"><span data-stu-id="d6764-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="d6764-129">Votre application doit utiliser la \_ constante WMDRMDEVICEAPP use \_ wpd \_ Device \_ PTR pour le paramètre *IWMDMDevice* \* .</span><span class="sxs-lookup"><span data-stu-id="d6764-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="d6764-130">L’extrait de code suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="d6764-130">The following code snippet demonstrates this.</span></span>


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



<span data-ttu-id="d6764-131">Les mêmes prérequis avec la clé privée et le certificat de l’application s’appliquent également ici.</span><span class="sxs-lookup"><span data-stu-id="d6764-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="d6764-132">Si la clé/le certificat n’est pas valide ou si l’initialisation du système WMDRM échoue, l’appel **QueryInferface** échoue.</span><span class="sxs-lookup"><span data-stu-id="d6764-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="d6764-133">La méthode ci-dessus pour acquérir l’interface **IWMDRMDeviceApp** à partir du pointeur **IStream** n’est utile que si votre application effectue déjà un transfert de contenu protégé préalablement, avant de continuer à effectuer des opérations de contrôle et de synchronisation des licences.</span><span class="sxs-lookup"><span data-stu-id="d6764-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="d6764-134">Notre recommandation pour la plupart des applications qui ont besoin d’accéder à **IWMDRMDeviceApp** consiste à initialiser **IWMDRMDeviceApp** directement, car cela ne nécessite pas que votre application transfère le contenu protégé ou conserve les interfaces de transfert pour effectuer la synchronisation des appareils et des licences. Cette méthode nécessite l’utilisation des API Windows Media Gestionnaire de périphériques (WMDM).</span><span class="sxs-lookup"><span data-stu-id="d6764-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="d6764-135">Pour plus d’informations et pour obtenir des exemples de code, consultez le livre blanc [accès aux API WMDRM à partir d’une application wpd](../windows-portable-devices.md) sur le site WHDC.</span><span class="sxs-lookup"><span data-stu-id="d6764-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6764-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6764-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6764-137">**Appareils mobiles Windows**</span><span class="sxs-lookup"><span data-stu-id="d6764-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
