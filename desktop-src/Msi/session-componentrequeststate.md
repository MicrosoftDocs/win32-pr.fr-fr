---
description: La propriété ComponentRequestState de l’objet de session obtient ou demande une modification de l’état d’action d’une ligne dans la table des composants.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Session. ComponentRequestState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538122"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="593d1-103">Session. ComponentRequestState, propriété</span><span class="sxs-lookup"><span data-stu-id="593d1-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="593d1-104">La propriété **ComponentRequestState** de l’objet de [**session**](session-object.md) obtient ou demande une modification de l’état d’action d’une ligne dans la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="593d1-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="593d1-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="593d1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="593d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="593d1-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="593d1-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="593d1-107">Property value</span></span>

<span data-ttu-id="593d1-108">Nom de chaîne requis de l’élément de composant, clé primaire de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="593d1-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="593d1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="593d1-109">Remarks</span></span>



| <span data-ttu-id="593d1-110">État de sélection</span><span class="sxs-lookup"><span data-stu-id="593d1-110">Selection state</span></span>        | <span data-ttu-id="593d1-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d1-111">Value</span></span> | <span data-ttu-id="593d1-112">Description</span><span class="sxs-lookup"><span data-stu-id="593d1-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="593d1-113">Null</span><span class="sxs-lookup"><span data-stu-id="593d1-113">Null</span></span>                   | <span data-ttu-id="593d1-114">Null</span><span class="sxs-lookup"><span data-stu-id="593d1-114">Null</span></span>  | <span data-ttu-id="593d1-115">Demande qu’aucune action ne soit effectuée pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="593d1-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="593d1-116">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="593d1-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="593d1-117">2</span><span class="sxs-lookup"><span data-stu-id="593d1-117">2</span></span>     | <span data-ttu-id="593d1-118">L’élément doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="593d1-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="593d1-119">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="593d1-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="593d1-120">3</span><span class="sxs-lookup"><span data-stu-id="593d1-120">3</span></span>     | <span data-ttu-id="593d1-121">L’élément doit être installé localement.</span><span class="sxs-lookup"><span data-stu-id="593d1-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="593d1-122">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="593d1-122">msiInstallStateSource</span></span>  | <span data-ttu-id="593d1-123">4</span><span class="sxs-lookup"><span data-stu-id="593d1-123">4</span></span>     | <span data-ttu-id="593d1-124">L’élément doit être installé et exécuté à partir du média source.</span><span class="sxs-lookup"><span data-stu-id="593d1-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="593d1-125">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="593d1-125">msiInstallStateDefault</span></span> | <span data-ttu-id="593d1-126">5</span><span class="sxs-lookup"><span data-stu-id="593d1-126">5</span></span>     | <span data-ttu-id="593d1-127">S’il est installé, l’élément doit être réinstallé dans le même État.</span><span class="sxs-lookup"><span data-stu-id="593d1-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="593d1-128">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="593d1-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="593d1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="593d1-129">Requirements</span></span>



| <span data-ttu-id="593d1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="593d1-130">Requirement</span></span> | <span data-ttu-id="593d1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="593d1-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="593d1-132">Version</span><span class="sxs-lookup"><span data-stu-id="593d1-132">Version</span></span><br/> | <span data-ttu-id="593d1-133">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="593d1-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="593d1-134">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="593d1-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="593d1-135">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="593d1-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="593d1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="593d1-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="593d1-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="593d1-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="593d1-138">IID</span><span class="sxs-lookup"><span data-stu-id="593d1-138">IID</span></span><br/>     | <span data-ttu-id="593d1-139">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="593d1-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




