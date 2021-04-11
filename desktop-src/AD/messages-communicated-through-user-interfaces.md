---
title: Messages communiqués par le biais des interfaces utilisateur
description: Cette rubrique répertorie les messages qu’un service d’annuaire peut envoyer à partir d’une interface utilisateur.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Messages communiqués par le biais des interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028604"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="a4565-104">Messages communiqués par le biais des interfaces utilisateur</span><span class="sxs-lookup"><span data-stu-id="a4565-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="a4565-105">Cette rubrique répertorie les messages qu’un service d’annuaire peut envoyer à partir d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a4565-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="a4565-106">Messages de page de requête communs</span><span class="sxs-lookup"><span data-stu-id="a4565-106">Common Query Page Messages</span></span>

<span data-ttu-id="a4565-107">Les messages suivants sont envoyés à une page d’extension de formulaire de requête du service d’annuaire dans la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :</span><span class="sxs-lookup"><span data-stu-id="a4565-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="a4565-108">**CQPM \_ CLEARFORM**</span><span class="sxs-lookup"><span data-stu-id="a4565-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="a4565-109">**CQPM \_ activer**</span><span class="sxs-lookup"><span data-stu-id="a4565-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="a4565-110">**CQPM \_ GETPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="a4565-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="a4565-111">**CQPM \_ HANDLERSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="a4565-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="a4565-112">**aide de CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="a4565-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="a4565-113">**initialisation de CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="a4565-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="a4565-114">**CQPM \_ persistant**</span><span class="sxs-lookup"><span data-stu-id="a4565-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="a4565-115">**version de CQPM \_**</span><span class="sxs-lookup"><span data-stu-id="a4565-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="a4565-116">**CQPM \_ SETDEFAULTPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="a4565-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="a4565-117">Messages divers</span><span class="sxs-lookup"><span data-stu-id="a4565-117">Miscellaneous Messages</span></span>

<span data-ttu-id="a4565-118">Le tableau suivant répertorie les messages qu’un service d’annuaire peut envoyer.</span><span class="sxs-lookup"><span data-stu-id="a4565-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="a4565-119">Message</span><span class="sxs-lookup"><span data-stu-id="a4565-119">Message</span></span>                  | <span data-ttu-id="a4565-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4565-120">Value</span></span>                     | <span data-ttu-id="a4565-121">Description</span><span class="sxs-lookup"><span data-stu-id="a4565-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4565-122">\_message ATTRCHANGED \_ DSPROP</span><span class="sxs-lookup"><span data-stu-id="a4565-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="a4565-123">"DsPropAttrChanged"</span><span class="sxs-lookup"><span data-stu-id="a4565-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="a4565-124">Message envoyé pour synchroniser les pages de propriétés et les outils d’administration de service d’annuaire, déclarés dans dsclient. h.</span><span class="sxs-lookup"><span data-stu-id="a4565-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="a4565-125">DSQPM \_ GETCLASSLIST</span><span class="sxs-lookup"><span data-stu-id="a4565-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="a4565-126">CQPM \_ HANDLERSPECIFIC + 0</span><span class="sxs-lookup"><span data-stu-id="a4565-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="a4565-127">Message de page envoyé aux pages de formulaire pour récupérer une liste de classes pour la requête, utilisé par le sélecteur de champ et la propriété bien pour générer sa liste de classes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="a4565-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="a4565-128">wParam = Flags et lParam = LPLPDSQUERYCLASSLIST, déclarés dans dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="a4565-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="a4565-129">DSQPM \_ HELPTOPICS</span><span class="sxs-lookup"><span data-stu-id="a4565-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="a4565-130">(CQPM \_ HANDLERSPECIFIC + 1)</span><span class="sxs-lookup"><span data-stu-id="a4565-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="a4565-131">Message de page envoyé aux pages de formulaire pour gérer la demande de « rubriques d’aide ».</span><span class="sxs-lookup"><span data-stu-id="a4565-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="a4565-132">wParam = 0, lParam = hWndParent, déclaré dans dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="a4565-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




