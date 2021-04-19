---
description: Dans la téléphonie Microsoft, les fournisseurs de services de téléphonie s’exécutent dans un processus distinct des applications de téléphonie.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Interface DLL de l’interface utilisateur du fournisseur de services de téléphonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544848"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="45588-103">Interface DLL de l’interface utilisateur du fournisseur de services de téléphonie</span><span class="sxs-lookup"><span data-stu-id="45588-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="45588-104">Dans la téléphonie Microsoft, les fournisseurs de services de téléphonie s’exécutent dans un processus distinct des applications de téléphonie.</span><span class="sxs-lookup"><span data-stu-id="45588-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="45588-105">Les fournisseurs de services communiquent avec TAPISRV via l’interface TSPI (Telephony Service Provider Interface) et s’exécutent dans son processus. interface d’applications vers TAPI, qui sont chargées dans le contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="45588-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="45588-106">Les composants de l’interface TAPI utilisent différents mécanismes de communication interprocessus pour acheminer les demandes de fonction et les messages entre les applications et les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="45588-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="45588-107">Les applications et les fournisseurs de services peuvent s’exécuter non seulement dans des processus distincts, mais aussi sur des systèmes complètement distincts.</span><span class="sxs-lookup"><span data-stu-id="45588-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="45588-108">Par conséquent, les fournisseurs de services ne peuvent pas afficher de boîtes de dialogue dans le processus, ni même sur l’ordinateur sur lequel ils s’exécutent. L’interface utilisateur doit être appelée à partir du contexte de l’application, sur l’ordinateur sur lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="45588-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="45588-109">Cette section définit le mécanisme par lequel les fonctions d’interface utilisateur du fournisseur de services sont chargées et appelées dans le contexte de l’application.</span><span class="sxs-lookup"><span data-stu-id="45588-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="45588-110">Un mécanisme est également défini par les fournisseurs de services qui peuvent ouvrir spontanément des boîtes de dialogue dans le contexte de l’application lorsque celles-ci ne seraient normalement pas attendues par l’application.</span><span class="sxs-lookup"><span data-stu-id="45588-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="45588-111">C’est le cas, par exemple, de la boîte de dialogue **parler/raccrocher** qui est affichée par un fournisseur de services de modem de données lorsque le modem est utilisé en tant que numéroteur pour les appels vocaux interactifs, et l’utilisateur doit être invité à prendre le téléphone et à informer le fournisseur de services quand il doit placer le OnHook du modem.</span><span class="sxs-lookup"><span data-stu-id="45588-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



