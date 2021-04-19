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
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a>Accéder aux variables de microprogramme UEFI à partir d’une application Windows universelle

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Comment accéder aux variables du microprogramme Unified Extensible Firmware Interface (UEFI) à partir d’une application Windows universelle.

À compter de Windows 10, version 1803, les applications Windows universelles peuvent utiliser [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) et [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (et leurs variantes « ex ») pour accéder aux variables de microprogramme UEFI en procédant comme suit :

-   Déclarez la fonctionnalité personnalisée **\_ Cw5n1h2txyewy de Microsoft. firmwareRead** dans le manifeste pour lire une variable de microprogramme, et/ou la fonction **Microsoft. firmwareWrite \_ cw5n1h2txyewy** pour écrire une variable de microprogramme.
-   Déclarez également la fonctionnalité restreinte **protectedApp** dans le manifeste de l’application.
-   Par exemple, les ajouts du manifeste de l’application suivants permettent à l’application Windows universelle de lire les variables du microprogramme :

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

-   Définissez l’option de l’éditeur de liens **/INTEGRITYCHECK**, pour toutes les configurations de projet, avant d’envoyer l’application au Microsoft Store. Cela permet de s’assurer que l’application sera lancée comme une application protégée. Pour plus d’informations [, consultez/INTEGRITYCHECK (exiger la vérification de la signature)](/cpp/build/reference/integritycheck-require-signature-check) .
-   Obtenez un fichier de [descripteur de capacité personnalisée](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) signé auprès de Microsoft. Consultez [création d’une fonctionnalité personnalisée pour associer un pilote à une application de prise en charge matérielle (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) et [utilisation d’une fonctionnalité personnalisée pour associer une application de support matériel (HSA) à un pilote](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) pour plus d’informations sur la façon d’obtenir un fichier SCCD signé de Microsoft, de l’empaqueter avec votre application et de l’activation du mode développeur. Voici un exemple de fichier SSCD de l' [exemple CustomCapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):
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

    

-   Soumettez l’application à la Microsoft Store pour la faire signer. À des fins de développement, vous pouvez ignorer la signature en activant test-Signing dans la base de données de configuration de démarrage (BCD). Pour plus d’informations, consultez [l’option de configuration de démarrage testsigning](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités spéciales et restreintes](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[**GetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[**SetFirmwareEnvironmentVariableEx**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[Accéder aux informations SMBIOS à partir d’une application Windows universelle](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
