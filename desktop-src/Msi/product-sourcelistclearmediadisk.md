---
description: La méthode SourceListClearMediaDisk de l’objet Product supprime un disque spécifié de l’ensemble des disques inscrits pour un produit. Accepte le dédérapageur en tant que paramètre. Cette méthode appelle MsiSourceListClearMediaDisk.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Méthode Product. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540364"
---
# <a name="productsourcelistclearmediadisk-method"></a><span data-ttu-id="a2644-105">Méthode Product. SourceListClearMediaDisk</span><span class="sxs-lookup"><span data-stu-id="a2644-105">Product.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="a2644-106">La méthode **SourceListClearMediaDisk** de l’objet [**Product**](product-object.md) supprime un disque spécifié de l’ensemble des disques inscrits pour un produit.</span><span class="sxs-lookup"><span data-stu-id="a2644-106">The **SourceListClearMediaDisk** method of the [**Product**](product-object.md) object removes a specified disk from the set of registered disks for a product.</span></span> <span data-ttu-id="a2644-107">Accepte le *dédérapageur* en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="a2644-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="a2644-108">Cette méthode appelle [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span><span class="sxs-lookup"><span data-stu-id="a2644-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2644-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2644-109">Syntax</span></span>


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="a2644-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2644-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2644-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="a2644-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="a2644-112">Ce paramètre fournit l’ID du disque à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a2644-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2644-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2644-113">Return value</span></span>

<span data-ttu-id="a2644-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a2644-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2644-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2644-115">Requirements</span></span>



| <span data-ttu-id="a2644-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2644-116">Requirement</span></span> | <span data-ttu-id="a2644-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2644-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2644-118">Version</span><span class="sxs-lookup"><span data-stu-id="a2644-118">Version</span></span><br/> | <span data-ttu-id="a2644-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a2644-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a2644-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2644-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a2644-121">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a2644-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a2644-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a2644-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="a2644-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2644-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a2644-124">IID</span><span class="sxs-lookup"><span data-stu-id="a2644-124">IID</span></span><br/>     | <span data-ttu-id="a2644-125">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a2644-125">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="a2644-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2644-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2644-127">**Production**</span><span class="sxs-lookup"><span data-stu-id="a2644-127">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="a2644-128">**MsiSourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="a2644-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="a2644-129">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="a2644-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




