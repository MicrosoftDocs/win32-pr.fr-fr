---
description: La propriété FeatureUsageCount est une propriété en lecture seule qui retourne le nombre de fois que la fonctionnalité a été utilisée.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Installer. FeatureUsageCount, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540989"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="427c0-103">Installer. FeatureUsageCount, propriété</span><span class="sxs-lookup"><span data-stu-id="427c0-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="427c0-104">La propriété **FeatureUsageCount** est une propriété en lecture seule qui retourne le nombre de fois que la fonctionnalité a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="427c0-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="427c0-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="427c0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="427c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="427c0-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="427c0-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="427c0-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="427c0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="427c0-108">Remarks</span></span>

<span data-ttu-id="427c0-109">L’utilisation des méthodes [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou de leurs équivalents d’API sur la fonctionnalité spécifiée incrémente cette propriété.</span><span class="sxs-lookup"><span data-stu-id="427c0-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="427c0-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="427c0-110">Requirements</span></span>



| <span data-ttu-id="427c0-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="427c0-111">Requirement</span></span> | <span data-ttu-id="427c0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="427c0-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="427c0-113">Version</span><span class="sxs-lookup"><span data-stu-id="427c0-113">Version</span></span><br/> | <span data-ttu-id="427c0-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="427c0-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="427c0-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="427c0-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="427c0-116">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="427c0-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="427c0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="427c0-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="427c0-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="427c0-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="427c0-119">IID</span><span class="sxs-lookup"><span data-stu-id="427c0-119">IID</span></span><br/>     | <span data-ttu-id="427c0-120">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="427c0-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="427c0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="427c0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="427c0-122">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="427c0-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




