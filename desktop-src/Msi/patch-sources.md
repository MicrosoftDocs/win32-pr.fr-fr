---
description: La propriété sources énumère toutes les sources de l’instance du correctif. Cette propriété appelle MsiSourceListEnumSources et retourne un tableau de chaînes et accepte le type de source comme argument.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Propriété patch. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532970"
---
# <a name="patchsources-property"></a><span data-ttu-id="a8ae0-104">Propriété patch. sources</span><span class="sxs-lookup"><span data-stu-id="a8ae0-104">Patch.Sources property</span></span>

<span data-ttu-id="a8ae0-105">La propriété **sources** énumère toutes les sources de l’instance du correctif.</span><span class="sxs-lookup"><span data-stu-id="a8ae0-105">The **Sources** property enumerates all the sources for the patch instance.</span></span> <span data-ttu-id="a8ae0-106">Cette propriété appelle [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) et retourne un tableau de chaînes et accepte le type de source comme argument.</span><span class="sxs-lookup"><span data-stu-id="a8ae0-106">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns an array of strings, and accepts the source type as argument.</span></span>

<span data-ttu-id="a8ae0-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a8ae0-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ae0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8ae0-108">Syntax</span></span>


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a><span data-ttu-id="a8ae0-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a8ae0-109">Property value</span></span>

<span data-ttu-id="a8ae0-110">Type de source à énumérer.</span><span class="sxs-lookup"><span data-stu-id="a8ae0-110">The type of source to enumerate.</span></span> <span data-ttu-id="a8ae0-111">La valeur peut être *msiInstallSourceTypeNetwork* (1) ou *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="a8ae0-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ae0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8ae0-112">Requirements</span></span>



| <span data-ttu-id="a8ae0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8ae0-113">Requirement</span></span> | <span data-ttu-id="a8ae0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8ae0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ae0-115">Version</span><span class="sxs-lookup"><span data-stu-id="a8ae0-115">Version</span></span><br/> | <span data-ttu-id="a8ae0-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8ae0-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8ae0-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8ae0-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8ae0-118">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8ae0-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a8ae0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a8ae0-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8ae0-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8ae0-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a8ae0-121">IID</span><span class="sxs-lookup"><span data-stu-id="a8ae0-121">IID</span></span><br/>     | <span data-ttu-id="a8ae0-122">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a8ae0-122">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a8ae0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8ae0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ae0-124">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="a8ae0-124">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="a8ae0-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="a8ae0-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="a8ae0-126">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="a8ae0-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




