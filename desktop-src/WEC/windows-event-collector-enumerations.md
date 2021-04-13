---
title: Énumérations du collecteur d’événements Windows
description: Le tableau suivant répertorie les énumérations du kit de développement logiciel (SDK) du collecteur d’événements Windows.
ms.assetid: 3775aa7c-ef35-4534-b709-15624fd7a90d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d2617c6eb0052ec1ac41d5f197d9216c253054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380032"
---
# <a name="windows-event-collector-enumerations"></a><span data-ttu-id="cdc7f-103">Énumérations du collecteur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="cdc7f-103">Windows Event Collector Enumerations</span></span>

<span data-ttu-id="cdc7f-104">Le tableau suivant répertorie les énumérations du kit de développement logiciel (SDK) du collecteur d’événements Windows.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-104">The following table lists the enumerations of the Windows Event Collector SDK.</span></span>



| <span data-ttu-id="cdc7f-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="cdc7f-105">Enumeration</span></span>                                                                                               | <span data-ttu-id="cdc7f-106">Description</span><span class="sxs-lookup"><span data-stu-id="cdc7f-106">Description</span></span>                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdc7f-107">**\_mode de configuration des abonnements EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-107">**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)                       | <span data-ttu-id="cdc7f-108">Spécifie différents modes de configuration qui modifient les paramètres par défaut d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-108">Specifies different configuration modes that change the default settings for a subscription.</span></span>                                            |
| [<span data-ttu-id="cdc7f-109">**FORMAT du contenu de l' \_ abonnement EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-109">**EC\_SUBSCRIPTION\_CONTENT\_FORMAT**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_content_format)                               | <span data-ttu-id="cdc7f-110">Spécifie la manière dont les événements sont rendus sur l’ordinateur qui envoie les événements avant que les événements ne soient envoyés à l’ordinateur du collecteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-110">Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.</span></span> |
| [<span data-ttu-id="cdc7f-111">**\_ \_ type d’informations d’identification de l’abonnement EC \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-111">**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)                           | <span data-ttu-id="cdc7f-112">Spécifie le type d’informations d’identification à utiliser lors de la communication avec les sources d’événements.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-112">Specifies the type of credentials to use when communicating with event sources.</span></span>                                                         |
| [<span data-ttu-id="cdc7f-113">**\_mode de remise des abonnements EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-113">**EC\_SUBSCRIPTION\_DELIVERY\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_delivery_mode)                                 | <span data-ttu-id="cdc7f-114">Spécifie la manière dont les événements sont remis via un abonnement aux événements (à l’aide d’un modèle push ou pull).</span><span class="sxs-lookup"><span data-stu-id="cdc7f-114">Specifies how events are delivered through an event subscription (using a push or pull model).</span></span>                                          |
| [<span data-ttu-id="cdc7f-115">**ID de propriété de l' \_ abonnement EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-115">**EC\_SUBSCRIPTION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)                                     | <span data-ttu-id="cdc7f-116">Définit des valeurs pour identifier les propriétés d’abonnement aux événements utilisées pour la configuration de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-116">Defines values to identify event subscription properties used for subscription configuration.</span></span>                                           |
| [<span data-ttu-id="cdc7f-117">**\_ \_ \_ \_ \_ état actif de l’état d’exécution de l’abonnement EC**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-117">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_ACTIVE\_STATUS**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_active_status) | <span data-ttu-id="cdc7f-118">Spécifie l’état d’un abonnement ou d’une source d’événement par rapport à un abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-118">Specifies the status of a subscription or an event source with respect to a subscription.</span></span>                                               |
| [<span data-ttu-id="cdc7f-119">**\_ID d' \_ \_ \_ informations sur l’état d’exécution \_ de l’abonnement EC**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-119">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id)             | <span data-ttu-id="cdc7f-120">Spécifie une valeur qui identifie une propriété de l’état d’exécution d’une source d’événements ou d’un abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-120">Specifies a value that identifies a property of the runtime status of an event source or a subscription.</span></span>                                |
| [<span data-ttu-id="cdc7f-121">**\_type d’abonnement EC \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-121">**EC\_SUBSCRIPTION\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_type)                                                    | <span data-ttu-id="cdc7f-122">Spécifie le type d’abonnement à utiliser (un abonnement initié par une source ou un collecteur initié).</span><span class="sxs-lookup"><span data-stu-id="cdc7f-122">Specifies the type of subscription to use (a source initiated or collector initiated subscription).</span></span>                                     |
| [<span data-ttu-id="cdc7f-123">**\_type de variante EC \_**</span><span class="sxs-lookup"><span data-stu-id="cdc7f-123">**EC\_VARIANT\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_variant_type)                                                              | <span data-ttu-id="cdc7f-124">Définit les valeurs qui spécifient les types de données utilisés dans les fonctions du collecteur d’événements Windows.</span><span class="sxs-lookup"><span data-stu-id="cdc7f-124">Defines the values that specify the data types that are used in the Windows Event Collector functions.</span></span>                                  |



 

 

 




