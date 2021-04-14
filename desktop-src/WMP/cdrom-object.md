---
title: Objet cdrom
description: L’objet cdrom offre un moyen d’accéder à un CD ou un DVD dans son lecteur.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Objet cdrom lecteur Windows Media
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104311923"
---
# <a name="cdrom-object"></a><span data-ttu-id="ae39e-104">Objet cdrom</span><span class="sxs-lookup"><span data-stu-id="ae39e-104">Cdrom Object</span></span>

<span data-ttu-id="ae39e-105">L’objet **cdrom** offre un moyen d’accéder à un CD ou un DVD dans son lecteur.</span><span class="sxs-lookup"><span data-stu-id="ae39e-105">The **Cdrom** object provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="ae39e-106">L’objet **cdrom** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ae39e-106">The **Cdrom** object supports the following properties.</span></span>



| <span data-ttu-id="ae39e-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="ae39e-107">Property</span></span>                                   | <span data-ttu-id="ae39e-108">Description</span><span class="sxs-lookup"><span data-stu-id="ae39e-108">Description</span></span>                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae39e-109">driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="ae39e-109">driveSpecifier</span></span>](cdrom-drivespecifier.md) | <span data-ttu-id="ae39e-110">Récupère la lettre du lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="ae39e-110">Retrieves the CD or DVD drive letter.</span></span>                                                                                                                   |
| [<span data-ttu-id="ae39e-111">playlist</span><span class="sxs-lookup"><span data-stu-id="ae39e-111">playlist</span></span>](cdrom-playlist.md)             | <span data-ttu-id="ae39e-112">Récupère un objet de [sélection](playlist-object.md) représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour le DVD.</span><span class="sxs-lookup"><span data-stu-id="ae39e-112">Retrieves a [Playlist](playlist-object.md) object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span> |



 

<span data-ttu-id="ae39e-113">L’objet **cdrom** prend en charge la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="ae39e-113">The **Cdrom** object supports the following method.</span></span>



| <span data-ttu-id="ae39e-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="ae39e-114">Method</span></span>                   | <span data-ttu-id="ae39e-115">Description</span><span class="sxs-lookup"><span data-stu-id="ae39e-115">Description</span></span>                          |
|--------------------------|--------------------------------------|
| [<span data-ttu-id="ae39e-116">émission</span><span class="sxs-lookup"><span data-stu-id="ae39e-116">eject</span></span>](cdrom-eject.md) | <span data-ttu-id="ae39e-117">Éjecte le CD ou DVD du lecteur.</span><span class="sxs-lookup"><span data-stu-id="ae39e-117">Ejects the CD or DVD from the drive.</span></span> |



 

<span data-ttu-id="ae39e-118">L’objet **cdrom** est accessible via la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="ae39e-118">The **Cdrom** object is accessed through the following method.</span></span>



| <span data-ttu-id="ae39e-119">Object</span><span class="sxs-lookup"><span data-stu-id="ae39e-119">Object</span></span>                                        | <span data-ttu-id="ae39e-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="ae39e-120">Method</span></span>                           |
|-----------------------------------------------|----------------------------------|
| [<span data-ttu-id="ae39e-121">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="ae39e-121">CdromCollection</span></span>](cdromcollection-object.md) | [<span data-ttu-id="ae39e-122">item</span><span class="sxs-lookup"><span data-stu-id="ae39e-122">item</span></span>](cdromcollection-item.md) |



 

<span data-ttu-id="ae39e-123">À des fins d’illustration, Player. cdromCollection. Item (*index*) est utilisé dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="ae39e-123">For purposes of illustration, player.cdromCollection.item(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae39e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae39e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae39e-125">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="ae39e-125">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




