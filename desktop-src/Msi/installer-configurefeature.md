---
description: La méthode ConfigureFeature de l’objet installer configure l’état installé d’une fonctionnalité de produit.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configméthode ureFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543979"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="fc2ce-103">Installer.Configméthode ureFeature</span><span class="sxs-lookup"><span data-stu-id="fc2ce-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="fc2ce-104">La méthode **ConfigureFeature** de l’objet [**installer**](installer-object.md) configure l’état installé d’une fonctionnalité de produit.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc2ce-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="fc2ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc2ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2ce-107">*Produit*</span><span class="sxs-lookup"><span data-stu-id="fc2ce-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2ce-108">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="fc2ce-109">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="fc2ce-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2ce-110">Spécifie l’ID de fonctionnalité de la fonctionnalité à configurer.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="fc2ce-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="fc2ce-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="fc2ce-112">Spécifie l’état d’installation de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="fc2ce-113">Ce paramètre doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="fc2ce-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2ce-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="fc2ce-115">Signification</span><span class="sxs-lookup"><span data-stu-id="fc2ce-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="fc2ce-116"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ce-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="fc2ce-117">La fonctionnalité est publiée</span><span class="sxs-lookup"><span data-stu-id="fc2ce-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="fc2ce-118"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ce-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="fc2ce-119">La fonctionnalité est installée localement.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="fc2ce-120"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ce-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="fc2ce-121">La fonctionnalité est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="fc2ce-122"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ce-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="fc2ce-123">La fonctionnalité est installée pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="fc2ce-124"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ce-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="fc2ce-125">La fonctionnalité est installée à son emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2ce-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc2ce-126">Return value</span></span>

<span data-ttu-id="fc2ce-127">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc2ce-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc2ce-128">Requirements</span></span>



| <span data-ttu-id="fc2ce-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc2ce-129">Requirement</span></span> | <span data-ttu-id="fc2ce-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc2ce-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2ce-131">Version</span><span class="sxs-lookup"><span data-stu-id="fc2ce-131">Version</span></span><br/> | <span data-ttu-id="fc2ce-132">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc2ce-133">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc2ce-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc2ce-134">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc2ce-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fc2ce-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fc2ce-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc2ce-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc2ce-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fc2ce-137">IID</span><span class="sxs-lookup"><span data-stu-id="fc2ce-137">IID</span></span><br/>     | <span data-ttu-id="fc2ce-138">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fc2ce-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="fc2ce-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc2ce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2ce-140">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="fc2ce-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="fc2ce-141">Fonctions d’installation et de configuration</span><span class="sxs-lookup"><span data-stu-id="fc2ce-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




