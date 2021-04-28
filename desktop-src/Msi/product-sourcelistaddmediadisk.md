---
description: 'Méthode Product. SourceListAddMediaDisk : la méthode SourceListAddMediaDisk ajoute un disque à l’ensemble des disques inscrits. Accepte les VolumeLabel et les DiskPrompt en tant que paramètres. Cette méthode appelle sur MsiSourceListAddMediaDisk.'
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Méthode Product. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113577"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="e10f3-105">Méthode Product. SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="e10f3-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="e10f3-106">La méthode **SourceListAddMediaDisk** ajoute un disque à l’ensemble des disques inscrits.</span><span class="sxs-lookup"><span data-stu-id="e10f3-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="e10f3-107">Accepte *les* *VolumeLabel* et les *DiskPrompt* en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="e10f3-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="e10f3-108">Cette méthode appelle sur [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="e10f3-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="e10f3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e10f3-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="e10f3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e10f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10f3-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="e10f3-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="e10f3-112">Ce paramètre fournit l’ID du disque en cours d’ajout ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e10f3-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="e10f3-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="e10f3-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="e10f3-114">Ce paramètre fournit l’étiquette du disque en cours d’ajout ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e10f3-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="e10f3-115">Une mise à jour remplace l’étiquette de volume existante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e10f3-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="e10f3-116">Pour modifier l’invite du disque uniquement, récupérez le nom du volume inscrit existant et fournissez-le avec l’invite du nouveau disque.</span><span class="sxs-lookup"><span data-stu-id="e10f3-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="e10f3-117">Une chaîne vide pour ce paramètre inscrit une chaîne vide (longueur de 0 octets) comme nom de volume.</span><span class="sxs-lookup"><span data-stu-id="e10f3-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="e10f3-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="e10f3-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="e10f3-119">Ce paramètre indique l’invite de disque du disque en cours d’ajout ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e10f3-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="e10f3-120">Une mise à jour remplace l’invite de disque existante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="e10f3-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="e10f3-121">Pour modifier le nom de volume uniquement, récupérez l’invite de disque existante à partir du Registre et fournissez-lui le nouveau nom de volume.</span><span class="sxs-lookup"><span data-stu-id="e10f3-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="e10f3-122">Une chaîne vide pour ce paramètre inscrit une chaîne vide (longueur de 0 octets) comme invite de disque.</span><span class="sxs-lookup"><span data-stu-id="e10f3-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10f3-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e10f3-123">Return value</span></span>

<span data-ttu-id="e10f3-124">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e10f3-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10f3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e10f3-125">Requirements</span></span>



| <span data-ttu-id="e10f3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e10f3-126">Requirement</span></span> | <span data-ttu-id="e10f3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e10f3-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10f3-128">Version</span><span class="sxs-lookup"><span data-stu-id="e10f3-128">Version</span></span><br/> | <span data-ttu-id="e10f3-129">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e10f3-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e10f3-130">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e10f3-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e10f3-131">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e10f3-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e10f3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e10f3-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="e10f3-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e10f3-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e10f3-134">IID</span><span class="sxs-lookup"><span data-stu-id="e10f3-134">IID</span></span><br/>     | <span data-ttu-id="e10f3-135">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e10f3-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="e10f3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e10f3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10f3-137">**Production**</span><span class="sxs-lookup"><span data-stu-id="e10f3-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="e10f3-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e10f3-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="e10f3-139">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e10f3-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




