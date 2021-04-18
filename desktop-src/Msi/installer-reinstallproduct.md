---
description: La méthode ReinstallProduct de l’objet installer réinstalle un produit ou corrige les problèmes d’installation dans un produit installé.
ms.assetid: ff933cce-9f27-4215-9291-dd860d9c4d08
title: Installer. ReinstallProduct, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1570f5a0dc607b4a011a5b4276a243c59a64392d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533104"
---
# <a name="installerreinstallproduct-method"></a><span data-ttu-id="34a9a-103">Installer. ReinstallProduct, méthode</span><span class="sxs-lookup"><span data-stu-id="34a9a-103">Installer.ReinstallProduct method</span></span>

<span data-ttu-id="34a9a-104">La méthode **ReinstallProduct** de l’objet [**installer**](installer-object.md) réinstalle un produit ou corrige les problèmes d’installation dans un produit installé.</span><span class="sxs-lookup"><span data-stu-id="34a9a-104">The **ReinstallProduct** method of the [**Installer**](installer-object.md) object reinstalls a product or corrects installation problems in an installed product.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a9a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34a9a-105">Syntax</span></span>


```JScript
Installer.ReinstallProduct(
  Product,
  ReinstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="34a9a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34a9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a9a-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="34a9a-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="34a9a-108">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="34a9a-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="34a9a-109">*ReinstallMode*</span><span class="sxs-lookup"><span data-stu-id="34a9a-109">*ReinstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="34a9a-110">Spécifie le type de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="34a9a-110">Specifies the type of reinstallation.</span></span> <span data-ttu-id="34a9a-111">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="34a9a-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="34a9a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="34a9a-112">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="34a9a-113">Signification</span><span class="sxs-lookup"><span data-stu-id="34a9a-113">Meaning</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <span data-ttu-id="34a9a-114"><dt>**msiReinstallModeFileMissing**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-114"><dt>**msiReinstallModeFileMissing**</dt></span></span> </dl>                     | <span data-ttu-id="34a9a-115">Réinstalle uniquement si le fichier est manquant.</span><span class="sxs-lookup"><span data-stu-id="34a9a-115">Reinstalls only if the file is missing.</span></span><br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <span data-ttu-id="34a9a-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-116"><dt>**msiReinstallModeFileOlderVersion**</dt></span></span> </dl> | <span data-ttu-id="34a9a-117">Réinstalle si le fichier est manquant ou s’il s’agit d’une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="34a9a-117">Reinstalls if the file is missing or is an older version.</span></span><br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <span data-ttu-id="34a9a-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-118"><dt>**msiReinstallModeFileEqualVersion**</dt></span></span> </dl> | <span data-ttu-id="34a9a-119">Réinstalle si le fichier est manquant ou s’il s’agit d’une version égale ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="34a9a-119">Reinstalls if the file is missing or is an equal or older version.</span></span><br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <span data-ttu-id="34a9a-120"><dt>**msiReinstallModeFileExact**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-120"><dt>**msiReinstallModeFileExact**</dt></span></span> </dl>                             | <span data-ttu-id="34a9a-121">Réinstalle si le fichier est manquant ou n’est pas une version exacte.</span><span class="sxs-lookup"><span data-stu-id="34a9a-121">Reinstalls if the file is missing or is not an exact version.</span></span><br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <span data-ttu-id="34a9a-122"><dt>**msiReinstallModeFileVerify**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-122"><dt>**msiReinstallModeFileVerify**</dt></span></span> </dl>                         | <span data-ttu-id="34a9a-123">Vérifie les fichiers exécutables Sum et les réinstalle s’ils sont manquants ou endommagés.</span><span class="sxs-lookup"><span data-stu-id="34a9a-123">Checks sum executables, and reinstalls if they are missing or corrupt.</span></span><br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <span data-ttu-id="34a9a-124"><dt>**msiReinstallModeFileReplace**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-124"><dt>**msiReinstallModeFileReplace**</dt></span></span> </dl>                     | <span data-ttu-id="34a9a-125">Réinstalle tous les fichiers, quelle que soit la version.</span><span class="sxs-lookup"><span data-stu-id="34a9a-125">Reinstalls all files regardless of version.</span></span><br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <span data-ttu-id="34a9a-126"><dt>**msiReinstallModeUserData**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-126"><dt>**msiReinstallModeUserData**</dt></span></span> </dl>                                 | <span data-ttu-id="34a9a-127">Garantit les valeurs requises par = entrées de Registre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="34a9a-127">Ensures required per=user registry entries.</span></span><br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <span data-ttu-id="34a9a-128"><dt>**msiReinstallModeMachineData**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-128"><dt>**msiReinstallModeMachineData**</dt></span></span> </dl>                     | <span data-ttu-id="34a9a-129">Garantit les valeurs requises par = entrées de registre de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="34a9a-129">Ensures required per=machine registry entries.</span></span><br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <span data-ttu-id="34a9a-130"><dt>**msiReinstallModeShortcut**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-130"><dt>**msiReinstallModeShortcut**</dt></span></span> </dl>                                 | <span data-ttu-id="34a9a-131">Valide les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="34a9a-131">Validates shortcuts.</span></span><br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <span data-ttu-id="34a9a-132"><dt>**msiReinstallModePackage**</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-132"><dt>**msiReinstallModePackage**</dt></span></span> </dl>                                     | <span data-ttu-id="34a9a-133">Utilise la source de remise en cache pour installer le package.</span><span class="sxs-lookup"><span data-stu-id="34a9a-133">Uses the recache source to install the package.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a9a-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34a9a-134">Return value</span></span>

<span data-ttu-id="34a9a-135">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="34a9a-135">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a9a-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34a9a-136">Requirements</span></span>



| <span data-ttu-id="34a9a-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34a9a-137">Requirement</span></span> | <span data-ttu-id="34a9a-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="34a9a-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a9a-139">Version</span><span class="sxs-lookup"><span data-stu-id="34a9a-139">Version</span></span><br/> | <span data-ttu-id="34a9a-140">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34a9a-140">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34a9a-141">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34a9a-141">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34a9a-142">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="34a9a-142">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="34a9a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="34a9a-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="34a9a-144"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34a9a-144"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="34a9a-145">IID</span><span class="sxs-lookup"><span data-stu-id="34a9a-145">IID</span></span><br/>     | <span data-ttu-id="34a9a-146">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="34a9a-146">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="34a9a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34a9a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a9a-148">**MsiReinstallProduct**</span><span class="sxs-lookup"><span data-stu-id="34a9a-148">**MsiReinstallProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
</dt> <dt>

[<span data-ttu-id="34a9a-149">Fonctions d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="34a9a-149">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




