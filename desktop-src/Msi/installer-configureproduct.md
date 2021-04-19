---
description: La méthode ConfigureProduct de l’objet installer installe ou désinstalle un produit.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configméthode ureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537924"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="7ceb4-103">Installer.Configméthode ureProduct</span><span class="sxs-lookup"><span data-stu-id="7ceb4-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="7ceb4-104">La méthode **ConfigureProduct** de l’objet [**installer**](installer-object.md) installe ou désinstalle un produit.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ceb4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ceb4-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="7ceb4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ceb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ceb4-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="7ceb4-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="7ceb4-108">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="7ceb4-109">*InstallLevel*</span><span class="sxs-lookup"><span data-stu-id="7ceb4-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="7ceb4-110">Spécifie la configuration d’installation par défaut du produit.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="7ceb4-111">Le paramètre InstallLevel est ignoré et toutes les fonctionnalités sont installées si le paramètre InstallState est défini sur une autre valeur que msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="7ceb4-112">Ce paramètre doit avoir la valeur 0 (installation à l’aide des niveaux de fonctionnalité créés), 65535 (installer toutes les fonctionnalités) ou une valeur comprise entre 0 et 65535 pour installer un sous-ensemble des fonctionnalités disponibles.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="7ceb4-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="7ceb4-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="7ceb4-114">Spécifie l’état d’installation de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="7ceb4-115">Ce paramètre doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="7ceb4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ceb4-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="7ceb4-117">Signification</span><span class="sxs-lookup"><span data-stu-id="7ceb4-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="7ceb4-118"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb4-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="7ceb4-119">La fonctionnalité est publiée</span><span class="sxs-lookup"><span data-stu-id="7ceb4-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="7ceb4-120"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb4-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="7ceb4-121">La fonctionnalité est installée localement.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="7ceb4-122"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb4-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="7ceb4-123">La fonctionnalité est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="7ceb4-124"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb4-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="7ceb4-125">La fonctionnalité est installée pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="7ceb4-126"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb4-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="7ceb4-127">La fonctionnalité est installée à son emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ceb4-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ceb4-128">Return value</span></span>

<span data-ttu-id="7ceb4-129">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ceb4-130">Notes</span><span class="sxs-lookup"><span data-stu-id="7ceb4-130">Remarks</span></span>

<span data-ttu-id="7ceb4-131">La méthode **ConfigureProduct** affiche l’interface utilisateur à l’aide des paramètres actuels.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="7ceb4-132">Les paramètres de l’interface utilisateur peuvent être modifiés en modifiant la [**propriété UILevel (objet programme d’installation)**](installer-uilevel.md) avant d’appeler la méthode **ConfigureProduct** .</span><span class="sxs-lookup"><span data-stu-id="7ceb4-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="7ceb4-133">Si le paramètre *InstallState* est défini sur une autre valeur que msiInstallStateDefault, le paramètre *InstallLevel* est ignoré et toutes les fonctionnalités du produit sont installées.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="7ceb4-134">Utilisez la méthode [**ConfigureFeature**](installer-configurefeature.md) pour contrôler l’installation de fonctionnalités individuelles lorsque le paramètre *InstallState* n’a pas la valeur msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ceb4-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ceb4-135">Requirements</span></span>



| <span data-ttu-id="7ceb4-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ceb4-136">Requirement</span></span> | <span data-ttu-id="7ceb4-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ceb4-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ceb4-138">Version</span><span class="sxs-lookup"><span data-stu-id="7ceb4-138">Version</span></span><br/> | <span data-ttu-id="7ceb4-139">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7ceb4-140">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7ceb4-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7ceb4-141">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ceb4-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7ceb4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ceb4-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="7ceb4-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ceb4-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7ceb4-144">IID</span><span class="sxs-lookup"><span data-stu-id="7ceb4-144">IID</span></span><br/>     | <span data-ttu-id="7ceb4-145">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7ceb4-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="7ceb4-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ceb4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ceb4-147">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="7ceb4-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="7ceb4-148">Fonctions d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="7ceb4-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




