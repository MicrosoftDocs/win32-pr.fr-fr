---
description: Lors de l’utilisation du service d’événements COM+, vous pouvez prendre des mesures pour vous assurer que les informations sensibles contenues dans un événement ne sont pas compromises.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Considérations sur la sécurité des événements COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950877"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="b3eb4-103">Considérations sur la sécurité des événements COM+</span><span class="sxs-lookup"><span data-stu-id="b3eb4-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="b3eb4-104">Lors de l’utilisation du service d’événements COM+, vous pouvez prendre des mesures pour vous assurer que les informations sensibles contenues dans un événement ne sont pas compromises.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="b3eb4-105">Les éditeurs d’événements doivent garder à l’esprit que toute partie pouvant écrire dans votre catalogue COM+ peut s’abonner à vos événements.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="b3eb4-106">Par conséquent, si les informations contenues dans un objet de classe d’événements sont sensibles, vous devez utiliser l’outil d’administration Services de composants pour vérifier que les communications avec les abonnés sont chiffrées pour l’application qui contient les composants de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="b3eb4-107">(Sous l’onglet **sécurité** de la feuille de propriétés de l’application com+, sélectionnez **confidentialité du paquet** comme **niveau d’authentification pour les appels** .) En outre, vous devez utiliser des [filtres d’événements](filtering-events-in-com-.md) pour vous assurer que les événements sont remis uniquement aux abonnés appropriés.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="b3eb4-108">Les abonnés aux événements doivent garder à l’esprit qu’un tiers malveillant disposant d’un accès à votre réseau et de la connaissance de votre objet de classe d’événements pourrait créer des événements faux.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="b3eb4-109">Vous devez donc utiliser la [sécurité basée sur les rôles](role-based-security-administration.md) pour vous assurer que les appelants des méthodes de votre objet de classe d’événements disposent des informations d’identification appropriées pour effectuer les actions décrites dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="b3eb4-110">Pour aider à protéger les serveurs de publication et les abonnés, utilisez le service événements COM+ sur un réseau privé d’hôtes approuvés isolé d’Internet par un pare-feu.</span><span class="sxs-lookup"><span data-stu-id="b3eb4-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3eb4-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3eb4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3eb4-112">Sécurité COM+</span><span class="sxs-lookup"><span data-stu-id="b3eb4-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="b3eb4-113">Filtrage des événements dans COM+</span><span class="sxs-lookup"><span data-stu-id="b3eb4-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="b3eb4-114">Objet de classe d’événements COM+</span><span class="sxs-lookup"><span data-stu-id="b3eb4-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



