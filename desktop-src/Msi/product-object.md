---
description: L’objet Product représente une instance unique d’un produit qui est publié, installé ou inconnu. L’objet peut être instancié avec la propriété Product comme &\# 0034 ; WindowsInstaller. installer. Product (ProductCode, UserSid, contexte) &\# 0034 ;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Product, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520855"
---
# <a name="product-object"></a><span data-ttu-id="e6874-103">Product, objet</span><span class="sxs-lookup"><span data-stu-id="e6874-103">Product object</span></span>

<span data-ttu-id="e6874-104">L’objet **Product** représente une instance unique d’un produit qui est publié, installé ou inconnu.</span><span class="sxs-lookup"><span data-stu-id="e6874-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="e6874-105">L’objet peut être instancié avec la propriété **Product** comme « windowsinstaller. installer. Product (*ProductCode*, *UserSid*, *Context*) ».</span><span class="sxs-lookup"><span data-stu-id="e6874-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="e6874-106">*UserSid* doit avoir la valeur null pour le contexte par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e6874-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="e6874-107">*UserSid* peut avoir la valeur null pour l’utilisateur actuel spécifié, lorsque le contexte n’est pas par machine.</span><span class="sxs-lookup"><span data-stu-id="e6874-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="e6874-108">Les paramètres *ProductCode* et *Context* sont requis.</span><span class="sxs-lookup"><span data-stu-id="e6874-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="e6874-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e6874-109">Members</span></span>

<span data-ttu-id="e6874-110">L’objet **Product** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6874-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="e6874-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6874-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6874-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6874-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6874-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6874-113">Methods</span></span>

<span data-ttu-id="e6874-114">L’objet **Product** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e6874-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="e6874-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e6874-115">Method</span></span>                                                                 | <span data-ttu-id="e6874-116">Description</span><span class="sxs-lookup"><span data-stu-id="e6874-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6874-117">**SourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e6874-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="e6874-118">Ajoutez un disque à l’ensemble de disques inscrits.</span><span class="sxs-lookup"><span data-stu-id="e6874-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="e6874-119">**SourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="e6874-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="e6874-120">Ajoutez une source réseau ou URL à la liste source.</span><span class="sxs-lookup"><span data-stu-id="e6874-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="e6874-121">**SourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="e6874-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="e6874-122">Efface la liste source complète du type spécifié de sources.</span><span class="sxs-lookup"><span data-stu-id="e6874-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="e6874-123">**SourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e6874-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="e6874-124">Supprimer un disque de l’ensemble de disques inscrits de la liste source.</span><span class="sxs-lookup"><span data-stu-id="e6874-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="e6874-125">**SourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="e6874-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="e6874-126">Supprimer une source de réseau ou d’URL de la liste source.</span><span class="sxs-lookup"><span data-stu-id="e6874-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="e6874-127">**SourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="e6874-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="e6874-128">Efface la dernière source utilisée.</span><span class="sxs-lookup"><span data-stu-id="e6874-128">Clears the last used source.</span></span> <span data-ttu-id="e6874-129">Cela force une résolution de liste source la prochaine fois que la source est requise.</span><span class="sxs-lookup"><span data-stu-id="e6874-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6874-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6874-130">Properties</span></span>

<span data-ttu-id="e6874-131">L’objet **Product** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e6874-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="e6874-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="e6874-132">Property</span></span>                                                      | <span data-ttu-id="e6874-133">Description</span><span class="sxs-lookup"><span data-stu-id="e6874-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6874-134">**ComponentState**</span><span class="sxs-lookup"><span data-stu-id="e6874-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="e6874-135">État d’un composant spécifié pour cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="e6874-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="e6874-136">**Context**</span><span class="sxs-lookup"><span data-stu-id="e6874-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="e6874-137">Contexte de cette instance de produit en tant que valeur MSIINSTALLCONTEXT.</span><span class="sxs-lookup"><span data-stu-id="e6874-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="e6874-138">**FeatureState**</span><span class="sxs-lookup"><span data-stu-id="e6874-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="e6874-139">État d’une fonctionnalité spécifiée pour cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="e6874-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="e6874-140">**InstallProperty**</span><span class="sxs-lookup"><span data-stu-id="e6874-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="e6874-141">Valeur d’une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e6874-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="e6874-142">**MediaDisks**</span><span class="sxs-lookup"><span data-stu-id="e6874-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="e6874-143">Énumère tous les disques multimédias pour cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="e6874-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="e6874-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="e6874-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="e6874-145">Retourne le code du produit.</span><span class="sxs-lookup"><span data-stu-id="e6874-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="e6874-146">**SourceListInfo**</span><span class="sxs-lookup"><span data-stu-id="e6874-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="e6874-147">Obtient et définit les propriétés des informations sur la source.</span><span class="sxs-lookup"><span data-stu-id="e6874-147">Get and set the source information properties.</span></span> <span data-ttu-id="e6874-148">Il s’agit d’une propriété de lecture ou d’écriture.</span><span class="sxs-lookup"><span data-stu-id="e6874-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="e6874-149">**Sources**</span><span class="sxs-lookup"><span data-stu-id="e6874-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="e6874-150">Énumère toutes les sources pour cette instance de produit.</span><span class="sxs-lookup"><span data-stu-id="e6874-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="e6874-151">**State**</span><span class="sxs-lookup"><span data-stu-id="e6874-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="e6874-152">État d’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="e6874-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="e6874-153">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="e6874-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="e6874-154">Retourne le SID de l’utilisateur, sous quel compte cette instance de produit est disponible.</span><span class="sxs-lookup"><span data-stu-id="e6874-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="e6874-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6874-155">Requirements</span></span>



| <span data-ttu-id="e6874-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6874-156">Requirement</span></span> | <span data-ttu-id="e6874-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6874-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6874-158">Version</span><span class="sxs-lookup"><span data-stu-id="e6874-158">Version</span></span><br/> | <span data-ttu-id="e6874-159">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6874-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6874-160">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6874-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6874-161">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e6874-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e6874-162">DLL</span><span class="sxs-lookup"><span data-stu-id="e6874-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6874-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6874-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e6874-164">IID</span><span class="sxs-lookup"><span data-stu-id="e6874-164">IID</span></span><br/>     | <span data-ttu-id="e6874-165">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e6874-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="e6874-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6874-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6874-167">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e6874-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




