---
description: La méthode ReinstallFeature de l’objet installer réinstalle les fonctionnalités ou corrige les problèmes liés aux fonctionnalités installées.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Installer. ReinstallFeature, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6bac008ee7121bbcb985b9a8ff5ba02df122266
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526640"
---
# <a name="installerreinstallfeature-method"></a><span data-ttu-id="99e13-103">Installer. ReinstallFeature, méthode</span><span class="sxs-lookup"><span data-stu-id="99e13-103">Installer.ReinstallFeature method</span></span>

<span data-ttu-id="99e13-104">La méthode **ReinstallFeature** de l’objet [**installer**](installer-object.md) réinstalle les fonctionnalités ou corrige les problèmes liés aux fonctionnalités installées.</span><span class="sxs-lookup"><span data-stu-id="99e13-104">The **ReinstallFeature** method of the [**Installer**](installer-object.md) object reinstalls features or corrects problems with installed features.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99e13-105">Syntax</span></span>


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="99e13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e13-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="99e13-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="99e13-108">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="99e13-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="99e13-109">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="99e13-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="99e13-110">Spécifie la fonctionnalité à réinstaller.</span><span class="sxs-lookup"><span data-stu-id="99e13-110">Specifies the feature to be reinstalled.</span></span> <span data-ttu-id="99e13-111">La fonctionnalité parente ou la fonctionnalité enfant de la fonctionnalité spécifiée n’est pas réinstallée.</span><span class="sxs-lookup"><span data-stu-id="99e13-111">The parent feature or child feature of the specified feature is not reinstalled.</span></span> <span data-ttu-id="99e13-112">Pour réinstaller la fonctionnalité parent ou enfant, vous devez appeler la méthode **ReinstallFeature** pour chaque séparément ou utiliser la méthode [**ReinstallProduct**](installer-reinstallproduct.md) .</span><span class="sxs-lookup"><span data-stu-id="99e13-112">To reinstall the parent or child feature, you must call the **ReinstallFeature** method for each separately or use the [**ReinstallProduct**](installer-reinstallproduct.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="99e13-113">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="99e13-113">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="99e13-114">Spécifie le type de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="99e13-114">Specifies the type of reinstallation.</span></span> <span data-ttu-id="99e13-115">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="99e13-115">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="99e13-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="99e13-116">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="99e13-117">Signification</span><span class="sxs-lookup"><span data-stu-id="99e13-117">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="99e13-118"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-118"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="99e13-119">Réinstalle uniquement si le fichier est manquant.</span><span class="sxs-lookup"><span data-stu-id="99e13-119">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="99e13-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-120"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="99e13-121">Réinstalle si le fichier est manquant ou s’il s’agit d’une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="99e13-121">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="99e13-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-122"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="99e13-123">Réinstalle si le fichier est manquant ou s’il s’agit d’une version égale ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="99e13-123">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="99e13-124"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-124"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="99e13-125">Réinstalle si le fichier est manquant ou n’est pas une version exacte.</span><span class="sxs-lookup"><span data-stu-id="99e13-125">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="99e13-126"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-126"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="99e13-127">Vérifie les fichiers exécutables Sum et les réinstalle s’ils sont manquants ou endommagés.</span><span class="sxs-lookup"><span data-stu-id="99e13-127">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="99e13-128"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-128"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="99e13-129">Réinstalle tous les fichiers, quelle que soit la version.</span><span class="sxs-lookup"><span data-stu-id="99e13-129">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="99e13-130"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-130"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="99e13-131">Garantit les valeurs requises par = entrées de Registre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="99e13-131">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="99e13-132"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-132"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="99e13-133">Garantit les valeurs requises par = entrées de registre de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="99e13-133">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="99e13-134"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-134"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="99e13-135">Valide les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="99e13-135">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="99e13-136"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-136"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="99e13-137">Utilise la source de remise en cache pour installer le package.</span><span class="sxs-lookup"><span data-stu-id="99e13-137">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e13-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99e13-138">Return value</span></span>

<span data-ttu-id="99e13-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="99e13-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e13-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99e13-140">Requirements</span></span>



| <span data-ttu-id="99e13-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99e13-141">Requirement</span></span> | <span data-ttu-id="99e13-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="99e13-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e13-143">Version</span><span class="sxs-lookup"><span data-stu-id="99e13-143">Version</span></span><br/> | <span data-ttu-id="99e13-144">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="99e13-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="99e13-145">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="99e13-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="99e13-146">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="99e13-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="99e13-147">DLL</span><span class="sxs-lookup"><span data-stu-id="99e13-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="99e13-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99e13-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="99e13-149">IID</span><span class="sxs-lookup"><span data-stu-id="99e13-149">IID</span></span><br/>     | <span data-ttu-id="99e13-150">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="99e13-150">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="99e13-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99e13-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e13-152">**MsiReinstallFeature**</span><span class="sxs-lookup"><span data-stu-id="99e13-152">**MsiReinstallFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[<span data-ttu-id="99e13-153">Fonctions d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="99e13-153">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




