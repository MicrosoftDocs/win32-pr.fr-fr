---
description: La propriété FeatureState en lecture seule retourne l’état installé d’une fonctionnalité.
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: Installer. FeatureState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532513"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="919bf-103">Installer. FeatureState, propriété</span><span class="sxs-lookup"><span data-stu-id="919bf-103">Installer.FeatureState property</span></span>

<span data-ttu-id="919bf-104">La propriété **FeatureState** en lecture seule retourne l’état installé d’une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="919bf-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="919bf-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="919bf-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="919bf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="919bf-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="919bf-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="919bf-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="919bf-108">Notes</span><span class="sxs-lookup"><span data-stu-id="919bf-108">Remarks</span></span>

<span data-ttu-id="919bf-109">Cette propriété retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="919bf-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="919bf-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="919bf-110">Value</span></span>                     | <span data-ttu-id="919bf-111">Description</span><span class="sxs-lookup"><span data-stu-id="919bf-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="919bf-112">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="919bf-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="919bf-113">La fonctionnalité n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="919bf-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="919bf-114">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="919bf-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="919bf-115">La fonctionnalité est publiée.</span><span class="sxs-lookup"><span data-stu-id="919bf-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="919bf-116">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="919bf-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="919bf-117">La fonctionnalité est installée pour s’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="919bf-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="919bf-118">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="919bf-118">msiInstallStateSource</span></span>     | <span data-ttu-id="919bf-119">La fonctionnalité est installée pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="919bf-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="919bf-120">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="919bf-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="919bf-121">Un paramètre non valide a été passé à la fonction.</span><span class="sxs-lookup"><span data-stu-id="919bf-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="919bf-122">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="919bf-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="919bf-123">Le code du produit ou l’ID de fonctionnalité est inconnu.</span><span class="sxs-lookup"><span data-stu-id="919bf-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="919bf-124">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="919bf-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="919bf-125">Les données de configuration sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="919bf-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="919bf-126">La propriété **FeatureState** ne valide pas le fait que la fonctionnalité soit accessible.</span><span class="sxs-lookup"><span data-stu-id="919bf-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="919bf-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="919bf-127">Requirements</span></span>



| <span data-ttu-id="919bf-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="919bf-128">Requirement</span></span> | <span data-ttu-id="919bf-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="919bf-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="919bf-130">Version</span><span class="sxs-lookup"><span data-stu-id="919bf-130">Version</span></span><br/> | <span data-ttu-id="919bf-131">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="919bf-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="919bf-132">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="919bf-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="919bf-133">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="919bf-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="919bf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="919bf-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="919bf-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919bf-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="919bf-136">IID</span><span class="sxs-lookup"><span data-stu-id="919bf-136">IID</span></span><br/>     | <span data-ttu-id="919bf-137">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="919bf-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="919bf-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="919bf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919bf-139">**MsiQueryFeatureState**</span><span class="sxs-lookup"><span data-stu-id="919bf-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




