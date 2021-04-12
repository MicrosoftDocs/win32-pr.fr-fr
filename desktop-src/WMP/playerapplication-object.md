---
title: Objet PlayerApplication
description: L’objet PlayerApplication permet de coordonner le basculement entre un contrôle du lecteur Windows Media distant et le mode complet du lecteur Windows Media.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Objet PlayerApplication lecteur Windows Media
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313243"
---
# <a name="playerapplication-object"></a><span data-ttu-id="a9197-104">Objet PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="a9197-104">PlayerApplication Object</span></span>

<span data-ttu-id="a9197-105">L’objet **PlayerApplication** permet de coordonner le basculement entre un contrôle du lecteur Windows Media distant et le mode complet du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a9197-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="a9197-106">Cet objet est utilisé uniquement avec les programmes C++ qui implémentent l’interface **IWMPRemoteMediaServices** et incorporent le contrôle Player en mode distant.</span><span class="sxs-lookup"><span data-stu-id="a9197-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="a9197-107">Les fichiers d’apparence utilisés comme interfaces personnalisées pour le contrôle du lecteur Windows Media distant accèdent à cet objet dans le code de script via l’attribut global **playerApplication** .</span><span class="sxs-lookup"><span data-stu-id="a9197-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="a9197-108">L’objet **PlayerApplication** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9197-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="a9197-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="a9197-109">Property</span></span>                                           | <span data-ttu-id="a9197-110">Description</span><span class="sxs-lookup"><span data-stu-id="a9197-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9197-111">hasDisplay</span><span class="sxs-lookup"><span data-stu-id="a9197-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="a9197-112">Récupère une valeur indiquant si la vidéo peut s’afficher via le contrôle du lecteur Windows Media distant.</span><span class="sxs-lookup"><span data-stu-id="a9197-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="a9197-113">playerDocked</span><span class="sxs-lookup"><span data-stu-id="a9197-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="a9197-114">Récupère une valeur indiquant si le lecteur Windows Media est dans un état d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="a9197-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="a9197-115">L’objet **PlayerApplication** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9197-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="a9197-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="a9197-116">Method</span></span>                                                                       | <span data-ttu-id="a9197-117">Description</span><span class="sxs-lookup"><span data-stu-id="a9197-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="a9197-118">switchToControl</span><span class="sxs-lookup"><span data-stu-id="a9197-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="a9197-119">Bascule un contrôle du lecteur Windows Media distant vers l’état d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="a9197-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="a9197-120">switchToPlayerApplication</span><span class="sxs-lookup"><span data-stu-id="a9197-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="a9197-121">Bascule un contrôle du lecteur Windows Media distant vers le mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="a9197-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="a9197-122">L’objet **PlayerApplication** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="a9197-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="a9197-123">Object</span><span class="sxs-lookup"><span data-stu-id="a9197-123">Object</span></span>                      | <span data-ttu-id="a9197-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="a9197-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="a9197-125">Lecteur</span><span class="sxs-lookup"><span data-stu-id="a9197-125">Player</span></span>](player-object.md) | [<span data-ttu-id="a9197-126">playerApplication</span><span class="sxs-lookup"><span data-stu-id="a9197-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="a9197-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9197-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9197-128">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="a9197-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="a9197-129">**Utilisation à distance du contrôle Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="a9197-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




