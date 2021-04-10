---
description: L’événement ShowMenu est envoyé lorsque le disque active ou désactive l’émission d’un menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950209"
---
# <a name="showmenu"></a><span data-ttu-id="a5a66-103">ShowMenu</span><span class="sxs-lookup"><span data-stu-id="a5a66-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="a5a66-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a5a66-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a5a66-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a5a66-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a5a66-106">L' `ShowMenu` événement est envoyé lorsque le disque active ou désactive l’émission d’un menu.</span><span class="sxs-lookup"><span data-stu-id="a5a66-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="a5a66-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5a66-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a66-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span><span class="sxs-lookup"><span data-stu-id="a5a66-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="a5a66-109">Spécifie le menu qui a été activé ou désactivé en tant que valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="a5a66-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="a5a66-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5a66-110">Value</span></span> | <span data-ttu-id="a5a66-111">Description</span><span class="sxs-lookup"><span data-stu-id="a5a66-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="a5a66-112">2</span><span class="sxs-lookup"><span data-stu-id="a5a66-112">2</span></span>     | <span data-ttu-id="a5a66-113">Intitulé</span><span class="sxs-lookup"><span data-stu-id="a5a66-113">Title</span></span>       |
| <span data-ttu-id="a5a66-114">3</span><span class="sxs-lookup"><span data-stu-id="a5a66-114">3</span></span>     | <span data-ttu-id="a5a66-115">Root</span><span class="sxs-lookup"><span data-stu-id="a5a66-115">Root</span></span>        |
| <span data-ttu-id="a5a66-116">4</span><span class="sxs-lookup"><span data-stu-id="a5a66-116">4</span></span>     | <span data-ttu-id="a5a66-117">Sous-titres</span><span class="sxs-lookup"><span data-stu-id="a5a66-117">Subpicture</span></span>  |
| <span data-ttu-id="a5a66-118">5</span><span class="sxs-lookup"><span data-stu-id="a5a66-118">5</span></span>     | <span data-ttu-id="a5a66-119">Audio</span><span class="sxs-lookup"><span data-stu-id="a5a66-119">Audio</span></span>       |
| <span data-ttu-id="a5a66-120">6</span><span class="sxs-lookup"><span data-stu-id="a5a66-120">6</span></span>     | <span data-ttu-id="a5a66-121">Angle</span><span class="sxs-lookup"><span data-stu-id="a5a66-121">Angle</span></span>       |
| <span data-ttu-id="a5a66-122">7</span><span class="sxs-lookup"><span data-stu-id="a5a66-122">7</span></span>     | <span data-ttu-id="a5a66-123">Chapitre</span><span class="sxs-lookup"><span data-stu-id="a5a66-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a5a66-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="a5a66-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="a5a66-125">Spécifie si l’opération est activée ou désactivée en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="a5a66-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



