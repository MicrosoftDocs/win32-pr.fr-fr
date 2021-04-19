---
description: La propriété FeatureCurrentState de l’objet session est une propriété en lecture seule qui retourne l’état installé actuel de la fonctionnalité désignée. Pour les valeurs d’État, consultez la propriété FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Session. FeatureCurrentState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537541"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="f7ec2-104">Session. FeatureCurrentState, propriété</span><span class="sxs-lookup"><span data-stu-id="f7ec2-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="f7ec2-105">La propriété **FeatureCurrentState** de l’objet [**session**](session-object.md) est une propriété en lecture seule qui retourne l’état installé actuel de la fonctionnalité désignée.</span><span class="sxs-lookup"><span data-stu-id="f7ec2-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="f7ec2-106">Pour les valeurs d’État, consultez la propriété [**FeatureRequestState**](session-featurerequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ec2-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="f7ec2-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f7ec2-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ec2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7ec2-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="f7ec2-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7ec2-109">Property value</span></span>

<span data-ttu-id="f7ec2-110">Nom de chaîne requis pour la fonctionnalité demandée et une clé primaire dans la [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f7ec2-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7ec2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f7ec2-111">Remarks</span></span>

<span data-ttu-id="f7ec2-112">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ec2-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ec2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7ec2-113">Requirements</span></span>



| <span data-ttu-id="f7ec2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7ec2-114">Requirement</span></span> | <span data-ttu-id="f7ec2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7ec2-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ec2-116">Version</span><span class="sxs-lookup"><span data-stu-id="f7ec2-116">Version</span></span><br/> | <span data-ttu-id="f7ec2-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f7ec2-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f7ec2-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f7ec2-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f7ec2-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7ec2-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f7ec2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ec2-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f7ec2-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ec2-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f7ec2-122">IID</span><span class="sxs-lookup"><span data-stu-id="f7ec2-122">IID</span></span><br/>     | <span data-ttu-id="f7ec2-123">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f7ec2-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="f7ec2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7ec2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ec2-125">**session**</span><span class="sxs-lookup"><span data-stu-id="f7ec2-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="f7ec2-126">**Propriété FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="f7ec2-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




