---
description: La propriété SourceListInfo de l’objet patch obtient et définit les propriétés d’informations relatives à la source d’un correctif. Cette propriété appelle MsiSourceListGetInfo ou MsiSourceListSetInfo. Il s’agit d’une propriété de lecture ou d’écriture.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Patch. SourceListInfo, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532971"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="0bcf6-105">Patch. SourceListInfo, propriété</span><span class="sxs-lookup"><span data-stu-id="0bcf6-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="0bcf6-106">La propriété **SourceListInfo** de l’objet [**patch**](patch-object.md) obtient et définit les propriétés d’informations relatives à la source d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="0bcf6-107">Cette propriété appelle [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="0bcf6-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="0bcf6-108">Il s’agit d’une propriété de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-108">This is a read or write property.</span></span>

<span data-ttu-id="0bcf6-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcf6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bcf6-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="0bcf6-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0bcf6-111">Property value</span></span>

<span data-ttu-id="0bcf6-112">Nom des propriétés d’informations sources d’un correctif à interroger ou définir.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="0bcf6-113">Pour connaître les valeurs possibles, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcf6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0bcf6-114">Remarks</span></span>

<span data-ttu-id="0bcf6-115">Toutes les propriétés qui peuvent être récupérées ne peuvent pas être définies.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="0bcf6-116">Le paramètre *szProperty* peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="0bcf6-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="0bcf6-117">Property</span></span>         | <span data-ttu-id="0bcf6-118">Pouvez-vous définir ?</span><span class="sxs-lookup"><span data-stu-id="0bcf6-118">Can set?</span></span> | <span data-ttu-id="0bcf6-119">Signification</span><span class="sxs-lookup"><span data-stu-id="0bcf6-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcf6-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="0bcf6-120">MediaPackagePath</span></span> | <span data-ttu-id="0bcf6-121">O</span><span class="sxs-lookup"><span data-stu-id="0bcf6-121">Y</span></span>        | <span data-ttu-id="0bcf6-122">Chemin d’accès relatif à la racine du support d’installation.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0bcf6-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="0bcf6-123">DiskPrompt</span></span>       | <span data-ttu-id="0bcf6-124">O</span><span class="sxs-lookup"><span data-stu-id="0bcf6-124">Y</span></span>        | <span data-ttu-id="0bcf6-125">Modèle d’invite utilisé pour inviter l’utilisateur à fournir un support d’installation.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="0bcf6-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="0bcf6-126">LastUsedSource</span></span>   | <span data-ttu-id="0bcf6-127">O</span><span class="sxs-lookup"><span data-stu-id="0bcf6-127">Y</span></span>        | <span data-ttu-id="0bcf6-128">Emplacement source utilisé le plus récemment pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="0bcf6-129">Lorsque vous définissez cette propriété, faites précéder l’emplacement source de « n ; » pour une source réseau ou « u ; » pour le type d’URL.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="0bcf6-130">Par exemple, utilisez «n ; \\ \\ éraflure \\ Scratch \\ test» ou « u ; https://microsoft.com/Patches/Office/SP1 ».</span><span class="sxs-lookup"><span data-stu-id="0bcf6-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="0bcf6-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="0bcf6-131">LastUsedType</span></span>     | <span data-ttu-id="0bcf6-132">N</span><span class="sxs-lookup"><span data-stu-id="0bcf6-132">N</span></span>        | <span data-ttu-id="0bcf6-133">« n » si la dernière source utilisée est un emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="0bcf6-134">« u » si la dernière source utilisée était un emplacement d’URL.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="0bcf6-135">« m » si la dernière source utilisée était un média.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-135">"m" if the last used source was media.</span></span> <span data-ttu-id="0bcf6-136">Chaîne vide ("") s’il n’existe aucune dernière source utilisée.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="0bcf6-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="0bcf6-137">PackageName</span></span>      | <span data-ttu-id="0bcf6-138">O</span><span class="sxs-lookup"><span data-stu-id="0bcf6-138">Y</span></span>        | <span data-ttu-id="0bcf6-139">Nom du package de Windows Installer ou du package correctif sur la source.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="0bcf6-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bcf6-140">Requirements</span></span>



| <span data-ttu-id="0bcf6-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bcf6-141">Requirement</span></span> | <span data-ttu-id="0bcf6-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bcf6-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcf6-143">Version</span><span class="sxs-lookup"><span data-stu-id="0bcf6-143">Version</span></span><br/> | <span data-ttu-id="0bcf6-144">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0bcf6-145">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0bcf6-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0bcf6-146">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0bcf6-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0bcf6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0bcf6-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="0bcf6-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bcf6-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0bcf6-149">IID</span><span class="sxs-lookup"><span data-stu-id="0bcf6-149">IID</span></span><br/>     | <span data-ttu-id="0bcf6-150">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0bcf6-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0bcf6-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bcf6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcf6-152">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="0bcf6-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="0bcf6-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="0bcf6-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="0bcf6-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="0bcf6-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="0bcf6-155">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="0bcf6-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




