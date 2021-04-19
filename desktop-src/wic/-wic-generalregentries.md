---
description: Entrées de Registre générales
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Entrées de Registre générales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529293"
---
# <a name="general-registry-entries"></a><span data-ttu-id="b7510-103">Entrées de Registre générales</span><span class="sxs-lookup"><span data-stu-id="b7510-103">General Registry Entries</span></span>


<span data-ttu-id="b7510-104">Les entrées de Registre suivantes doivent être effectuées séparément pour le décodeur et l’encodeur :</span><span class="sxs-lookup"><span data-stu-id="b7510-104">The following registry entries must be made separately for both the decoder and the encoder:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

<span data-ttu-id="b7510-105">Les entrées FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions et formats sont requises.</span><span class="sxs-lookup"><span data-stu-id="b7510-105">The FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions, and Formats entries are required.</span></span> <span data-ttu-id="b7510-106">Toutes les autres sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="b7510-106">All of the others are optional.</span></span>

<span data-ttu-id="b7510-107">Notez que les entrées DeviceManufacturer et DeviceModels sont spécifiques aux codecs bruts et font référence au fabricant de l’appareil photo et aux modèles d’appareil photo auxquels le codec est applicable.</span><span class="sxs-lookup"><span data-stu-id="b7510-107">Note that the DeviceManufacturer and DeviceModels entries are specific to raw codecs and refer to the camera manufacturer and camera models that the codec is applicable to.</span></span> <span data-ttu-id="b7510-108">La version spec est la version de la spécification de format d’image avec laquelle le codec est conforme.</span><span class="sxs-lookup"><span data-stu-id="b7510-108">The spec version is the version of the image format specification with which the codec complies.</span></span> <span data-ttu-id="b7510-109">L’entrée formats spécifie les formats de pixel pris en charge par le codec.</span><span class="sxs-lookup"><span data-stu-id="b7510-109">The Formats entry specifies the pixel formats supported by the codec.</span></span> <span data-ttu-id="b7510-110">Un codec peut prendre en charge plusieurs formats de pixel.</span><span class="sxs-lookup"><span data-stu-id="b7510-110">A codec may support more than one pixel format.</span></span> <span data-ttu-id="b7510-111">Dans ce cas, vous devez entrer plusieurs clés sous HKEY \_ classes \_ racine \\ CLSID \\ {encodeur/décodeur CLSID} \\ .</span><span class="sxs-lookup"><span data-stu-id="b7510-111">In that case, you would enter multiple keys under HKEY\_CLASSES\_ROOT\\CLSID\\{Encoder/Decoder CLSID}\\Formats.</span></span>

## <a name="arbitrationpriority"></a><span data-ttu-id="b7510-112">ArbitrationPriority</span><span class="sxs-lookup"><span data-stu-id="b7510-112">ArbitrationPriority</span></span>

<span data-ttu-id="b7510-113">À compter de Windows 8, ArbitrationPriority est une nouvelle entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="b7510-113">Starting in Windows 8, ArbitrationPriority is a new registry entry.</span></span> <span data-ttu-id="b7510-114">Les valeurs valides sont comprises entre 0 et 10.</span><span class="sxs-lookup"><span data-stu-id="b7510-114">Valid values are 0 through 10.</span></span> <span data-ttu-id="b7510-115">Lorsque la clé ArbitrationPriority est présente, la valeur de cette clé indique au WIC de définir la priorité du codec associé derrière tous les autres codecs ayant une valeur ArbitrationPriority inférieure.</span><span class="sxs-lookup"><span data-stu-id="b7510-115">When the ArbitrationPriority key is present, the value of this key will instruct WIC to prioritize the associated codec behind any other codecs with a lower ArbitrationPriority value.</span></span> <span data-ttu-id="b7510-116">Cette évaluation se produit avant l’arbitrage du codec WIC existant et garantit que le codec associé est classé en dessous d’un codec concurrent, même s’il est plus ou moins puissant.</span><span class="sxs-lookup"><span data-stu-id="b7510-116">This evaluation occurs before the existing WIC codec arbitration occurs, and ensures the associated codec is prioritized below any competing codec, even if it is as or more capable.</span></span> <span data-ttu-id="b7510-117">Tout codec qui n’a pas de valeur ArbitrationPriority explicite définie dans le registre aura par défaut la priorité 0.</span><span class="sxs-lookup"><span data-stu-id="b7510-117">Any codec that doesn’t have an explicit ArbitrationPriority value defined in the registry will default to Priority 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7510-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7510-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b7510-119">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b7510-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b7510-120">Installation et inscription du CODEC</span><span class="sxs-lookup"><span data-stu-id="b7510-120">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="b7510-121">Entrées de Registre spécifiques à l’encodeur</span><span class="sxs-lookup"><span data-stu-id="b7510-121">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="b7510-122">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b7510-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="b7510-123">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="b7510-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b7510-124">**Fonctionnement du composant Windows Imaging : détection et arbitrage des codecs**</span><span class="sxs-lookup"><span data-stu-id="b7510-124">**How the Windows Imaging Component Works: Codec Discovery and Arbitration**</span></span>](-wic-howwicworks.md)
</dt> </dl>

 

 



