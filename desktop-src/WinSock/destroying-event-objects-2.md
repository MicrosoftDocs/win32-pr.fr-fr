---
description: Utilisation de WPUCloseEvent pour détruire un objet d’événement (application ou fournisseur de services) lorsque l’objet d’événement n’est plus nécessaire.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Destruction d’objets d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f0a17f623d0dd9ebceaf76b963ce72306000b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318393"
---
# <a name="destroying-event-objects"></a><span data-ttu-id="5afed-103">Destruction d’objets d’événement</span><span class="sxs-lookup"><span data-stu-id="5afed-103">Destroying Event Objects</span></span>

<span data-ttu-id="5afed-104">L’entité qui crée un objet d’événement (application ou fournisseur de services) est chargée de la détruire lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5afed-104">The entity that creates an event object (application or service provider) is responsible for destroying it when it is no longer required.</span></span> <span data-ttu-id="5afed-105">Les fournisseurs de services le font par le biais de **WPUCloseEvent**.</span><span class="sxs-lookup"><span data-stu-id="5afed-105">Service providers do this through **WPUCloseEvent**.</span></span>

 

 



