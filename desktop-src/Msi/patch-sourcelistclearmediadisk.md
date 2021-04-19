---
description: La méthode SourceListClearMediaDisk de l’objet patch supprime un disque spécifié de l’ensemble des disques inscrits pour un correctif. Accepte le dédérapageur en tant que paramètre. Cette méthode appelle MsiSourceListClearMediaDisk.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Méthode patch. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537404"
---
# <a name="patchsourcelistclearmediadisk-method"></a><span data-ttu-id="e8bd0-105">Méthode patch. SourceListClearMediaDisk</span><span class="sxs-lookup"><span data-stu-id="e8bd0-105">Patch.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="e8bd0-106">La méthode **SourceListClearMediaDisk** de l’objet [**patch**](patch-object.md) supprime un disque spécifié de l’ensemble des disques inscrits pour un correctif.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-106">The **SourceListClearMediaDisk** method of the [**Patch**](patch-object.md) object removes a specified disk from the set of registered disks for a patch.</span></span> <span data-ttu-id="e8bd0-107">Accepte le *dédérapageur* en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="e8bd0-108">Cette méthode appelle [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span><span class="sxs-lookup"><span data-stu-id="e8bd0-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bd0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8bd0-109">Syntax</span></span>


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="e8bd0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8bd0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8bd0-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="e8bd0-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="e8bd0-112">Ce paramètre fournit l’ID du disque à supprimer.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8bd0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8bd0-113">Return value</span></span>

<span data-ttu-id="e8bd0-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bd0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8bd0-115">Requirements</span></span>



| <span data-ttu-id="e8bd0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8bd0-116">Requirement</span></span> | <span data-ttu-id="e8bd0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8bd0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bd0-118">Version</span><span class="sxs-lookup"><span data-stu-id="e8bd0-118">Version</span></span><br/> | <span data-ttu-id="e8bd0-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8bd0-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8bd0-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e8bd0-121">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e8bd0-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e8bd0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bd0-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e8bd0-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bd0-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e8bd0-124">IID</span><span class="sxs-lookup"><span data-stu-id="e8bd0-124">IID</span></span><br/>     | <span data-ttu-id="e8bd0-125">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e8bd0-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="e8bd0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8bd0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bd0-127">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="e8bd0-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="e8bd0-128">**MsiSourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e8bd0-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="e8bd0-129">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e8bd0-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




