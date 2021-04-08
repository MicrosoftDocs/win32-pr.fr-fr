---
description: Pour que les abonnés puissent trouver une classe d’événements et s’y abonner, les classes d’événements doivent être inscrites dans le catalogue COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Inscription d’une classe d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748292"
---
# <a name="registering-an-event-class"></a><span data-ttu-id="b2976-103">Inscription d’une classe d’événements</span><span class="sxs-lookup"><span data-stu-id="b2976-103">Registering an Event Class</span></span>

<span data-ttu-id="b2976-104">Pour que les abonnés puissent trouver une classe d’événements et s’y abonner, les classes d’événements doivent être inscrites dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="b2976-104">So that subscribers can find an event class and subscribe to it, event classes must be registered in the COM+ catalog.</span></span> <span data-ttu-id="b2976-105">COM+ requiert une bibliothèque de types décrivant les interfaces et les méthodes d’événement afin qu’il puisse faire correspondre et connecter correctement les abonnés et les serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="b2976-105">COM+ requires a type library that describes the event interfaces and methods so that it can properly match and connect subscribers and publishers.</span></span> <span data-ttu-id="b2976-106">La bibliothèque de types doit résider dans ou être accompagnée d’une DLL d’inscription automatique.</span><span class="sxs-lookup"><span data-stu-id="b2976-106">The type library must reside in or be accompanied by a self-registering DLL.</span></span>

<span data-ttu-id="b2976-107">Vous pouvez utiliser l’outil d’administration Services de composants ou les fonctions d’administration COM+ pour inscrire une classe d’événements dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="b2976-107">You can use the Component Services administrative tool or the COM+ Administrative functions to register an event class in the COM+ catalog.</span></span>

<span data-ttu-id="b2976-108">**Pour inscrire une classe d’événements à l’aide de l’outil d’administration Services de composants**</span><span class="sxs-lookup"><span data-stu-id="b2976-108">**To register an event class with the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="b2976-109">Créer une application COM+.</span><span class="sxs-lookup"><span data-stu-id="b2976-109">Create a new COM+ application.</span></span>

2.  <span data-ttu-id="b2976-110">Ouvrez le dossier de l’application et sélectionnez **composants**.</span><span class="sxs-lookup"><span data-stu-id="b2976-110">Open the application folder and select **Components**.</span></span>

3.  <span data-ttu-id="b2976-111">Dans le menu **Action**, cliquez sur **Nouveau**.</span><span class="sxs-lookup"><span data-stu-id="b2976-111">On the **Action** menu, click **New**.</span></span> <span data-ttu-id="b2976-112">(Vous pouvez également sélectionner le dossier **composants** , cliquer avec le bouton droit, pointer sur **nouveau**, puis cliquer sur **composant**.)</span><span class="sxs-lookup"><span data-stu-id="b2976-112">(You can also select the **Components** folder, right-click, point to **New**, and then click **Component**.)</span></span>

4.  <span data-ttu-id="b2976-113">Cliquez sur **installer de nouvelles classes d’événements**.</span><span class="sxs-lookup"><span data-stu-id="b2976-113">Click **Install new event class(es)**.</span></span>

5.  <span data-ttu-id="b2976-114">Entrez le chemin d’accès à la DLL du composant de classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="b2976-114">Enter the path to the event class component DLL.</span></span>

6.  <span data-ttu-id="b2976-115">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2976-115">Click **OK**.</span></span>

<span data-ttu-id="b2976-116">La classe d’événements est enregistrée dans le catalogue COM+ et peut être localisée par les abonnés intéressés par l’obtention des informations fournies par la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="b2976-116">The event class is registered in the COM+ catalog and can be located by subscribers interested in obtaining the information provided by the event class.</span></span> <span data-ttu-id="b2976-117">Pour plus d’informations sur l’enregistrement de la classe d’événements à l’aide des interfaces d’administration COM+, consultez [**ICOMAdminCatalog :: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span><span class="sxs-lookup"><span data-stu-id="b2976-117">For information about how to register the event class by using the COM+ administrative interfaces, see [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2976-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2976-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2976-119">Inscription d’un abonnement</span><span class="sxs-lookup"><span data-stu-id="b2976-119">Registering a Subscription</span></span>](registering-a-subscription.md)
</dt> </dl>

 

 



