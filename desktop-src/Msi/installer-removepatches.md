---
description: La méthode RemovePatches supprime un ou plusieurs correctifs pour les produits éligibles pour recevoir le correctif. La méthode RemovePatches appelle MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer. RemovePatches, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533103"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="835d7-104">Installer. RemovePatches, méthode</span><span class="sxs-lookup"><span data-stu-id="835d7-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="835d7-105">La méthode **RemovePatches** supprime un ou plusieurs correctifs pour les produits éligibles pour recevoir le correctif.</span><span class="sxs-lookup"><span data-stu-id="835d7-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="835d7-106">La méthode **RemovePatches** appelle [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="835d7-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="835d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="835d7-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="835d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="835d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835d7-109">*PatchList*</span><span class="sxs-lookup"><span data-stu-id="835d7-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="835d7-110">Chaîne qui contient une liste délimitée par des points-virgules des correctifs à supprimer.</span><span class="sxs-lookup"><span data-stu-id="835d7-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="835d7-111">Chaque correctif peut être représenté soit par le chemin d’accès complet au package de correctifs, soit par le GUID du correctif.</span><span class="sxs-lookup"><span data-stu-id="835d7-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="835d7-112">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="835d7-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="835d7-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="835d7-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="835d7-114">Chaîne contenant le GUID du produit à partir duquel les correctifs doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="835d7-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="835d7-115">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="835d7-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="835d7-116">*UninstallType*</span><span class="sxs-lookup"><span data-stu-id="835d7-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="835d7-117">Valeur entière qui spécifie le type de suppression de correctif logiciel.</span><span class="sxs-lookup"><span data-stu-id="835d7-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="835d7-118">Ce paramètre doit être **msiInstallTypeSingleInstance**.</span><span class="sxs-lookup"><span data-stu-id="835d7-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="835d7-119">*PropertyList*</span><span class="sxs-lookup"><span data-stu-id="835d7-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="835d7-120">Chaîne qui spécifie les paires propriété = valeur à inclure.</span><span class="sxs-lookup"><span data-stu-id="835d7-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="835d7-121">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="835d7-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="835d7-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="835d7-122">Return value</span></span>

<span data-ttu-id="835d7-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="835d7-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="835d7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="835d7-124">Remarks</span></span>

<span data-ttu-id="835d7-125">Consultez [désinstallation des correctifs](uninstalling-patches.md) pour obtenir un exemple qui montre comment une application peut supprimer un correctif de tous les produits disponibles pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="835d7-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="835d7-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="835d7-126">Requirements</span></span>



| <span data-ttu-id="835d7-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="835d7-127">Requirement</span></span> | <span data-ttu-id="835d7-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="835d7-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="835d7-129">Version</span><span class="sxs-lookup"><span data-stu-id="835d7-129">Version</span></span><br/> | <span data-ttu-id="835d7-130">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="835d7-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="835d7-131">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="835d7-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="835d7-132">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="835d7-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="835d7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="835d7-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="835d7-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="835d7-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="835d7-135">IID</span><span class="sxs-lookup"><span data-stu-id="835d7-135">IID</span></span><br/>     | <span data-ttu-id="835d7-136">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="835d7-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="835d7-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="835d7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835d7-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="835d7-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="835d7-139">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="835d7-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="835d7-140">Désinstallation des correctifs</span><span class="sxs-lookup"><span data-stu-id="835d7-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="835d7-141">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="835d7-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




