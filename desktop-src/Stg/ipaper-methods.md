---
title: Méthodes IPaper
description: Fournit des objets de copapiers qui sont contrôlés principalement par leur interface IPaper native.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197316"
---
# <a name="ipaper-methods"></a><span data-ttu-id="65204-104">Méthodes IPaper</span><span class="sxs-lookup"><span data-stu-id="65204-104">IPaper Methods</span></span>

<span data-ttu-id="65204-105">**StoServe** fournit des objets de copapier contrôlés principalement par leur interface **IPaper** native.</span><span class="sxs-lookup"><span data-stu-id="65204-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="65204-106">Le tableau suivant répertorie les méthodes **IPaper** à partir de IPaper. H dans le \\ répertoire frère Inc.</span><span class="sxs-lookup"><span data-stu-id="65204-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="65204-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="65204-107">Method</span></span>    | <span data-ttu-id="65204-108">Description</span><span class="sxs-lookup"><span data-stu-id="65204-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="65204-109">InitPaper</span><span class="sxs-lookup"><span data-stu-id="65204-109">InitPaper</span></span> | <span data-ttu-id="65204-110">Initialise l’objet Paper et crée un tableau de données d’encre.</span><span class="sxs-lookup"><span data-stu-id="65204-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="65204-111">Verrouillage</span><span class="sxs-lookup"><span data-stu-id="65204-111">Lock</span></span>      | <span data-ttu-id="65204-112">Permet au client de contrôler le papier et de verrouiller les autres clients.</span><span class="sxs-lookup"><span data-stu-id="65204-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="65204-113">Déverrouiller</span><span class="sxs-lookup"><span data-stu-id="65204-113">Unlock</span></span>    | <span data-ttu-id="65204-114">Abandonne le contrôle client du papier.</span><span class="sxs-lookup"><span data-stu-id="65204-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="65204-115">Load</span><span class="sxs-lookup"><span data-stu-id="65204-115">Load</span></span>      | <span data-ttu-id="65204-116">Charge le contenu papier à partir du fichier composé du client et avertit les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="65204-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="65204-117">Enregistrer</span><span class="sxs-lookup"><span data-stu-id="65204-117">Save</span></span>      | <span data-ttu-id="65204-118">Enregistre le contenu du document dans le fichier composé du client.</span><span class="sxs-lookup"><span data-stu-id="65204-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="65204-119">InkStart</span><span class="sxs-lookup"><span data-stu-id="65204-119">InkStart</span></span>  | <span data-ttu-id="65204-120">Démarre le dessin de l’encre couleur sur l’aire du papier.</span><span class="sxs-lookup"><span data-stu-id="65204-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="65204-121">InkDraw</span><span class="sxs-lookup"><span data-stu-id="65204-121">InkDraw</span></span>   | <span data-ttu-id="65204-122">Place des points de données d’encre sur la surface du papier électronique.</span><span class="sxs-lookup"><span data-stu-id="65204-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="65204-123">InkStop</span><span class="sxs-lookup"><span data-stu-id="65204-123">InkStop</span></span>   | <span data-ttu-id="65204-124">Arrête le dessin manuscrit sur l’aire de papier.</span><span class="sxs-lookup"><span data-stu-id="65204-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="65204-125">Effacer</span><span class="sxs-lookup"><span data-stu-id="65204-125">Erase</span></span>     | <span data-ttu-id="65204-126">Effacer le contenu du document actuel et avertit les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="65204-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="65204-127">Redimensionner</span><span class="sxs-lookup"><span data-stu-id="65204-127">Resize</span></span>    | <span data-ttu-id="65204-128">Redimensionne la taille du rectangle de dessin du papier et notifie les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="65204-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="65204-129">Redessiner</span><span class="sxs-lookup"><span data-stu-id="65204-129">Redraw</span></span>    | <span data-ttu-id="65204-130">Redessine le contenu de l’objet Paper et avertit les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="65204-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="65204-131">Les méthodes intéressantes pour cet exemple de code sur les fichiers composés sont [**charger**](ipaper--load.md), [**Enregistrer**](ipaper--save.md)et [**redessiner**](ipaper--redraw.md).</span><span class="sxs-lookup"><span data-stu-id="65204-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="65204-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) sont des méthodes utilisées par les clients pour enregistrer les séquences de dessin de l’encre.</span><span class="sxs-lookup"><span data-stu-id="65204-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="65204-133">Le client répond généralement à un message WM \_ LBUTTONDOWN au début d’une séquence de dessin d’encre en appelant **InkStart** sur le codocument.</span><span class="sxs-lookup"><span data-stu-id="65204-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="65204-134">Lorsque l’utilisateur déplace la souris ou le stylet pour dessiner tout en maintenant le bouton gauche enfoncé, le client répond aux \_ messages WM MOUSEMOVE répétés avec les appels correspondants à **InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="65204-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="65204-135">Quand l’utilisateur relâche le bouton gauche de la souris, le client répond à un \_ message WM LBUTTONUP avec un appel à **InkStop**, qui marque la fin de la séquence de dessin de l’encre.</span><span class="sxs-lookup"><span data-stu-id="65204-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="65204-136">[**InkStart**](inkstart-method.md) indique au codocument la position de début de la séquence de dessin dans les coordonnées de la fenêtre cliente.</span><span class="sxs-lookup"><span data-stu-id="65204-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="65204-137">Il passe également la couleur et la largeur de l’encre actuellement sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="65204-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="65204-138">Le client gère ces sélections ; Le « colivre » les enregistre simplement lorsque l’appel **InkStart** est effectué.</span><span class="sxs-lookup"><span data-stu-id="65204-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="65204-139">[**InkDraw**](inkdraw-method.md) est appelé à plusieurs reprises pour indiquer au codocument la succession des coordonnées de la fenêtre qui représentent le mouvement de dessin de la souris ou du stylet.</span><span class="sxs-lookup"><span data-stu-id="65204-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="65204-140">[**InkStop**](cguipaper-methods.md) indique au codocument de marquer la fin d’une séquence de dessin.</span><span class="sxs-lookup"><span data-stu-id="65204-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




