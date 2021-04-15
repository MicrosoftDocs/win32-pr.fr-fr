---
description: Comment accéder aux informations SMBIOS (System Management BIOS) à partir d’une application Windows universelle.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Accéder aux informations SMBIOS à partir d’une application Windows universelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529319"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Accéder aux informations SMBIOS à partir d’une application Windows universelle

> OBSERVE Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.

Comment accéder aux informations SMBIOS (System Management BIOS) à partir d’une application Windows universelle.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Accéder aux informations SMBIOS à partir d’une application plateforme Windows universelle

À compter de Windows 10, version 1803, les applications Windows universelles peuvent utiliser [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) et [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) pour accéder aux informations SMBIOS en déclarant la fonctionnalité restreinte **SMBIOS** dans le manifeste de l’application.

> [!IMPORTANT]
> Seul l’accès aux tables du microprogramme SMBIOS brut (RSMB) est pris en charge à partir d’une application Windows universelle. **Accès \_ Le refus** est retourné si vous essayez d’accéder à d’autres types de table de microprogramme à partir d’une application Windows universelle.

 

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

[Accéder aux variables de microprogramme UEFI à partir d’une application Windows universelle](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
