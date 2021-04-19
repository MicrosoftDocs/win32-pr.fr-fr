---
description: L’objet patch représente une instance unique d’un correctif qui a été inscrit ou appliqué. L’objet peut être instancié avec la propriété patch comme &\# 0034 ; WindowsInstaller. installer. patch (PatchCode, ProductCode, UserSid, context) &\# 0034 ;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Objet patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528006"
---
# <a name="patch-object"></a><span data-ttu-id="e89dd-103">Objet patch</span><span class="sxs-lookup"><span data-stu-id="e89dd-103">Patch object</span></span>

<span data-ttu-id="e89dd-104">L’objet **patch** représente une instance unique d’un correctif qui a été inscrit ou appliqué.</span><span class="sxs-lookup"><span data-stu-id="e89dd-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="e89dd-105">L’objet peut être instancié avec la propriété **patch** comme « windowsinstaller. installer. patch (*PatchCode*, *ProductCode*, *UserSid*, *Context*) ».</span><span class="sxs-lookup"><span data-stu-id="e89dd-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="e89dd-106">Pour un contexte d’ordinateur, le paramètre *UserSid* doit être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="e89dd-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="e89dd-107">La valeur *ProductCode* peut être définie sur une chaîne vide pour les correctifs qui sont inscrits uniquement et qui ne sont pas encore appliqués à un produit.</span><span class="sxs-lookup"><span data-stu-id="e89dd-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="e89dd-108">La valeur *ProductCode* peut être définie sur une chaîne vide lors de la lecture ou de la mise à jour des informations de liste source d’un correctif.</span><span class="sxs-lookup"><span data-stu-id="e89dd-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="e89dd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e89dd-109">Members</span></span>

<span data-ttu-id="e89dd-110">L’objet **patch** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e89dd-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="e89dd-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e89dd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e89dd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e89dd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e89dd-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e89dd-113">Methods</span></span>

<span data-ttu-id="e89dd-114">L’objet **patch** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e89dd-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="e89dd-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e89dd-115">Method</span></span>                                                               | <span data-ttu-id="e89dd-116">Description</span><span class="sxs-lookup"><span data-stu-id="e89dd-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e89dd-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e89dd-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="e89dd-118">Ajoutez un disque à l’ensemble de disques inscrits.</span><span class="sxs-lookup"><span data-stu-id="e89dd-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="e89dd-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="e89dd-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="e89dd-120">Ajoutez une source réseau ou URL à la liste source.</span><span class="sxs-lookup"><span data-stu-id="e89dd-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="e89dd-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="e89dd-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="e89dd-122">Efface la liste source complète du type spécifié de sources.</span><span class="sxs-lookup"><span data-stu-id="e89dd-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="e89dd-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e89dd-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="e89dd-124">Supprimer un disque de l’ensemble de disques inscrits de la liste source.</span><span class="sxs-lookup"><span data-stu-id="e89dd-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="e89dd-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="e89dd-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="e89dd-126">Supprimer une source de réseau ou d’URL de la liste source.</span><span class="sxs-lookup"><span data-stu-id="e89dd-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="e89dd-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="e89dd-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="e89dd-128">Efface la dernière source utilisée de la liste source.</span><span class="sxs-lookup"><span data-stu-id="e89dd-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="e89dd-129">Cela force une résolution de liste source la prochaine fois que la source est requise.</span><span class="sxs-lookup"><span data-stu-id="e89dd-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e89dd-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e89dd-130">Properties</span></span>

<span data-ttu-id="e89dd-131">L’objet **patch** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e89dd-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="e89dd-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="e89dd-132">Property</span></span>                                                  | <span data-ttu-id="e89dd-133">Description</span><span class="sxs-lookup"><span data-stu-id="e89dd-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e89dd-134">**Context**</span><span class="sxs-lookup"><span data-stu-id="e89dd-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="e89dd-135">Le contexte de cette instance de patch est une valeur MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="e89dd-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="e89dd-136">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="e89dd-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="e89dd-137">Énumère tous les disques multimédias pour cette instance de correctif.</span><span class="sxs-lookup"><span data-stu-id="e89dd-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="e89dd-138">**PatchCode**</span><span class="sxs-lookup"><span data-stu-id="e89dd-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="e89dd-139">Retourne le code du correctif.</span><span class="sxs-lookup"><span data-stu-id="e89dd-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="e89dd-140">**PatchProperty**</span><span class="sxs-lookup"><span data-stu-id="e89dd-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="e89dd-141">Obtient des informations de propriété sur un correctif spécifique appliqué à une instance spécifique du produit.</span><span class="sxs-lookup"><span data-stu-id="e89dd-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="e89dd-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="e89dd-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="e89dd-143">Retourne le code du produit.</span><span class="sxs-lookup"><span data-stu-id="e89dd-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="e89dd-144">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="e89dd-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="e89dd-145">Obtient et définit les propriétés des informations sur la source.</span><span class="sxs-lookup"><span data-stu-id="e89dd-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="e89dd-146">Il s’agit d’une propriété de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="e89dd-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="e89dd-147">**Sources**</span><span class="sxs-lookup"><span data-stu-id="e89dd-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="e89dd-148">Énumère toutes les sources pour cette instance du correctif.</span><span class="sxs-lookup"><span data-stu-id="e89dd-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="e89dd-149">**State**</span><span class="sxs-lookup"><span data-stu-id="e89dd-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="e89dd-150">État d’installation du correctif.</span><span class="sxs-lookup"><span data-stu-id="e89dd-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="e89dd-151">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="e89dd-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="e89dd-152">Retourne le SID de l’utilisateur, sous le compte pour lequel cette instance de correctif est disponible.</span><span class="sxs-lookup"><span data-stu-id="e89dd-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="e89dd-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e89dd-153">Requirements</span></span>



| <span data-ttu-id="e89dd-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e89dd-154">Requirement</span></span> | <span data-ttu-id="e89dd-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="e89dd-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e89dd-156">Version</span><span class="sxs-lookup"><span data-stu-id="e89dd-156">Version</span></span><br/> | <span data-ttu-id="e89dd-157">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e89dd-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e89dd-158">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e89dd-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e89dd-159">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e89dd-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e89dd-160">DLL</span><span class="sxs-lookup"><span data-stu-id="e89dd-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="e89dd-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e89dd-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e89dd-162">IID</span><span class="sxs-lookup"><span data-stu-id="e89dd-162">IID</span></span><br/>     | <span data-ttu-id="e89dd-163">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e89dd-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="e89dd-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e89dd-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89dd-165">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e89dd-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




