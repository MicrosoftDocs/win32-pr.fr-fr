---
description: La région de mise à jour identifie la partie d’une fenêtre qui est obsolète ou non valide et qui doit être redessinée.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: La région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991769"
---
# <a name="the-update-region"></a><span data-ttu-id="e59f3-103">La région de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e59f3-103">The Update Region</span></span>

<span data-ttu-id="e59f3-104">La *région de mise à jour* identifie la partie d’une fenêtre qui est obsolète ou non valide et qui doit être redessinée.</span><span class="sxs-lookup"><span data-stu-id="e59f3-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="e59f3-105">Le système utilise la région de mise à jour pour générer des messages de [**\_ peinture WM**](wm-paint.md) pour les applications et réduire le temps que les applications consacrent à mettre à jour le contenu de leur Windows.</span><span class="sxs-lookup"><span data-stu-id="e59f3-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="e59f3-106">Le système ajoute uniquement la partie non valide de la fenêtre à la zone de mise à jour, ce qui requiert que cette partie soit dessinée uniquement.</span><span class="sxs-lookup"><span data-stu-id="e59f3-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="e59f3-107">Lorsque le système détermine qu’une fenêtre a besoin d’être mis à jour, il définit les dimensions de la région de mise à jour sur la partie non valide de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e59f3-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="e59f3-108">La définition de la région de mise à jour n’entraîne pas immédiatement le dessin de l’application.</span><span class="sxs-lookup"><span data-stu-id="e59f3-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="e59f3-109">Au lieu de cela, l’application continue de récupérer les messages de la file d’attente de messages d’application jusqu’à ce qu’aucun message ne soit conservé.</span><span class="sxs-lookup"><span data-stu-id="e59f3-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="e59f3-110">Le système vérifie ensuite la région de mise à jour et, si la région n’est pas vide (non NULL), elle envoie un message de [**\_ peinture WM**](wm-paint.md) à la procédure de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e59f3-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="e59f3-111">Une application peut utiliser la région de mise à jour pour générer ses messages de [**\_ peinture WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="e59f3-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="e59f3-112">Par exemple, une application qui charge des données à partir de fichiers ouverts définit généralement la région de mise à jour lors du chargement afin que les nouvelles données soient dessinées lors du traitement du message **WM de \_ peinture** suivant.</span><span class="sxs-lookup"><span data-stu-id="e59f3-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="e59f3-113">En général, une application ne doit pas être dessinée au moment où ses données changent, mais acheminer toutes les opérations de dessin via le message de **\_ peinture WM** .</span><span class="sxs-lookup"><span data-stu-id="e59f3-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



