---
description: La propriété ComponentCurrentState de l’objet session est une propriété en lecture seule qui retourne l’état installé actuel du composant désigné. Pour les valeurs d’État, consultez la propriété ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Session. ComponentCurrentState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537542"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="446a0-104">Session. ComponentCurrentState, propriété</span><span class="sxs-lookup"><span data-stu-id="446a0-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="446a0-105">La propriété **ComponentCurrentState** de l’objet [**session**](session-object.md) est une propriété en lecture seule qui retourne l’état installé actuel du composant désigné.</span><span class="sxs-lookup"><span data-stu-id="446a0-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="446a0-106">Pour les valeurs d’État, consultez la propriété [**ComponentRequestState**](session-componentrequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="446a0-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="446a0-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="446a0-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="446a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="446a0-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="446a0-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="446a0-109">Property value</span></span>

<span data-ttu-id="446a0-110">Nom de chaîne requis du composant demandé, clé primaire dans la table des composants.</span><span class="sxs-lookup"><span data-stu-id="446a0-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="446a0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="446a0-111">Remarks</span></span>

<span data-ttu-id="446a0-112">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="446a0-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="446a0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="446a0-113">Requirements</span></span>



| <span data-ttu-id="446a0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="446a0-114">Requirement</span></span> | <span data-ttu-id="446a0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="446a0-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="446a0-116">Version</span><span class="sxs-lookup"><span data-stu-id="446a0-116">Version</span></span><br/> | <span data-ttu-id="446a0-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="446a0-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="446a0-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="446a0-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="446a0-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="446a0-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="446a0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="446a0-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="446a0-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="446a0-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="446a0-122">IID</span><span class="sxs-lookup"><span data-stu-id="446a0-122">IID</span></span><br/>     | <span data-ttu-id="446a0-123">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="446a0-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="446a0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="446a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446a0-125">**session**</span><span class="sxs-lookup"><span data-stu-id="446a0-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="446a0-126">**Propriété ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="446a0-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




