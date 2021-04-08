---
description: La propriété EnableResetOnStop définit ou récupère une valeur qui détermine le mode de reprise de la lecture lorsque le graphique de filtre effectue une transition à partir de l’état arrêté.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propriété EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746645"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="44dae-103">Propriété EnableResetOnStop</span><span class="sxs-lookup"><span data-stu-id="44dae-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="44dae-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="44dae-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="44dae-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="44dae-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="44dae-106">La `EnableResetOnStop` propriété définit ou récupère une valeur qui détermine le mode de reprise de la lecture lorsque le graphique de filtre effectue une transition à partir de l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="44dae-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="44dae-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44dae-107">Return Value</span></span>

<span data-ttu-id="44dae-108">Retourne une valeur booléenne indiquant où l’objet MSWebDVD recommence à s’exécuter après l’arrêt du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="44dae-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="44dae-109">Notes</span><span class="sxs-lookup"><span data-stu-id="44dae-109">Remarks</span></span>

<span data-ttu-id="44dae-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="44dae-110">This property is read/write.</span></span>

<span data-ttu-id="44dae-111">Les valeurs possibles de cette propriété sont : avec la valeur par défaut true.</span><span class="sxs-lookup"><span data-stu-id="44dae-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="44dae-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="44dae-112">Value</span></span> | <span data-ttu-id="44dae-113">Description</span><span class="sxs-lookup"><span data-stu-id="44dae-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44dae-114">true</span><span class="sxs-lookup"><span data-stu-id="44dae-114">true</span></span>  | <span data-ttu-id="44dae-115">Le navigateur DVD est réinitialisé et démarre la lecture à partir du début du disque. Il s’agit de la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="44dae-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="44dae-116">false</span><span class="sxs-lookup"><span data-stu-id="44dae-116">false</span></span> | <span data-ttu-id="44dae-117">Le navigateur DVD reprend la lecture là où il s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="44dae-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



