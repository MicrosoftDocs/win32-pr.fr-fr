---
description: La propriété MediaDisks énumère tous les disques multimédias pour cette instance de produit. Cette propriété appelle MsiSourceListEnumMediaDisks. Retourne les informations de disque sous la forme d’un tableau d’objets d’enregistrement.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Patch. MediaDisks, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527995"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="b82a6-105">Patch. MediaDisks, propriété</span><span class="sxs-lookup"><span data-stu-id="b82a6-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="b82a6-106">La propriété **MediaDisks** énumère tous les disques multimédias pour cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="b82a6-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="b82a6-107">Cette propriété appelle [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="b82a6-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="b82a6-108">Retourne les informations de disque sous la forme d’un tableau d’objets d' [**enregistrement**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b82a6-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="b82a6-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b82a6-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82a6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b82a6-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="b82a6-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b82a6-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b82a6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b82a6-112">Remarks</span></span>

<span data-ttu-id="b82a6-113">Dans chaque enregistrement, le premier champ contient l’ID de disque, le deuxième le nom de volume et le troisième l’invite de disque inscrite pour le disque.</span><span class="sxs-lookup"><span data-stu-id="b82a6-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82a6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b82a6-114">Requirements</span></span>



| <span data-ttu-id="b82a6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b82a6-115">Requirement</span></span> | <span data-ttu-id="b82a6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b82a6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b82a6-117">Version</span><span class="sxs-lookup"><span data-stu-id="b82a6-117">Version</span></span><br/> | <span data-ttu-id="b82a6-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b82a6-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b82a6-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b82a6-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b82a6-120">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b82a6-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b82a6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b82a6-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b82a6-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b82a6-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b82a6-123">IID</span><span class="sxs-lookup"><span data-stu-id="b82a6-123">IID</span></span><br/>     | <span data-ttu-id="b82a6-124">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b82a6-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="b82a6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b82a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82a6-126">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="b82a6-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="b82a6-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="b82a6-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="b82a6-128">**Enregistrement**</span><span class="sxs-lookup"><span data-stu-id="b82a6-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="b82a6-129">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="b82a6-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




