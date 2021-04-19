---
description: La propriété lecture récupère l’état actuel de l’objet MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Propriété lecture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517153"
---
# <a name="playstate-property"></a><span data-ttu-id="ef4cb-103">Propriété lecture</span><span class="sxs-lookup"><span data-stu-id="ef4cb-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="ef4cb-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ef4cb-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ef4cb-106">La `PlayState` propriété récupère l’état actuel de l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="ef4cb-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="ef4cb-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef4cb-107">Return Value</span></span>

<span data-ttu-id="ef4cb-108">Retourne une valeur entière représentant l’état actuel du navigateur DVD.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="ef4cb-109">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef4cb-109">Return code</span></span> | <span data-ttu-id="ef4cb-110">Description</span><span class="sxs-lookup"><span data-stu-id="ef4cb-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="ef4cb-111">-2</span><span class="sxs-lookup"><span data-stu-id="ef4cb-111">-2</span></span>          | <span data-ttu-id="ef4cb-112">Indéfini</span><span class="sxs-lookup"><span data-stu-id="ef4cb-112">Undefined</span></span>     |
| <span data-ttu-id="ef4cb-113">-1</span><span class="sxs-lookup"><span data-stu-id="ef4cb-113">-1</span></span>          | <span data-ttu-id="ef4cb-114">Non initialisé(e)</span><span class="sxs-lookup"><span data-stu-id="ef4cb-114">Uninitialized</span></span> |
| <span data-ttu-id="ef4cb-115">0</span><span class="sxs-lookup"><span data-stu-id="ef4cb-115">0</span></span>           | <span data-ttu-id="ef4cb-116">Arrêté</span><span class="sxs-lookup"><span data-stu-id="ef4cb-116">Stopped</span></span>       |
| <span data-ttu-id="ef4cb-117">1</span><span class="sxs-lookup"><span data-stu-id="ef4cb-117">1</span></span>           | <span data-ttu-id="ef4cb-118">Suspendu</span><span class="sxs-lookup"><span data-stu-id="ef4cb-118">Paused</span></span>        |
| <span data-ttu-id="ef4cb-119">2</span><span class="sxs-lookup"><span data-stu-id="ef4cb-119">2</span></span>           | <span data-ttu-id="ef4cb-120">En cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="ef4cb-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="ef4cb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ef4cb-121">Remarks</span></span>

<span data-ttu-id="ef4cb-122">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="ef4cb-123">L’objet **mswebdvd** contrôle le filtre du navigateur de DVD DirectShow, qui effectue le travail réel de navigation sur le DVD.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="ef4cb-124">Il s’agit en fait de l’état du navigateur DVD auquel cette propriété fait référence.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="ef4cb-125">Le navigateur DVD peut avoir plusieurs États, comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="ef4cb-126">La `PlayState` propriété peut être utile en tant qu’outil de diagnostic, mais en général, il n’y a aucune raison pour qu’une application de script surveille l’état du navigateur DVD.</span><span class="sxs-lookup"><span data-stu-id="ef4cb-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 



