---
description: Pour chaque produit indiqué par le package de correctifs comme éligibles pour recevoir le correctif, la méthode ApplyPatch de l’objet installer appelle une installation et définit la propriété PATCH sur le chemin d’accès du package correctif.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer. ApplyPatch, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536002"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="68560-103">Installer. ApplyPatch, méthode</span><span class="sxs-lookup"><span data-stu-id="68560-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="68560-104">Pour chaque produit indiqué par le package de correctifs comme éligibles pour recevoir le correctif, la méthode **ApplyPatch** de l’objet [**installer**](installer-object.md) appelle une installation et définit la propriété [**patch**](patch.md) sur le chemin d’accès du package correctif.</span><span class="sxs-lookup"><span data-stu-id="68560-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="68560-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68560-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="68560-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68560-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68560-107">*PatchPackage*</span><span class="sxs-lookup"><span data-stu-id="68560-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="68560-108">Spécifie un chemin d’accès au package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="68560-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="68560-109">*InstallPackage*</span><span class="sxs-lookup"><span data-stu-id="68560-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="68560-110">Si *InstallType* a la valeur MsiInstallTypeNetworkImage, *INSTALLPACKAGE* spécifie le chemin d’accès au produit qui doit être corrigé.</span><span class="sxs-lookup"><span data-stu-id="68560-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="68560-111">Si *InstallType* a la valeur msiInstallTypeDefault et que *INSTALLPACKAGE* a la valeur 0, le programme d’installation applique le correctif à tous les produits éligibles figurant dans le package de correctifs.</span><span class="sxs-lookup"><span data-stu-id="68560-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="68560-112">Si *InstallType* est msiInstallTypeSingleInstance, le programme d’installation applique le correctif au produit spécifié par *INSTALLPACKAGE*.</span><span class="sxs-lookup"><span data-stu-id="68560-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="68560-113">Dans ce cas, les autres produits éligibles répertoriés dans le package de correctifs sont ignorés et le paramètre *INSTALLPACKAGE* contient la chaîne terminée par le caractère null qui représente le code de produit de l’instance à corriger.</span><span class="sxs-lookup"><span data-stu-id="68560-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="68560-114">Ce type d’installation requiert la version de Windows Installer fournie avec Windows Server 2003 ou version ultérieure, ou Windows Installer XP SP1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68560-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="68560-115">*InstallType (type d'installation)*</span><span class="sxs-lookup"><span data-stu-id="68560-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="68560-116">Ce paramètre spécifie le type d’installation à corriger.</span><span class="sxs-lookup"><span data-stu-id="68560-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="68560-117">Le paramètre *InstallType* est ignoré si *INSTALLPACKAGE* est omis.</span><span class="sxs-lookup"><span data-stu-id="68560-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="68560-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="68560-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="68560-119">Signification</span><span class="sxs-lookup"><span data-stu-id="68560-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="68560-120"><dt>**msiInstallTypeNetworkImage**</dt></span><span class="sxs-lookup"><span data-stu-id="68560-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="68560-121">Indique une installation administrative.</span><span class="sxs-lookup"><span data-stu-id="68560-121">Indicates a administrative installation.</span></span> <span data-ttu-id="68560-122">Dans ce cas, *INSTALLPACKAGE* doit être défini sur un chemin d’accès de package.</span><span class="sxs-lookup"><span data-stu-id="68560-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="68560-123">La valeur 1 pour msiInstallTypeNetworkImage spécifie une installation d’administration.</span><span class="sxs-lookup"><span data-stu-id="68560-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="68560-124"><dt>**msiInstallTypeDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="68560-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="68560-125">Recherche des produits à corriger dans le système.</span><span class="sxs-lookup"><span data-stu-id="68560-125">Searches system for products to patch.</span></span> <span data-ttu-id="68560-126">Dans ce cas, *INSTALLPACKAGE* doit être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="68560-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="68560-127"><dt>**msiInstallSingleInstance**</dt></span><span class="sxs-lookup"><span data-stu-id="68560-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="68560-128">Correction du produit spécifié par *INSTALLPACKAGE*.</span><span class="sxs-lookup"><span data-stu-id="68560-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="68560-129">*INSTALLPACKAGE* est le code du produit de l’instance à corriger.</span><span class="sxs-lookup"><span data-stu-id="68560-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="68560-130">Ce type d’installation requiert la version de Windows Installer fournie avec Windows Server 2003 ou version ultérieure, ou Windows Installer XP SP1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68560-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="68560-131">Pour plus d’informations, consultez [installation de plusieurs instances de produits et correctifs](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="68560-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="68560-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="68560-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="68560-133">Spécifie les paramètres de propriété définis sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="68560-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="68560-134">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="68560-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68560-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68560-135">Return value</span></span>

<span data-ttu-id="68560-136">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="68560-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68560-137">Notes</span><span class="sxs-lookup"><span data-stu-id="68560-137">Remarks</span></span>

<span data-ttu-id="68560-138">Étant donné que le délimiteur de liste pour les transformations, les sources et les correctifs est un point-virgule, ce caractère ne doit pas être utilisé pour les noms de fichiers ou les chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="68560-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="68560-139">La propriété de [**réinstallation**](reinstall.md) est requise lors de l’application d’une [petite mise à jour](small-updates.md) ou d’un correctif de [mise à niveau mineur](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="68560-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="68560-140">Sans cette propriété, le correctif est inscrit sur le système, mais ne peut pas mettre à jour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="68560-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="68560-141">**Windows Installer 2,0 :** Vous devez définir la propriété [**réinstaller**](reinstall.md) sur la ligne de commande lors de l’application d’une [petite mise à jour](small-updates.md) ou d’un correctif de [mise à niveau mineure](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="68560-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="68560-142">Pour les correctifs qui n’utilisent pas de [type d’action personnalisé 51](custom-action-type-51.md) pour définir automatiquement les propriétés **REINSTALL** et [**REINSTALLMODE**](reinstallmode.md) , la propriété **REINSTALL** doit être définie explicitement à l’aide du paramètre *CommandLine* .</span><span class="sxs-lookup"><span data-stu-id="68560-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="68560-143">Définissez la propriété **réinstaller** pour répertorier les fonctionnalités affectées par le correctif ou utilisez un paramètre par défaut pratique « réinstaller = All ».</span><span class="sxs-lookup"><span data-stu-id="68560-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="68560-144">La valeur par défaut de la propriété **REINSTALLMODE** est « omus ».</span><span class="sxs-lookup"><span data-stu-id="68560-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="68560-145">**Windows Installer 3,0 et versions ultérieures :** À partir de Windows Installer version 3,0, la propriété de [**réinstallation**](reinstall.md) est configurée par le programme d’installation et n’a pas besoin d’être définie sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="68560-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="68560-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68560-146">Requirements</span></span>



| <span data-ttu-id="68560-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68560-147">Requirement</span></span> | <span data-ttu-id="68560-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="68560-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68560-149">Version</span><span class="sxs-lookup"><span data-stu-id="68560-149">Version</span></span><br/> | <span data-ttu-id="68560-150">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="68560-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="68560-151">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="68560-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="68560-152">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="68560-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="68560-153">DLL</span><span class="sxs-lookup"><span data-stu-id="68560-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="68560-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68560-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="68560-155">IID</span><span class="sxs-lookup"><span data-stu-id="68560-155">IID</span></span><br/>     | <span data-ttu-id="68560-156">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="68560-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="68560-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68560-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68560-158">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="68560-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="68560-159">À propos des propriétés</span><span class="sxs-lookup"><span data-stu-id="68560-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="68560-160">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="68560-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




