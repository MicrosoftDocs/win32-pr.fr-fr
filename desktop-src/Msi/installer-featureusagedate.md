---
description: La propriété FeatureUsageDate est une propriété en lecture seule qui retourne la date de la dernière utilisation de la fonctionnalité spécifiée.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer. FeatureUsageDate, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537326"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="d74e9-103">Installer. FeatureUsageDate, propriété</span><span class="sxs-lookup"><span data-stu-id="d74e9-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="d74e9-104">La propriété **FeatureUsageDate** est une propriété en lecture seule qui retourne la date de la dernière utilisation de la fonctionnalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d74e9-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="d74e9-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d74e9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d74e9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d74e9-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="d74e9-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d74e9-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d74e9-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d74e9-108">Remarks</span></span>

<span data-ttu-id="d74e9-109">L’utilisation des méthodes [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou de leurs équivalents d’API sur la fonctionnalité spécifiée définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d74e9-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="d74e9-110">La date est au format de date MS-DOS, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d74e9-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="d74e9-111">Bits</span><span class="sxs-lookup"><span data-stu-id="d74e9-111">Bits</span></span> | <span data-ttu-id="d74e9-112">Contenu</span><span class="sxs-lookup"><span data-stu-id="d74e9-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="d74e9-113">0-4</span><span class="sxs-lookup"><span data-stu-id="d74e9-113">0-4</span></span>  | <span data-ttu-id="d74e9-114">Jour du mois (1-31)</span><span class="sxs-lookup"><span data-stu-id="d74e9-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="d74e9-115">5-8</span><span class="sxs-lookup"><span data-stu-id="d74e9-115">5-8</span></span>  | <span data-ttu-id="d74e9-116">Month (1 = janvier, 2 = février, etc.)</span><span class="sxs-lookup"><span data-stu-id="d74e9-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="d74e9-117">9-15</span><span class="sxs-lookup"><span data-stu-id="d74e9-117">9-15</span></span> | <span data-ttu-id="d74e9-118">Décalage d’année à partir de 1980 (Ajouter 1980 pour atteindre l’année réelle)</span><span class="sxs-lookup"><span data-stu-id="d74e9-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d74e9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d74e9-119">Requirements</span></span>



| <span data-ttu-id="d74e9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d74e9-120">Requirement</span></span> | <span data-ttu-id="d74e9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d74e9-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d74e9-122">Version</span><span class="sxs-lookup"><span data-stu-id="d74e9-122">Version</span></span><br/> | <span data-ttu-id="d74e9-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d74e9-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d74e9-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d74e9-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d74e9-125">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="d74e9-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d74e9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d74e9-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="d74e9-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d74e9-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d74e9-128">IID</span><span class="sxs-lookup"><span data-stu-id="d74e9-128">IID</span></span><br/>     | <span data-ttu-id="d74e9-129">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d74e9-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="d74e9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d74e9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74e9-131">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="d74e9-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




