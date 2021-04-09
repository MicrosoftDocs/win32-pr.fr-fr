---
title: Conception de Server-Side
description: Les fonctions côté serveur communiquent avec l’Assistant client via l’objet Windows. external. Le script côté serveur fournit ces fonctions pour répondre aux événements de l’Assistant et récupérer des informations sur l’Assistant.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- assistants de publication, conception côté serveur
- Window. external, assistants de publication
- assistants de publication, Window. external
- assistants de publication, fonctions de script de navigation
- scripts, assistants de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940997"
---
# <a name="server-side-design"></a><span data-ttu-id="35f5c-109">Conception de Server-Side</span><span class="sxs-lookup"><span data-stu-id="35f5c-109">Server-Side Design</span></span>

<span data-ttu-id="35f5c-110">Les fonctions côté serveur communiquent avec l’Assistant client via l’objet **Windows. external** .</span><span class="sxs-lookup"><span data-stu-id="35f5c-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="35f5c-111">Le script côté serveur fournit ces fonctions pour répondre aux événements de l’Assistant et récupérer des informations sur l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35f5c-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="35f5c-112">Les rubriques suivantes sont traitées dans ce document.</span><span class="sxs-lookup"><span data-stu-id="35f5c-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="35f5c-113">Implémentation de fonctions de script de navigation</span><span class="sxs-lookup"><span data-stu-id="35f5c-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="35f5c-114">OnBack()</span><span class="sxs-lookup"><span data-stu-id="35f5c-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="35f5c-115">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="35f5c-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="35f5c-116">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="35f5c-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="35f5c-117">Autres méthodes et propriétés</span><span class="sxs-lookup"><span data-stu-id="35f5c-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="35f5c-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35f5c-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="35f5c-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35f5c-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="35f5c-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35f5c-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="35f5c-121">Implémentation de fonctions de script de navigation</span><span class="sxs-lookup"><span data-stu-id="35f5c-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="35f5c-122">Le script côté serveur dans chaque page HTML répond aux boutons de navigation par le biais de fonctions pour **OnBack**, **OnNext** et **OnCancel**.</span><span class="sxs-lookup"><span data-stu-id="35f5c-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="35f5c-123">Ces fonctions doivent être accessibles via **IHTMLDocument :: obten \_ script** sur le client et ne prennent pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="35f5c-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="35f5c-124">OnBack()</span><span class="sxs-lookup"><span data-stu-id="35f5c-124">OnBack()</span></span>

-   <span data-ttu-id="35f5c-125">Répond lorsque l’utilisateur clique sur **précédent** dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35f5c-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="35f5c-126">Si la page côté serveur Active est la première page côté serveur, appelez **Window. external. FinalBack** pour indiquer au client d’accéder à la page précédente côté client.</span><span class="sxs-lookup"><span data-stu-id="35f5c-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="35f5c-127">Si la page côté serveur active n’est pas la première page côté serveur, accédez à la page précédente côté serveur.</span><span class="sxs-lookup"><span data-stu-id="35f5c-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="35f5c-128">Cette fonction doit être implémentée pour chaque page.</span><span class="sxs-lookup"><span data-stu-id="35f5c-128">This function must be implemented for each page.</span></span> <span data-ttu-id="35f5c-129">Toute page qui ne parvient pas à le faire est considérée comme non valide et affiche une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="35f5c-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="35f5c-130">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="35f5c-130">OnNext()</span></span>

-   <span data-ttu-id="35f5c-131">Répond quand l’utilisateur clique sur **suivant** dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35f5c-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="35f5c-132">Si la page côté serveur Active est la dernière page côté serveur, appelez **Window. external. FinalNext** pour indiquer au client d’accéder à la page suivante côté client ou de terminer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35f5c-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="35f5c-133">Si la page côté serveur active n’est pas la dernière page côté serveur, accédez à la page suivante côté serveur.</span><span class="sxs-lookup"><span data-stu-id="35f5c-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="35f5c-134">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="35f5c-134">OnCancel()</span></span>

-   <span data-ttu-id="35f5c-135">Répond quand l’utilisateur clique sur **Annuler** dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35f5c-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="35f5c-136">L’interface utilisateur doit être conçue pour permettre à l’utilisateur d’annuler à tout moment.</span><span class="sxs-lookup"><span data-stu-id="35f5c-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="35f5c-137">Une fois que le traitement de la fonction **OnCancel** est traité, le client ferme l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35f5c-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="35f5c-138">Autres méthodes et propriétés</span><span class="sxs-lookup"><span data-stu-id="35f5c-138">Other Methods and Properties</span></span>

<span data-ttu-id="35f5c-139">Les fonctions implémentées par le client sont accessibles via **Windows. external**, comme les propriétés.</span><span class="sxs-lookup"><span data-stu-id="35f5c-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="35f5c-140">Les services disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="35f5c-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="35f5c-141">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35f5c-141">Methods</span></span>

-   [<span data-ttu-id="35f5c-142">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="35f5c-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="35f5c-143">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="35f5c-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="35f5c-144">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="35f5c-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="35f5c-145">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35f5c-145">Properties</span></span>

-   <span data-ttu-id="35f5c-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35f5c-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="35f5c-147">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="35f5c-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="35f5c-148">L’exemple de code suivant montre le code côté serveur d’une page d’assistant simple qui implémente la page d’erreur du service Web.</span><span class="sxs-lookup"><span data-stu-id="35f5c-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="35f5c-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35f5c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35f5c-150">Conception côté client</span><span class="sxs-lookup"><span data-stu-id="35f5c-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="35f5c-151">Inscription d’un service</span><span class="sxs-lookup"><span data-stu-id="35f5c-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 