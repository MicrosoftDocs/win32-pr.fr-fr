---
title: Architecture (Text Services Framework)
description: Architecture
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Text Services Framework (TSF), architecture
- TSF (Text Services Framework), architecture
- services de texte, architecture
- Applications compatibles TSF, architecture
- Text Services Framework (TSF), composants
- TSF (Text Services Framework), composants
- services de texte, composants
- Applications compatibles TSF, composants
- Text Services Framework (TSF), applications
- TSF (Text Services Framework), applications
- services de texte, applications
- Applications compatibles TSF, à propos de
- Text Services Framework (TSF), text services
- TSF (Text Services Framework), services de texte
- services de texte, à propos de
- Applications compatibles TSF, services de texte
- Text Services Framework (TSF), gestionnaire TSF
- TSF (Text Services Framework), gestionnaire TSF
- services de texte, gestionnaire TSF
- Applications compatibles TSF, gestionnaire TSF
- Gestionnaire TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104567140"
---
# <a name="architecture-text-services-framework"></a><span data-ttu-id="51f29-124">Architecture (Text Services Framework)</span><span class="sxs-lookup"><span data-stu-id="51f29-124">Architecture (Text Services Framework)</span></span>

<span data-ttu-id="51f29-125">Text Services Framework comprend trois composants principaux :</span><span class="sxs-lookup"><span data-stu-id="51f29-125">Text Services Framework includes three primary components:</span></span>

-   <span data-ttu-id="51f29-126">**Applications :** Les opérations d’application incluent généralement l’affichage, la modification directe et le stockage de texte.</span><span class="sxs-lookup"><span data-stu-id="51f29-126">**Applications:** Application operations typically include display, direct editing, and storage of text.</span></span> <span data-ttu-id="51f29-127">Une application fournit l’accès au texte en implémentant un serveur COM qui prend en charge certaines interfaces et communique avec TSF à l’aide des interfaces exposées par le gestionnaire TSF.</span><span class="sxs-lookup"><span data-stu-id="51f29-127">An application provides access to text by implementing a COM server that supports certain interfaces and communicates with TSF using interfaces that the TSF manager exposes.</span></span> <span data-ttu-id="51f29-128">Tout au long de cette documentation, le terme, application, fait référence à une application compatible TSF, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="51f29-128">Throughout this documentation, the term, application, refers to a TSF-enabled application, unless otherwise specified.</span></span>
-   <span data-ttu-id="51f29-129">**Services de texte :** Un service de texte fonctionne comme un fournisseur de texte pour une application.</span><span class="sxs-lookup"><span data-stu-id="51f29-129">**Text Services:** A text service functions as a text provider to an application.</span></span> <span data-ttu-id="51f29-130">Un service de texte peut obtenir du texte à partir d’une application, et écrire du texte dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="51f29-130">A text service can obtain text from, and write text to, an application.</span></span> <span data-ttu-id="51f29-131">Un service de texte peut également associer des données et des propriétés à un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="51f29-131">A text service can also associate data and properties with a block of text.</span></span> <span data-ttu-id="51f29-132">Un service de texte est implémenté en tant que serveur COM in-proc qui s’inscrit auprès de TSF.</span><span class="sxs-lookup"><span data-stu-id="51f29-132">A text service is implemented as a COM in-proc server that registers itself with TSF.</span></span> <span data-ttu-id="51f29-133">Une fois inscrit, l’utilisateur interagit avec le service de texte à l’aide de la barre de langue ou des raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="51f29-133">When registered, the user interacts with the text service using the language bar or keyboard shortcuts.</span></span> <span data-ttu-id="51f29-134">Plusieurs services de texte peuvent être installés.</span><span class="sxs-lookup"><span data-stu-id="51f29-134">Multiple text services can be installed.</span></span>
-   <span data-ttu-id="51f29-135">**Gestionnaire TSF :** Le gestionnaire TSF fonctionne comme médiateur entre une application et un ou plusieurs services de texte.</span><span class="sxs-lookup"><span data-stu-id="51f29-135">**TSF Manager:** The TSF manager functions as a mediator between an application and one or more text services.</span></span> <span data-ttu-id="51f29-136">Un service de texte n’interagit jamais directement avec une application.</span><span class="sxs-lookup"><span data-stu-id="51f29-136">A text service never interacts directly with an application.</span></span> <span data-ttu-id="51f29-137">Toutes les communications passent par le gestionnaire TSF.</span><span class="sxs-lookup"><span data-stu-id="51f29-137">All communication passes through the TSF manager.</span></span> <span data-ttu-id="51f29-138">Le gestionnaire TSF est implémenté par le système d’exploitation et ne peut pas être remplacé.</span><span class="sxs-lookup"><span data-stu-id="51f29-138">The TSF manager is implemented by the operating system and cannot be replaced.</span></span> <span data-ttu-id="51f29-139">Dans cette documentation, le terme, Manager, fait référence au gestionnaire TSF, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="51f29-139">Throughout this documentation, the term, manager, refers to the TSF manager, unless otherwise specified.</span></span>

<span data-ttu-id="51f29-140">L’illustration suivante montre les principaux éléments architecturaux de TSF.</span><span class="sxs-lookup"><span data-stu-id="51f29-140">The following illustration shows the primary architectural elements of TSF.</span></span>

![architecture de l’infrastructure de services de texte](images/tsf-arch.gif)

<span data-ttu-id="51f29-142">Avec cette architecture, le gestionnaire TSF fournit une couche d’abstraction entre les applications et les services de texte.</span><span class="sxs-lookup"><span data-stu-id="51f29-142">With this architecture, the TSF manager provides an abstraction layer between applications and text services.</span></span> <span data-ttu-id="51f29-143">Cette couche d’abstraction permet à une application et à un ou plusieurs services de texte de partager du texte, et elle permet au gestionnaire TSF de gérer les services de texte.</span><span class="sxs-lookup"><span data-stu-id="51f29-143">This abstraction layer enables an application and one or more text services to share text, and it enables the TSF manager to manage text services.</span></span>

 

 




