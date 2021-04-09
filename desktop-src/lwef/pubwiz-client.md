---
title: Conception de Client-Side
description: Le script des pages HTML côté serveur communique avec le client de l’Assistant commande d’impression en ligne dans lequel il est hébergé. Cette communication s’effectue par le biais de méthodes et de propriétés accessibles par l’objet Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- assistants de publication, conception côté client
- Window. external, assistants de publication
- assistants de publication, Window. external
- assistants de publication, considérations relatives à la conception
- assistants de publication, Assistant commande d’impression en ligne
- Assistant commande d’impression en ligne, conception côté client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940967"
---
# <a name="client-side-design"></a><span data-ttu-id="0b88d-110">Conception de Client-Side</span><span class="sxs-lookup"><span data-stu-id="0b88d-110">Client-Side Design</span></span>

<span data-ttu-id="0b88d-111">Le script des pages HTML côté serveur communique avec le client de l’Assistant commande d’impression en ligne dans lequel il est hébergé.</span><span class="sxs-lookup"><span data-stu-id="0b88d-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="0b88d-112">Cette communication s’effectue par le biais de méthodes et de propriétés accessibles par l’objet **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="0b88d-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="0b88d-113">Les rubriques suivantes sont traitées dans ce document.</span><span class="sxs-lookup"><span data-stu-id="0b88d-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="0b88d-114">Méthodes et propriétés</span><span class="sxs-lookup"><span data-stu-id="0b88d-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="0b88d-115">Remarques sur la conception</span><span class="sxs-lookup"><span data-stu-id="0b88d-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="0b88d-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b88d-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="0b88d-117">Méthodes et propriétés</span><span class="sxs-lookup"><span data-stu-id="0b88d-117">Methods and Properties</span></span>

<span data-ttu-id="0b88d-118">Les méthodes et propriétés suivantes sont disponibles via l’objet **Window. external** .</span><span class="sxs-lookup"><span data-stu-id="0b88d-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="0b88d-119">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="0b88d-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="0b88d-120">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="0b88d-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="0b88d-121">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="0b88d-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="0b88d-122">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="0b88d-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="0b88d-123">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="0b88d-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="0b88d-124">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="0b88d-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="0b88d-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b88d-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="0b88d-126">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="0b88d-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="0b88d-127">Le script de la page côté serveur appelle ces méthodes pour notifier le client des événements au cours de la procédure de publication.</span><span class="sxs-lookup"><span data-stu-id="0b88d-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="0b88d-128">Prenons l’exemple de [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) .</span><span class="sxs-lookup"><span data-stu-id="0b88d-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="0b88d-129">Lorsque l’Assistant affiche la première page HTML côté serveur, il s’occupe de la connaissance des handles des pages d’Assistant précédentes et des pages HTML hébergées.</span><span class="sxs-lookup"><span data-stu-id="0b88d-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="0b88d-130">À ce stade de notre exemple, l’utilisateur, assis sur la première page HTML, clique sur le bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="0b88d-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="0b88d-131">L’Assistant envoie une notification de cet événement au serveur.</span><span class="sxs-lookup"><span data-stu-id="0b88d-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="0b88d-132">À la réception de ce message, le script côté serveur fait référence à son gestionnaire **OnBack** pour cet événement, qui, comme il s’agit de la première page HTML, appelle la méthode **FinalBack** .</span><span class="sxs-lookup"><span data-stu-id="0b88d-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="0b88d-133">L’Assistant accède alors à la page de l’Assistant affichée avant d’entrer dans l’interface utilisateur côté serveur.</span><span class="sxs-lookup"><span data-stu-id="0b88d-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="0b88d-134">Pour une description complète de ces méthodes et propriétés, consultez la documentation relative aux objets [**WebWizardHost**](/windows/desktop/shell/webwizardhost) et [**NewWDEvents**](/windows/desktop/shell/newwdevents) .</span><span class="sxs-lookup"><span data-stu-id="0b88d-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="0b88d-135">Remarques sur la conception</span><span class="sxs-lookup"><span data-stu-id="0b88d-135">Design Considerations</span></span>

<span data-ttu-id="0b88d-136">Le code HTML qui compose chaque page côté serveur s’affiche normalement dans le volet de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="0b88d-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="0b88d-137">Lorsque vous concevez ces pages, gardez à l’esprit qu’une fenêtre d’Assistant ne peut pas être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="0b88d-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="0b88d-138">Les pages doivent donc être construites et dimensionnées de sorte que les barres de défilement soient évitées chaque fois que possible pour fournir à l’utilisateur une navigation lisse dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="0b88d-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="0b88d-139">Chaque page HTML doit également fournir un gestionnaire pour les événements **OnBack**, **OnNext** et **OnCancel** .</span><span class="sxs-lookup"><span data-stu-id="0b88d-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="0b88d-140">Le gestionnaire **OnNext** gère également l’événement **Finish** .</span><span class="sxs-lookup"><span data-stu-id="0b88d-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="0b88d-141">Une page qui n’implémente pas une fonction **OnBack** n’est pas considérée comme non valide et entraîne l’affichage d’une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0b88d-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b88d-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b88d-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b88d-143">**WebWizardHost**</span><span class="sxs-lookup"><span data-stu-id="0b88d-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="0b88d-144">**NewWDEvents**</span><span class="sxs-lookup"><span data-stu-id="0b88d-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="0b88d-145">Conception côté serveur</span><span class="sxs-lookup"><span data-stu-id="0b88d-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 