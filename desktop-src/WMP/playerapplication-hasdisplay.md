---
title: PlayerApplication.hasDisplay
description: La propriété hasDisplay récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle de lecteur distant.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- Lecteur Windows Media PlayerApplication. hasDisplay
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537460"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="1d6be-104">PlayerApplication.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="1d6be-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="1d6be-105">La propriété **hasDisplay** récupère une valeur indiquant si la vidéo peut s’afficher par le biais du contrôle de lecteur distant.</span><span class="sxs-lookup"><span data-stu-id="1d6be-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6be-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d6be-106">Syntax</span></span>

<span data-ttu-id="1d6be-107">*playerApplication*. **hasDisplay**</span><span class="sxs-lookup"><span data-stu-id="1d6be-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1d6be-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1d6be-108">Possible Values</span></span>

<span data-ttu-id="1d6be-109">Cette propriété est une **valeur booléenne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1d6be-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d6be-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1d6be-110">Remarks</span></span>

<span data-ttu-id="1d6be-111">Cette propriété est utilisée uniquement lors de la communication à distance du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1d6be-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="1d6be-112">Plusieurs contrôles de lecteur Windows Media peuvent s’exécuter à distance en même temps, mais la vidéo ne peut s’afficher qu’à un seul emplacement à la fois, soit en mode complet du lecteur, soit dans l’un des contrôles du lecteur Windows Media à distance.</span><span class="sxs-lookup"><span data-stu-id="1d6be-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="1d6be-113">Utilisez cette propriété pour déterminer si le contrôle actuel est celui par le biais duquel la vidéo peut être affichée.</span><span class="sxs-lookup"><span data-stu-id="1d6be-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="1d6be-114">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="1d6be-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6be-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d6be-115">Requirements</span></span>



| <span data-ttu-id="1d6be-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d6be-116">Requirement</span></span> | <span data-ttu-id="1d6be-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d6be-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6be-118">Version</span><span class="sxs-lookup"><span data-stu-id="1d6be-118">Version</span></span><br/> | <span data-ttu-id="1d6be-119">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1d6be-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1d6be-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1d6be-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d6be-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d6be-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6be-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d6be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6be-123">**Objet PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="1d6be-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="1d6be-124">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="1d6be-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





