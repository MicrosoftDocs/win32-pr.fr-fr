---
description: La méthode ApplyMultiplePatches applique un ou plusieurs correctifs aux produits qui peuvent recevoir le correctif. La méthode définit la propriété PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer. ApplyMultiplePatches, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544093"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="e6d1c-104">Installer. ApplyMultiplePatches, méthode</span><span class="sxs-lookup"><span data-stu-id="e6d1c-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="e6d1c-105">La méthode **ApplyMultiplePatches** applique un ou plusieurs correctifs aux produits qui peuvent recevoir le correctif.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="e6d1c-106">La méthode définit la propriété [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="e6d1c-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d1c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6d1c-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="e6d1c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6d1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d1c-109">*PatchPackagesList*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-110">Chaîne qui contient une liste délimitée par des points-virgules des chemins d’accès aux fichiers correctifs.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="e6d1c-111">Par exemple : "" c : \\ \\ cache de téléchargement sus \\ \\ Office \\ SP1. msp ; c : \\ sus \\ cache de téléchargement \\ \\ Office \\ qfe1. msp ; c : \\ sus \\ download \\ cache \\ Office \\ QFEn. msp ""</span><span class="sxs-lookup"><span data-stu-id="e6d1c-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="e6d1c-112">*Produit*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-113">Ce paramètre fournit le [**ProductCode**](productcode.md) du produit en cours de correction.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="e6d1c-114">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-114">This parameter is optional.</span></span> <span data-ttu-id="e6d1c-115">Lorsque ce paramètre a la valeur null, les correctifs sont appliqués à tous les produits qui sont éligibles à la réception de ces correctifs.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="e6d1c-116">*szPropertiesList*</span><span class="sxs-lookup"><span data-stu-id="e6d1c-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d1c-117">Chaîne terminée par le caractère null qui spécifie les paramètres de propriété de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="e6d1c-118">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-118">This parameter is optional.</span></span> <span data-ttu-id="e6d1c-119">Consultez [à propos des propriétés](about-properties.md) et [définition des valeurs de propriété publiques sur la ligne de commande](setting-public-property-values-on-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="e6d1c-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="e6d1c-120">Ces propriétés sont partagées par tous les produits cibles.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d1c-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6d1c-121">Return value</span></span>

<span data-ttu-id="e6d1c-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d1c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6d1c-123">Requirements</span></span>



| <span data-ttu-id="e6d1c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6d1c-124">Requirement</span></span> | <span data-ttu-id="e6d1c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6d1c-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d1c-126">Version</span><span class="sxs-lookup"><span data-stu-id="e6d1c-126">Version</span></span><br/> | <span data-ttu-id="e6d1c-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6d1c-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6d1c-129">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e6d1c-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="e6d1c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d1c-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6d1c-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6d1c-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="e6d1c-132">IID</span><span class="sxs-lookup"><span data-stu-id="e6d1c-132">IID</span></span><br/>     | <span data-ttu-id="e6d1c-133">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e6d1c-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="e6d1c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6d1c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d1c-135">À propos des propriétés</span><span class="sxs-lookup"><span data-stu-id="e6d1c-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-137">**CORRECTIF**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-138">Définition des valeurs de propriété publiques sur la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e6d1c-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="e6d1c-139">**MsiApplyMultiplePatches**</span><span class="sxs-lookup"><span data-stu-id="e6d1c-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="e6d1c-140">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e6d1c-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




