---
description: La propriété PatchProperty obtient des informations sur un correctif spécifique appliqué à une instance spécifique du produit. Cette propriété appelle MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Méthode patch. PatchProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528861"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="5d3a9-104">Méthode patch. PatchProperty</span><span class="sxs-lookup"><span data-stu-id="5d3a9-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="5d3a9-105">La propriété **PatchProperty** obtient des informations sur un correctif spécifique appliqué à une instance spécifique du produit.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="5d3a9-106">Cette propriété appelle [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="5d3a9-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3a9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d3a9-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="5d3a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d3a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d3a9-109">*szProperty*</span><span class="sxs-lookup"><span data-stu-id="5d3a9-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="5d3a9-110">Le paramètre *szProperty* peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="5d3a9-111">Nom</span><span class="sxs-lookup"><span data-stu-id="5d3a9-111">Name</span></span>          | <span data-ttu-id="5d3a9-112">Signification</span><span class="sxs-lookup"><span data-stu-id="5d3a9-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3a9-113">LocalPackage</span><span class="sxs-lookup"><span data-stu-id="5d3a9-113">LocalPackage</span></span>  | <span data-ttu-id="5d3a9-114">Obtient le fichier correctif mis en cache utilisé par le produit.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5d3a9-115">Transformations</span><span class="sxs-lookup"><span data-stu-id="5d3a9-115">Transforms</span></span>    | <span data-ttu-id="5d3a9-116">Obtient l’ensemble des transformations de correctifs appliquées au produit par la dernière installation de correctif logiciel.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="5d3a9-117">Cette valeur peut ne pas être disponible pour les applications non gérées par utilisateur si l’utilisateur n’est pas connecté à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="5d3a9-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="5d3a9-118">InstallDate</span></span>   | <span data-ttu-id="5d3a9-119">Obtient la date à laquelle le correctif a été appliqué au produit.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5d3a9-120">Non installables</span><span class="sxs-lookup"><span data-stu-id="5d3a9-120">Uninstallable</span></span> | <span data-ttu-id="5d3a9-121">Retourne « 1 » si le correctif est marqué comme possible pour la désinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="5d3a9-122">Dans ce cas, le programme d’installation peut toujours bloquer la désinstallation si ce correctif est requis par un autre correctif qui ne peut pas être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="5d3a9-123">State</span><span class="sxs-lookup"><span data-stu-id="5d3a9-123">State</span></span>         | <span data-ttu-id="5d3a9-124">Retourne « 1 » si ce correctif est actuellement appliqué au produit.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="5d3a9-125">Retourne « 2 » si ce correctif logiciel a été remplacé par un autre correctif.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="5d3a9-126">Retourne « 4 » si ce correctif a été rendu obsolète par un autre correctif.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="5d3a9-127">Ces valeurs correspondent aux constantes utilisées par le paramètre *dwFilter* de [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="5d3a9-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="5d3a9-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d3a9-128">DisplayName</span></span>   | <span data-ttu-id="5d3a9-129">Obtient le nom complet inscrit pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="5d3a9-130">Pour les correctifs qui n’incluent pas la propriété DisplayName dans la table [MsiPatchMetadata](msipatchmetadata-table.md) , le nom complet retourné est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="5d3a9-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="5d3a9-131">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="5d3a9-131">MoreInfoURL</span></span>   | <span data-ttu-id="5d3a9-132">Obtenir l’URL des informations de support inscrites pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="5d3a9-133">Pour les correctifs qui n’incluent pas la propriété MoreInfoURL dans la table [MsiPatchMetadata](msipatchmetadata-table.md) , l’URL des informations de prise en charge retournées est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="5d3a9-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d3a9-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d3a9-134">Return value</span></span>

<span data-ttu-id="5d3a9-135">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d3a9-136">Notes</span><span class="sxs-lookup"><span data-stu-id="5d3a9-136">Remarks</span></span>

<span data-ttu-id="5d3a9-137">Cette méthode peut retourner \_ une erreur Unknown \_ patch, si l’objet [**patch**](patch-object.md) est initialisé avec une chaîne vide pour *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d3a9-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d3a9-138">Requirements</span></span>



| <span data-ttu-id="5d3a9-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d3a9-139">Requirement</span></span> | <span data-ttu-id="5d3a9-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d3a9-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3a9-141">Version</span><span class="sxs-lookup"><span data-stu-id="5d3a9-141">Version</span></span><br/> | <span data-ttu-id="5d3a9-142">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d3a9-143">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d3a9-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d3a9-144">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5d3a9-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5d3a9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5d3a9-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d3a9-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d3a9-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5d3a9-147">IID</span><span class="sxs-lookup"><span data-stu-id="5d3a9-147">IID</span></span><br/>     | <span data-ttu-id="5d3a9-148">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d3a9-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="5d3a9-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d3a9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d3a9-150">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="5d3a9-151">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="5d3a9-152">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="5d3a9-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="5d3a9-153">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5d3a9-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




