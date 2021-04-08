---
description: Le fournisseur de Registre système tente d’envoyer une notification pour chaque événement qui se produit.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Réception d’événements de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034257"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="69bcc-103">Réception d’événements de Registre</span><span class="sxs-lookup"><span data-stu-id="69bcc-103">Receiving Registry Events</span></span>

<span data-ttu-id="69bcc-104">Le fournisseur de Registre système tente d’envoyer une notification pour chaque événement qui se produit.</span><span class="sxs-lookup"><span data-stu-id="69bcc-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="69bcc-105">Toutefois, le fournisseur de Registre système ne garantit pas que le consommateur recevra un ou tous les événements.</span><span class="sxs-lookup"><span data-stu-id="69bcc-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="69bcc-106">L’exception est que le fournisseur de Registre système s’assure qu’un consommateur recevra une notification pour chaque inscription d’événement.</span><span class="sxs-lookup"><span data-stu-id="69bcc-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="69bcc-107">Par exemple, supposons qu’un consommateur s’inscrit pour deux événements de changement d’arborescence, en demandant une notification pour les instances [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) .</span><span class="sxs-lookup"><span data-stu-id="69bcc-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="69bcc-108">Chaque inscription a la même valeur Hive (sous-arborescence) mais une valeur RootPath différente.</span><span class="sxs-lookup"><span data-stu-id="69bcc-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="69bcc-109">Si les clés des deux chemins changent plusieurs fois, le fournisseur de Registre système garantit que le consommateur recevra une notification pour chaque chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="69bcc-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="69bcc-110">En fonction du temps de réponse du Registre et du fournisseur de Registre système, le consommateur peut recevoir autant de notifications qu’il y avait d’occurrences d’événements.</span><span class="sxs-lookup"><span data-stu-id="69bcc-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69bcc-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69bcc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69bcc-112">Inscription pour les événements du Registre système</span><span class="sxs-lookup"><span data-stu-id="69bcc-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
