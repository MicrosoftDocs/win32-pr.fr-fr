---
title: États des objets
description: États des objets
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511206"
---
# <a name="object-states"></a><span data-ttu-id="e51b0-103">États des objets</span><span class="sxs-lookup"><span data-stu-id="e51b0-103">Object States</span></span>

<span data-ttu-id="e51b0-104">Un objet composé existe dans l’un des trois États suivants : passif, chargé ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e51b0-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="e51b0-105">L’état d’un objet de document composé décrit la relation entre l’objet dans son conteneur et l’application responsable de sa création.</span><span class="sxs-lookup"><span data-stu-id="e51b0-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="e51b0-106">Le tableau suivant récapitule ces États.</span><span class="sxs-lookup"><span data-stu-id="e51b0-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="e51b0-107">État de l’objet</span><span class="sxs-lookup"><span data-stu-id="e51b0-107">Object state</span></span>       | <span data-ttu-id="e51b0-108">Description</span><span class="sxs-lookup"><span data-stu-id="e51b0-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51b0-109">Passif</span><span class="sxs-lookup"><span data-stu-id="e51b0-109">Passive</span></span><br/> | <span data-ttu-id="e51b0-110">L’objet composé-document existe uniquement dans le stockage, soit sur le disque soit dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="e51b0-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="e51b0-111">Dans cet État, l’objet n’est pas disponible pour l’affichage ou la modification.</span><span class="sxs-lookup"><span data-stu-id="e51b0-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="e51b0-112">Loaded</span><span class="sxs-lookup"><span data-stu-id="e51b0-112">Loaded</span></span><br/>  | <span data-ttu-id="e51b0-113">Les structures de données de l’objet créées par le gestionnaire d’objets se trouvent dans la mémoire du conteneur.</span><span class="sxs-lookup"><span data-stu-id="e51b0-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="e51b0-114">Le conteneur a établi la communication avec le gestionnaire d’objets et des données de présentation mises en cache sont disponibles pour le rendu de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e51b0-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="e51b0-115">Les appels sont traités par le gestionnaire d’objets.</span><span class="sxs-lookup"><span data-stu-id="e51b0-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="e51b0-116">Cet État, en raison de sa faible surcharge, est utilisé lorsqu’un utilisateur affiche ou imprime simplement un objet.</span><span class="sxs-lookup"><span data-stu-id="e51b0-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="e51b0-117">En cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="e51b0-117">Running</span></span><br/> | <span data-ttu-id="e51b0-118">Les objets qui contrôlent la communication à distance ont été créés et l’application serveur OLE est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e51b0-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="e51b0-119">Les interfaces de l’objet sont accessibles et le conteneur peut recevoir la notification des modifications.</span><span class="sxs-lookup"><span data-stu-id="e51b0-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="e51b0-120">Dans cet État, un utilisateur final peut modifier ou manipuler l’objet.</span><span class="sxs-lookup"><span data-stu-id="e51b0-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="e51b0-121">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e51b0-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e51b0-122">Passage à l’État chargé</span><span class="sxs-lookup"><span data-stu-id="e51b0-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="e51b0-123">Passage à l’État en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="e51b0-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="e51b0-124">Passage à l’état passif</span><span class="sxs-lookup"><span data-stu-id="e51b0-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="e51b0-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e51b0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e51b0-126">Documents composés</span><span class="sxs-lookup"><span data-stu-id="e51b0-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





