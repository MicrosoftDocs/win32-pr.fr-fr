---
title: Bonnes pratiques WinRM
description: Cette rubrique décrit quelques-unes des meilleures pratiques pour l’utilisation des différentes fonctionnalités de l’API WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941043"
---
# <a name="winrm-best-practices"></a><span data-ttu-id="0727a-103">Bonnes pratiques WinRM</span><span class="sxs-lookup"><span data-stu-id="0727a-103">WinRM Best Practices</span></span>

<span data-ttu-id="0727a-104">Cette rubrique décrit quelques-unes des meilleures pratiques pour l’utilisation des différentes fonctionnalités de l’API WinRM.</span><span class="sxs-lookup"><span data-stu-id="0727a-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="0727a-105">Quotas</span><span class="sxs-lookup"><span data-stu-id="0727a-105">Quotas</span></span>

<span data-ttu-id="0727a-106">Lorsqu’un quota est atteint, le service WinRM retourne une erreur au client.</span><span class="sxs-lookup"><span data-stu-id="0727a-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="0727a-107">Par conséquent, la logique du client doit retenter explicitement l’opération en fonction de l’erreur retournée.</span><span class="sxs-lookup"><span data-stu-id="0727a-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="0727a-108">Abonnements à des événements</span><span class="sxs-lookup"><span data-stu-id="0727a-108">Event subscriptions</span></span>

<span data-ttu-id="0727a-109">Lorsque vous utilisez des abonnements déclenchés par le collecteur, limitez le nombre d’ordinateurs distants à 500 et isolez le service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) dans un processus hôte distinct.</span><span class="sxs-lookup"><span data-stu-id="0727a-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="0727a-110">Une erreur de connexion contiendra un thread jusqu’à ce qu’il expire. Un grand nombre d’erreurs de connexion simultanées peuvent entraîner l’épuisement du pool de threads et rendre le serveur sans réponse.</span><span class="sxs-lookup"><span data-stu-id="0727a-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 