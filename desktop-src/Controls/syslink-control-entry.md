---
title: SysLink
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles SysLink.
ms.assetid: 13a7b6d0-4bf1-480f-b447-838a550a5866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9bbfaea9b86c2d8dc42c84d050e5bec997ceb18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939804"
---
# <a name="syslink"></a><span data-ttu-id="5dd0a-103">SysLink</span><span class="sxs-lookup"><span data-stu-id="5dd0a-103">SysLink</span></span>

<span data-ttu-id="5dd0a-104">Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles SysLink.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-104">This section contains information about the programming elements used with SysLink controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="5dd0a-105">Vues d'ensemble</span><span class="sxs-lookup"><span data-stu-id="5dd0a-105">Overviews</span></span>



| <span data-ttu-id="5dd0a-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5dd0a-106">Topic</span></span>                                    | <span data-ttu-id="5dd0a-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="5dd0a-107">Contents</span></span>                                                                                       |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dd0a-108">Contrôle SysLink</span><span class="sxs-lookup"><span data-stu-id="5dd0a-108">SysLink Controls</span></span>](syslink-overview.md) | <span data-ttu-id="5dd0a-109">Le contrôle SysLink offre un moyen pratique d’incorporer des liens hypertexte dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-109">The SysLink control provides a convenient way to embed hypertext links in a window.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="5dd0a-110">Messages</span><span class="sxs-lookup"><span data-stu-id="5dd0a-110">Messages</span></span>



| <span data-ttu-id="5dd0a-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5dd0a-111">Topic</span></span>                                           | <span data-ttu-id="5dd0a-112">Contenu</span><span class="sxs-lookup"><span data-stu-id="5dd0a-112">Contents</span></span>                                                                             |
|-------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dd0a-113">**\_GETIDEALHEIGHT LM**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-113">**LM\_GETIDEALHEIGHT**</span></span>](lm-getidealheight.md) | <span data-ttu-id="5dd0a-114">Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-114">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="5dd0a-115">**\_GETIDEALSIZE LM**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-115">**LM\_GETIDEALSIZE**</span></span>](lm-getidealsize.md)     | <span data-ttu-id="5dd0a-116">Récupère la hauteur par défaut d’un lien pour la largeur actuelle du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-116">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="5dd0a-117">**LM \_ GETITEM**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-117">**LM\_GETITEM**</span></span>](lm-getitem.md)               | <span data-ttu-id="5dd0a-118">Récupère les États et les attributs d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-118">Retrieves the states and attributes of an item.</span></span><br/>                           |
| [<span data-ttu-id="5dd0a-119">**LANMANAGER \_ HITTEST**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-119">**LM\_HITTEST**</span></span>](lm-hittest.md)               | <span data-ttu-id="5dd0a-120">Détermine si l’utilisateur a cliqué sur le lien spécifié.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-120">Determines whether the user clicked the specified link.</span></span><br/>                   |
| [<span data-ttu-id="5dd0a-121">**\_SETITEM LM**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-121">**LM\_SETITEM**</span></span>](lm-setitem.md)               | <span data-ttu-id="5dd0a-122">Définit les États et les attributs d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-122">Sets the states and attributes of an item.</span></span><br/>                                |



 

### <a name="structures"></a><span data-ttu-id="5dd0a-123">Structures</span><span class="sxs-lookup"><span data-stu-id="5dd0a-123">Structures</span></span>



| <span data-ttu-id="5dd0a-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5dd0a-124">Topic</span></span>                                | <span data-ttu-id="5dd0a-125">Contenu</span><span class="sxs-lookup"><span data-stu-id="5dd0a-125">Contents</span></span>                                                                                                                                                                           |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dd0a-126">**LHITTESTINFO**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-126">**LHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lhittestinfo) | <span data-ttu-id="5dd0a-127">Utilisé pour obtenir des informations sur le lien correspondant à un emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-127">Used to get information about the link corresponding to a given location.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="5dd0a-128">**LITEM**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-128">**LITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-litem)               | <span data-ttu-id="5dd0a-129">Utilisé pour définir et récupérer des informations sur un élément de lien.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-129">Used to set and retrieve information about a link item.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="5dd0a-130">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="5dd0a-130">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)             | <span data-ttu-id="5dd0a-131">[**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) contient des informations de notification.</span><span class="sxs-lookup"><span data-stu-id="5dd0a-131">The [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) Contains notification information.</span></span> <span data-ttu-id="5dd0a-132">Envoie cette structure avec les messages de [ \_ retour](nm-return.md) par [ \_ un clic ou un NM NM](nm-click-syslink.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd0a-132">Send this structure with the [NM\_CLICK](nm-click-syslink.md) or [NM\_RETURN](nm-return.md) messages.</span></span><br/> |



 

 

 





