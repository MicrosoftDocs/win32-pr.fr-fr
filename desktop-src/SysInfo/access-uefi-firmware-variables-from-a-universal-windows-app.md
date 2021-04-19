---
description: Comment accéder aux variables du microprogramme Unified Extensible Firmware Interface (UEFI) à partir d’une application Windows universelle.
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: Accéder aux variables de microprogramme UEFI à partir d’une application Windows universelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531987"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="e938c-103">Accéder aux variables de microprogramme UEFI à partir d’une application Windows universelle</span><span class="sxs-lookup"><span data-stu-id="e938c-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="e938c-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e938c-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e938c-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e938c-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e938c-106">Comment accéder aux variables du microprogramme Unified Extensible Firmware Interface (UEFI) à partir d’une application Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="e938c-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="e938c-107">À compter de Windows 10, version 1803, les applications Windows universelles peuvent utiliser [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) et [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (et leurs variantes « ex ») pour accéder aux variables de microprogramme UEFI en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="e938c-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="e938c-108">Déclarez la fonctionnalité personnalisée **\_ Cw5n1h2txyewy de Microsoft. firmwareRead** dans le manifeste pour lire une variable de microprogramme, et/ou la fonction **Microsoft. firmwareWrite \_ cw5n1h2txyewy** pour écrire une variable de microprogramme.</span><span class="sxs-lookup"><span data-stu-id="e938c-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="e938c-109">Déclarez également la fonctionnalité restreinte **protectedApp** dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="e938c-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="e938c-110">Par exemple, les ajouts du manifeste de l’application suivants permettent à l’application Windows universelle de lire les variables du microprogramme :</span><span class="sxs-lookup"><span data-stu-id="e938c-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="e938c-111">Définissez l’option de l’éditeur de liens **/INTEGRITYCHECK**, pour toutes les configurations de projet, avant d’envoyer l’application au Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e938c-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="e938c-112">Cela permet de s’assurer que l’application sera lancée comme une application protégée.</span><span class="sxs-lookup"><span data-stu-id="e938c-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="e938c-113">Pour plus d’informations [, consultez/INTEGRITYCHECK (exiger la vérification de la signature)](/cpp/build/reference/integritycheck-require-signature-check) .</span><span class="sxs-lookup"><span data-stu-id="e938c-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="e938c-114">Obtenez un fichier de [descripteur de capacité personnalisée](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) signé auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e938c-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="e938c-115">Consultez [création d’une fonctionnalité personnalisée pour associer un pilote à une application de prise en charge matérielle (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) et [utilisation d’une fonctionnalité personnalisée pour associer une application de support matériel (HSA) à un pilote](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) pour plus d’informations sur la façon d’obtenir un fichier SCCD signé de Microsoft, de l’empaqueter avec votre application et de l’activation du mode développeur.</span><span class="sxs-lookup"><span data-stu-id="e938c-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="e938c-116">Voici un exemple de fichier SSCD de l' [exemple CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span><span class="sxs-lookup"><span data-stu-id="e938c-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="e938c-117">Soumettez l’application à la Microsoft Store pour la faire signer.</span><span class="sxs-lookup"><span data-stu-id="e938c-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="e938c-118">À des fins de développement, vous pouvez ignorer la signature en activant test-Signing dans la base de données de configuration de démarrage (BCD).</span><span class="sxs-lookup"><span data-stu-id="e938c-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="e938c-119">Pour plus d’informations, consultez [l’option de configuration de démarrage testsigning](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .</span><span class="sxs-lookup"><span data-stu-id="e938c-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e938c-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e938c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e938c-121">Fonctionnalités spéciales et restreintes</span><span class="sxs-lookup"><span data-stu-id="e938c-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="e938c-122">**GetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="e938c-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="e938c-123">**GetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="e938c-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="e938c-124">**SetFirmwareEnvironmentVariable**</span><span class="sxs-lookup"><span data-stu-id="e938c-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="e938c-125">**SetFirmwareEnvironmentVariableEx**</span><span class="sxs-lookup"><span data-stu-id="e938c-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="e938c-126">Accéder aux informations SMBIOS à partir d’une application Windows universelle</span><span class="sxs-lookup"><span data-stu-id="e938c-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
