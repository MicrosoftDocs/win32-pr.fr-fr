---
description: La propriété PatchesEx retourne un objet RecordList qui énumère la liste des correctifs.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Installer. PatchesEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539200"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="48d54-103">Installer. PatchesEx, propriété</span><span class="sxs-lookup"><span data-stu-id="48d54-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="48d54-104">La propriété **PatchesEx** retourne un objet [**RecordList**](recordlist-object.md) qui énumère la liste des correctifs.</span><span class="sxs-lookup"><span data-stu-id="48d54-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="48d54-105">Cette propriété appelle [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="48d54-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="48d54-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="48d54-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d54-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48d54-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="48d54-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="48d54-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="48d54-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48d54-109">Requirements</span></span>



| <span data-ttu-id="48d54-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48d54-110">Requirement</span></span> | <span data-ttu-id="48d54-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="48d54-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d54-112">Version</span><span class="sxs-lookup"><span data-stu-id="48d54-112">Version</span></span><br/> | <span data-ttu-id="48d54-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="48d54-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="48d54-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="48d54-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="48d54-115">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="48d54-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="48d54-116">DLL</span><span class="sxs-lookup"><span data-stu-id="48d54-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="48d54-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48d54-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="48d54-118">IID</span><span class="sxs-lookup"><span data-stu-id="48d54-118">IID</span></span><br/>     | <span data-ttu-id="48d54-119">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="48d54-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="48d54-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d54-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d54-121">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="48d54-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="48d54-122">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="48d54-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="48d54-123">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="48d54-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="48d54-124">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="48d54-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




