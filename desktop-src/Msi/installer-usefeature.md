---
description: La méthode UseFeature de l’objet installer incrémente le nombre d’utilisations d’une fonctionnalité particulière et retourne l’état d’installation de cette fonctionnalité. Cette méthode doit être utilisée pour indiquer l’intention d’une application d’utiliser une fonctionnalité.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Installer. UseFeature, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535359"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="8fc37-104">Installer. UseFeature, méthode</span><span class="sxs-lookup"><span data-stu-id="8fc37-104">Installer.UseFeature method</span></span>

<span data-ttu-id="8fc37-105">La méthode **UseFeature** de l’objet [**installer**](installer-object.md) incrémente le nombre d’utilisations d’une fonctionnalité particulière et retourne l’état d’installation de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8fc37-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="8fc37-106">Cette méthode doit être utilisée pour indiquer l’intention d’une application d’utiliser une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8fc37-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc37-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fc37-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="8fc37-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fc37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc37-109">*Produit*</span><span class="sxs-lookup"><span data-stu-id="8fc37-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc37-110">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="8fc37-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="8fc37-111">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="8fc37-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc37-112">Identifie la fonctionnalité à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8fc37-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="8fc37-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="8fc37-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc37-114">Ce paramètre doit être *msiInstallModeNoDetection*.</span><span class="sxs-lookup"><span data-stu-id="8fc37-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc37-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fc37-115">Return value</span></span>

<span data-ttu-id="8fc37-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8fc37-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc37-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8fc37-117">Remarks</span></span>

<span data-ttu-id="8fc37-118">La méthode **UseFeature** doit uniquement être utilisée sur les fonctionnalités dont la publication est connue.</span><span class="sxs-lookup"><span data-stu-id="8fc37-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="8fc37-119">L’application doit déterminer l’état de la fonctionnalité en appelant la propriété [**FeatureState**](installer-featurestate.md) ou la propriété [**features**](installer-features.md) ou leurs équivalents d’API.</span><span class="sxs-lookup"><span data-stu-id="8fc37-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc37-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fc37-120">Requirements</span></span>



| <span data-ttu-id="8fc37-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fc37-121">Requirement</span></span> | <span data-ttu-id="8fc37-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fc37-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc37-123">Version</span><span class="sxs-lookup"><span data-stu-id="8fc37-123">Version</span></span><br/> | <span data-ttu-id="8fc37-124">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8fc37-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8fc37-125">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8fc37-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8fc37-126">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="8fc37-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8fc37-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc37-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fc37-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc37-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8fc37-129">IID</span><span class="sxs-lookup"><span data-stu-id="8fc37-129">IID</span></span><br/>     | <span data-ttu-id="8fc37-130">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8fc37-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="8fc37-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fc37-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc37-132">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="8fc37-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




