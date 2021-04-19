---
description: Solution de sécurité des familles Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Solution de sécurité des familles Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534131"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="4e772-103">Solution de sécurité des familles Windows</span><span class="sxs-lookup"><span data-stu-id="4e772-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="4e772-104">Les exigences clés définies par Microsoft pour une solution plus complète sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="4e772-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="4e772-105">Notez que la définition de Online est une technologie essentiellement accessible sur Internet, contrairement à un client hors connexion qui est généralement limité au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4e772-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="4e772-106">Fournissez une zone unique et facile à trouver dans l’interface utilisateur du système d’exploitation dans laquelle toutes les stratégies de contrôle parental, le contrôle de la surveillance des activités et les données d’activité d’une identité peuvent être facilement découvertes.</span><span class="sxs-lookup"><span data-stu-id="4e772-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="4e772-107">Prendre en charge la surveillance de l’activité suffisante de l’utilisateur contrôlé pour qu’un parent ou gardien ait une confiance raisonnable dans le cas où des activités à risque peuvent être découvertes.</span><span class="sxs-lookup"><span data-stu-id="4e772-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="4e772-108">Vous pouvez également reconfigurer la reconfiguration des stratégies de l’utilisateur contrôlé de sorte que les modifications non souhaitées ou non autorisées soient détectables.</span><span class="sxs-lookup"><span data-stu-id="4e772-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="4e772-109">Exposez les fonctionnalités d’analyse d’activité par le biais d’interfaces de journalisation des événements Windows Vista standard et fournissez une solution de visionneuse intégrée.</span><span class="sxs-lookup"><span data-stu-id="4e772-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="4e772-110">Définissez des événements d’activité standard et fournissez une extensibilité à la génération d’événements personnalisés par les éditeurs de logiciels indépendants.</span><span class="sxs-lookup"><span data-stu-id="4e772-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="4e772-111">Promouvez que toutes les analyses et restrictions pour un utilisateur sont activées uniquement sur la base d’un abonnement par les parents ou les gardiens.</span><span class="sxs-lookup"><span data-stu-id="4e772-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="4e772-112">Dans la mesure du possible, les fonctionnalités des restrictions doivent être complètement inactives pour que les utilisateurs non contrôlés réduisent les risques liés à la sécurité et à la compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="4e772-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="4e772-113">Chaque fois que cela est possible, Microsoft s’efforce de ne pas prendre de décisions de valeur par âge ou par d’autres paramètres pour l’utilisateur contrôlé (des tiers peuvent choisir de le faire).</span><span class="sxs-lookup"><span data-stu-id="4e772-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="4e772-114">Ces décisions sont laissées au parent ou au gardien, souvent influencées par les communautés ou les organisations.</span><span class="sxs-lookup"><span data-stu-id="4e772-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="4e772-115">Fournissez des implémentations dans le produit pour la surveillance de l’activité hors connexion et des restrictions où peu ou pas d’offres sont disponibles aujourd’hui, où la fonctionnalité de risque de sécurité associée est disponible dans le produit, ou lorsqu’une solution Microsoft fournit des fonctionnalités puissantes et robustes entièrement intégrées à la conception du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4e772-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="4e772-116">En règle générale, faites en sorte que les applications effectuent leurs propres journaux et restrictions pour un contexte et une expérience d’interface utilisateur optimaux.</span><span class="sxs-lookup"><span data-stu-id="4e772-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="4e772-117">Exception : fournir une surveillance des activités en ligne complète et des restrictions dans les domaines sélectionnés, où l’avantage pour les consommateurs et l’industrie l’emporte sur les coûts.</span><span class="sxs-lookup"><span data-stu-id="4e772-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="4e772-118">Exposez les paramètres d’interface utilisateur et les définitions d’événements d’activité des contrôles parentaux en utilisant des API publiques afin que des tiers puissent interroger l’État, modifier les paramètres et lire les journaux d’activité s’ils s’exécutent avec des privilèges de compte Windows suffisants.</span><span class="sxs-lookup"><span data-stu-id="4e772-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="4e772-119">L’objectif principal est de promouvoir la coexistence de solutions de contrôle parental tierces avec la fonctionnalité intégrée et de prendre en charge l’ajout de valeur en intégrant, en étendant ou en fournissant des fonctionnalités alternatives qui conviennent.</span><span class="sxs-lookup"><span data-stu-id="4e772-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



