---
description: La méthode FeatureInfo de l’objet session retourne un objet FeatureInfo qui contient des informations descriptives sur la fonctionnalité spécifiée.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Session. FeatureInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532003"
---
# <a name="sessionfeatureinfo-method"></a><span data-ttu-id="d189f-103">Session. FeatureInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="d189f-103">Session.FeatureInfo method</span></span>

<span data-ttu-id="d189f-104">La méthode **FeatureInfo** de l’objet [**session**](session-object.md) retourne un objet **FeatureInfo** qui contient des informations descriptives sur la fonctionnalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d189f-104">The **FeatureInfo** method of the [**Session**](session-object.md) object returns a **FeatureInfo** object containing descriptive information for the specified feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="d189f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d189f-105">Syntax</span></span>


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="d189f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d189f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d189f-107">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="d189f-107">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="d189f-108">Identifie la fonctionnalité qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="d189f-108">Identifies the feature of interest.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d189f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d189f-109">Return value</span></span>

<span data-ttu-id="d189f-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d189f-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d189f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d189f-111">Requirements</span></span>



| <span data-ttu-id="d189f-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d189f-112">Requirement</span></span> | <span data-ttu-id="d189f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d189f-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d189f-114">Version</span><span class="sxs-lookup"><span data-stu-id="d189f-114">Version</span></span><br/> | <span data-ttu-id="d189f-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d189f-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d189f-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d189f-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d189f-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="d189f-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d189f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d189f-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d189f-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d189f-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d189f-120">IID</span><span class="sxs-lookup"><span data-stu-id="d189f-120">IID</span></span><br/>     | <span data-ttu-id="d189f-121">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d189f-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="d189f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d189f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d189f-123">**MsiGetFeatureInfo**</span><span class="sxs-lookup"><span data-stu-id="d189f-123">**MsiGetFeatureInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




