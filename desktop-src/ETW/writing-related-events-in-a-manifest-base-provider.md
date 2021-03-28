---
description: Utilisez la fonction EventWriteTransfer lorsque plusieurs composants veulent associer leurs événements dans un scénario de suivi de bout en bout.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Écriture d’événements connexes dans un fournisseur basé sur un manifeste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527280"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="55c22-103">Écriture d’événements connexes dans un fournisseur basé sur un manifeste</span><span class="sxs-lookup"><span data-stu-id="55c22-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="55c22-104">Utilisez la fonction [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) lorsque plusieurs composants veulent associer leurs événements dans un scénario de suivi de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="55c22-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="55c22-105">Par exemple, les composants A, B et C effectuent des tâches sur une activité associée et veulent lier tous les événements associés à cette activité.</span><span class="sxs-lookup"><span data-stu-id="55c22-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="55c22-106">ETW utilise le stockage local des threads pour rendre l’identificateur d’activité du composant précédent disponible pour le composant suivant.</span><span class="sxs-lookup"><span data-stu-id="55c22-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="55c22-107">Le composant récupère l’identificateur du composant précédent à partir du stockage local et lui affecte l’identificateur d’activité associé.</span><span class="sxs-lookup"><span data-stu-id="55c22-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="55c22-108">Le consommateur peut ensuite utiliser l’identificateur d’activité associé pour parcourir la chaîne des événements d’un composant à l’autre.</span><span class="sxs-lookup"><span data-stu-id="55c22-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



