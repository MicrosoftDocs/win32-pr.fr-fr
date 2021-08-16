---
description: comment accéder aux informations SMBIOS (System Management BIOS) à partir d’une application Windows universelle.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: accéder aux informations SMBIOS à partir d’une application de Windows universel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936d30a653059b3573e962b2e52770aa2bd000180ee0612c1855de3d6a1a9778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764953"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>accéder aux informations SMBIOS à partir d’une application de Windows universel

> OBSERVE Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.

comment accéder aux informations SMBIOS (System Management BIOS) à partir d’une application Windows universelle.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>accéder aux informations SMBIOS à partir d’une application plateforme Windows universelle

à compter de Windows 10, la version 1803, les applications universelles Windows peuvent utiliser [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) et [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) pour accéder aux informations smbios en déclarant la fonctionnalité restreinte **smbios** dans le manifeste de l’application.

> [!IMPORTANT]
> seul l’accès aux tables du microprogramme SMBIOS brut (RSMB) est pris en charge à partir d’une application Windows universelle. **Accès \_ le refus** est retourné si vous essayez d’accéder à d’autres types de table de microprogramme à partir d’une application de Windows universelle.

 

Pour déclarer la fonctionnalité restreinte **SMBIOS** dans le manifeste de l’application, ajoutez l’espace de noms **ResCap** et la fonction **SMBIOS** comme suit :

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités spéciales et restreintes](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[accéder aux variables de microprogramme UEFI à partir d’une application Windows universelle](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
