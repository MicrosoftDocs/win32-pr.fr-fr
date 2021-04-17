---
description: La propriété CurrentDomain récupère le domaine DVD dans lequel se trouve l’objet MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481864"
---
# <a name="currentdomain-property"></a><span data-ttu-id="c6e04-103">CurrentDomain, propriété</span><span class="sxs-lookup"><span data-stu-id="c6e04-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="c6e04-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6e04-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c6e04-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c6e04-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c6e04-106">La `CurrentDomain` propriété récupère le domaine DVD dans lequel se trouve l’objet mswebdvd.</span><span class="sxs-lookup"><span data-stu-id="c6e04-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="c6e04-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c6e04-107">Return Value</span></span>

<span data-ttu-id="c6e04-108">Retourne une valeur entière représentant le domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="c6e04-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e04-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c6e04-109">Remarks</span></span>

<span data-ttu-id="c6e04-110">Les valeurs possibles de la propriété sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c6e04-110">The possible values of the property are:</span></span>



| <span data-ttu-id="c6e04-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6e04-111">Value</span></span> | <span data-ttu-id="c6e04-112">Description</span><span class="sxs-lookup"><span data-stu-id="c6e04-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="c6e04-113">1</span><span class="sxs-lookup"><span data-stu-id="c6e04-113">1</span></span>     | <span data-ttu-id="c6e04-114">Première lecture</span><span class="sxs-lookup"><span data-stu-id="c6e04-114">First play</span></span>           |
| <span data-ttu-id="c6e04-115">2</span><span class="sxs-lookup"><span data-stu-id="c6e04-115">2</span></span>     | <span data-ttu-id="c6e04-116">Menu du gestionnaire de vidéos</span><span class="sxs-lookup"><span data-stu-id="c6e04-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="c6e04-117">3</span><span class="sxs-lookup"><span data-stu-id="c6e04-117">3</span></span>     | <span data-ttu-id="c6e04-118">Menu de l’ensemble de titres vidéo</span><span class="sxs-lookup"><span data-stu-id="c6e04-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="c6e04-119">4</span><span class="sxs-lookup"><span data-stu-id="c6e04-119">4</span></span>     | <span data-ttu-id="c6e04-120">Intitulé</span><span class="sxs-lookup"><span data-stu-id="c6e04-120">Title</span></span>                |
| <span data-ttu-id="c6e04-121">5</span><span class="sxs-lookup"><span data-stu-id="c6e04-121">5</span></span>     | <span data-ttu-id="c6e04-122">Arrêter</span><span class="sxs-lookup"><span data-stu-id="c6e04-122">Stop</span></span>                 |



 

<span data-ttu-id="c6e04-123">Appelez cette méthode pour vérifier que le navigateur DVD est dans un domaine valide pour la méthode que vous allez appeler.</span><span class="sxs-lookup"><span data-stu-id="c6e04-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="c6e04-124">Par exemple, avant d’appeler [**PlayTitle**](playtitle-method.md), vérifiez la `CurrentDomain` propriété pour vous assurer que le navigateur DVD n’est pas dans le domaine Stop ou First Play.</span><span class="sxs-lookup"><span data-stu-id="c6e04-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 



