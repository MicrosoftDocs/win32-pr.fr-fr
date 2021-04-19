---
description: La propriété SourceListInfo de l’objet Product obtient et définit les propriétés d’informations relatives à la source d’un produit. Cette propriété appelle MsiSourceListGetInfo ou MsiSourceListSetInfo. Il s’agit d’une propriété de lecture ou d’écriture.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Propriété Product. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525553"
---
# <a name="productsourcelistinfo-property"></a><span data-ttu-id="ca878-105">Propriété Product. SourceListInfo</span><span class="sxs-lookup"><span data-stu-id="ca878-105">Product.SourceListInfo property</span></span>

<span data-ttu-id="ca878-106">La propriété **SourceListInfo** de l’objet [**Product**](product-object.md) obtient et définit les propriétés d’informations relatives à la source d’un produit.</span><span class="sxs-lookup"><span data-stu-id="ca878-106">The **SourceListInfo** property of the [**Product**](product-object.md) object gets and sets the source information properties for a product.</span></span> <span data-ttu-id="ca878-107">Cette propriété appelle [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="ca878-107">This property calls [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="ca878-108">Il s’agit d’une propriété de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="ca878-108">This is a read or write property.</span></span>

<span data-ttu-id="ca878-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ca878-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca878-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca878-110">Syntax</span></span>


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="ca878-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ca878-111">Property value</span></span>

<span data-ttu-id="ca878-112">Nom des propriétés d’informations sources d’un produit à interroger ou définir.</span><span class="sxs-lookup"><span data-stu-id="ca878-112">The name of the source information properties for a product to query or set.</span></span> <span data-ttu-id="ca878-113">Pour connaître les valeurs possibles, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ca878-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca878-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ca878-114">Remarks</span></span>

<span data-ttu-id="ca878-115">Toutes les propriétés qui peuvent être récupérées ne peuvent pas être définies.</span><span class="sxs-lookup"><span data-stu-id="ca878-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="ca878-116">Le paramètre *szProperty* peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca878-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="ca878-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="ca878-117">Property</span></span>         | <span data-ttu-id="ca878-118">Pouvez-vous définir ?</span><span class="sxs-lookup"><span data-stu-id="ca878-118">Can set?</span></span> | <span data-ttu-id="ca878-119">Signification</span><span class="sxs-lookup"><span data-stu-id="ca878-119">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca878-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="ca878-120">MediaPackagePath</span></span> | <span data-ttu-id="ca878-121">O</span><span class="sxs-lookup"><span data-stu-id="ca878-121">Y</span></span>        | <span data-ttu-id="ca878-122">Chemin d’accès relatif à la racine du support d’installation.</span><span class="sxs-lookup"><span data-stu-id="ca878-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="ca878-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="ca878-123">DiskPrompt</span></span>       | <span data-ttu-id="ca878-124">O</span><span class="sxs-lookup"><span data-stu-id="ca878-124">Y</span></span>        | <span data-ttu-id="ca878-125">Modèle d’invite utilisé pour inviter l’utilisateur à fournir un support d’installation.</span><span class="sxs-lookup"><span data-stu-id="ca878-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="ca878-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="ca878-126">LastUsedSource</span></span>   | <span data-ttu-id="ca878-127">O</span><span class="sxs-lookup"><span data-stu-id="ca878-127">Y</span></span>        | <span data-ttu-id="ca878-128">Emplacement source utilisé le plus récemment pour le produit.</span><span class="sxs-lookup"><span data-stu-id="ca878-128">The most recently used source location for the product.</span></span> <span data-ttu-id="ca878-129">Lorsque vous définissez cette propriété, faites précéder l’emplacement source de « n ; » pour une source réseau ou « u ; » pour le type d’URL.</span><span class="sxs-lookup"><span data-stu-id="ca878-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="ca878-130">Par exemple, «n ; \\ \\ Scratch \\ éraflures \\ » et « u ; https://MyServer/MyFolder/MySource ».</span><span class="sxs-lookup"><span data-stu-id="ca878-130">For example, "n;\\\\scratch\\scratch\\MySource" and "u;https://MyServer/MyFolder/MySource".</span></span> |
| <span data-ttu-id="ca878-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="ca878-131">LastUsedType</span></span>     | <span data-ttu-id="ca878-132">N</span><span class="sxs-lookup"><span data-stu-id="ca878-132">N</span></span>        | <span data-ttu-id="ca878-133">« n » si la dernière source utilisée est un emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="ca878-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="ca878-134">« u » si la dernière source utilisée était un emplacement d’URL.</span><span class="sxs-lookup"><span data-stu-id="ca878-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="ca878-135">« m » si la dernière source utilisée était un média.</span><span class="sxs-lookup"><span data-stu-id="ca878-135">"m" if the last used source was media.</span></span> <span data-ttu-id="ca878-136">Chaîne vide ("") s’il n’existe aucune dernière source utilisée.</span><span class="sxs-lookup"><span data-stu-id="ca878-136">Empty string ("") if there is no last used source.</span></span>                                                                   |
| <span data-ttu-id="ca878-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="ca878-137">PackageName</span></span>      | <span data-ttu-id="ca878-138">O</span><span class="sxs-lookup"><span data-stu-id="ca878-138">Y</span></span>        | <span data-ttu-id="ca878-139">Nom du package de Windows Installer ou du package correctif sur la source.</span><span class="sxs-lookup"><span data-stu-id="ca878-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="ca878-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca878-140">Requirements</span></span>



| <span data-ttu-id="ca878-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca878-141">Requirement</span></span> | <span data-ttu-id="ca878-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca878-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca878-143">Version</span><span class="sxs-lookup"><span data-stu-id="ca878-143">Version</span></span><br/> | <span data-ttu-id="ca878-144">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca878-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca878-145">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca878-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca878-146">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ca878-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ca878-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ca878-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca878-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca878-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ca878-149">IID</span><span class="sxs-lookup"><span data-stu-id="ca878-149">IID</span></span><br/>     | <span data-ttu-id="ca878-150">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ca878-150">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="ca878-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca878-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca878-152">**Production**</span><span class="sxs-lookup"><span data-stu-id="ca878-152">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="ca878-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="ca878-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="ca878-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="ca878-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="ca878-155">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="ca878-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




