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
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="20aa0-103">Accéder aux informations SMBIOS à partir d’une application Windows universelle</span><span class="sxs-lookup"><span data-stu-id="20aa0-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="20aa0-104">OBSERVE Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="20aa0-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="20aa0-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="20aa0-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="20aa0-106">Comment accéder aux informations SMBIOS (System Management BIOS) à partir d’une application Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="20aa0-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="20aa0-107">Accéder aux informations SMBIOS à partir d’une application plateforme Windows universelle</span><span class="sxs-lookup"><span data-stu-id="20aa0-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="20aa0-108">À compter de Windows 10, version 1803, les applications Windows universelles peuvent utiliser [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) et [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) pour accéder aux informations SMBIOS en déclarant la fonctionnalité restreinte **SMBIOS** dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="20aa0-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20aa0-109">Seul l’accès aux tables du microprogramme SMBIOS brut (RSMB) est pris en charge à partir d’une application Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="20aa0-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="20aa0-110">**Accès \_ Le refus** est retourné si vous essayez d’accéder à d’autres types de table de microprogramme à partir d’une application Windows universelle.</span><span class="sxs-lookup"><span data-stu-id="20aa0-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="20aa0-111">Pour déclarer la fonctionnalité restreinte **SMBIOS** dans le manifeste de l’application, ajoutez l’espace de noms **ResCap** et la fonction **SMBIOS** comme suit :</span><span class="sxs-lookup"><span data-stu-id="20aa0-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="20aa0-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20aa0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20aa0-113">Fonctionnalités spéciales et restreintes</span><span class="sxs-lookup"><span data-stu-id="20aa0-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="20aa0-114">GetSystemFirmwareTable</span><span class="sxs-lookup"><span data-stu-id="20aa0-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="20aa0-115">EnumSystemFirmwareTables</span><span class="sxs-lookup"><span data-stu-id="20aa0-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="20aa0-116">Accéder aux variables de microprogramme UEFI à partir d’une application Windows universelle</span><span class="sxs-lookup"><span data-stu-id="20aa0-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
