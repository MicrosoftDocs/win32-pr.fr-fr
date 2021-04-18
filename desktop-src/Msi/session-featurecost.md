---
description: La propriété FeatureCost de l’objet session retourne la quantité totale d’espace disque (en unités de 512 octets) requise par la fonctionnalité spécifiée et ses fonctionnalités parentes (jusqu’à la racine du tableau des fonctionnalités).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session. FeatureCost, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540506"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="11a31-103">Session. FeatureCost, propriété</span><span class="sxs-lookup"><span data-stu-id="11a31-103">Session.FeatureCost property</span></span>

<span data-ttu-id="11a31-104">La propriété **FeatureCost** de l’objet [**session**](session-object.md) retourne la quantité totale d’espace disque (en unités de 512 octets) requise par la fonctionnalité spécifiée et ses fonctionnalités parentes (jusqu’à la racine du tableau des fonctionnalités).</span><span class="sxs-lookup"><span data-stu-id="11a31-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="11a31-105">Pour chaque fonctionnalité, le coût total est constitué des coûts de disque attribués à chaque composant lié à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="11a31-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="11a31-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="11a31-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a31-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11a31-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="11a31-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="11a31-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="11a31-109">Notes</span><span class="sxs-lookup"><span data-stu-id="11a31-109">Remarks</span></span>

<span data-ttu-id="11a31-110">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="11a31-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="11a31-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11a31-111">Requirements</span></span>



| <span data-ttu-id="11a31-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11a31-112">Requirement</span></span> | <span data-ttu-id="11a31-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="11a31-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a31-114">Version</span><span class="sxs-lookup"><span data-stu-id="11a31-114">Version</span></span><br/> | <span data-ttu-id="11a31-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="11a31-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="11a31-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11a31-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="11a31-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="11a31-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="11a31-118">DLL</span><span class="sxs-lookup"><span data-stu-id="11a31-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="11a31-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a31-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="11a31-120">IID</span><span class="sxs-lookup"><span data-stu-id="11a31-120">IID</span></span><br/>     | <span data-ttu-id="11a31-121">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="11a31-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




