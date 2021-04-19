---
description: La propriété MediaDisks énumère tous les disques multimédias pour cette instance de produit. Cette propriété appelle MsiSourceListEnumMediaDisks. Retourne les informations de disque sous la forme d’un tableau d’objets d’enregistrement.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Propriété Product. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528037"
---
# <a name="productmediadisks-property"></a><span data-ttu-id="f4248-105">Propriété Product. MediaDisks</span><span class="sxs-lookup"><span data-stu-id="f4248-105">Product.MediaDisks property</span></span>

<span data-ttu-id="f4248-106">La propriété **MediaDisks** énumère tous les disques multimédias pour cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="f4248-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="f4248-107">Cette propriété appelle [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="f4248-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="f4248-108">Retourne les informations de disque sous la forme d’un tableau d’objets d' [**enregistrement**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="f4248-108">Returns the disk information as an array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="f4248-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f4248-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4248-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4248-110">Syntax</span></span>


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="f4248-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f4248-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f4248-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f4248-112">Remarks</span></span>

<span data-ttu-id="f4248-113">Dans chaque enregistrement, le premier champ contient l’ID de disque, le deuxième le nom de volume et le troisième l’invite de disque inscrite pour le disque.</span><span class="sxs-lookup"><span data-stu-id="f4248-113">In each record, the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4248-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4248-114">Requirements</span></span>



| <span data-ttu-id="f4248-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4248-115">Requirement</span></span> | <span data-ttu-id="f4248-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4248-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4248-117">Version</span><span class="sxs-lookup"><span data-stu-id="f4248-117">Version</span></span><br/> | <span data-ttu-id="f4248-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f4248-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f4248-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f4248-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f4248-120">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f4248-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f4248-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f4248-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="f4248-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4248-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f4248-123">IID</span><span class="sxs-lookup"><span data-stu-id="f4248-123">IID</span></span><br/>     | <span data-ttu-id="f4248-124">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f4248-124">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="f4248-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4248-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4248-126">**Production**</span><span class="sxs-lookup"><span data-stu-id="f4248-126">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="f4248-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="f4248-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="f4248-128">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="f4248-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




