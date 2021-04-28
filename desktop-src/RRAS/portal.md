---
title: Service de routage et d’accès à distance
description: Service de routage et d’accès à distance
ms.assetid: fa0a183a-0254-401e-8b78-441cb3f83e8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d81e743f640e600588413f0c15c44e0410c5ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116467"
---
# <a name="routing-and-remote-access-service"></a><span data-ttu-id="53d7e-103">Service de routage et d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="53d7e-103">Routing and Remote Access Service</span></span>

## <a name="purpose"></a><span data-ttu-id="53d7e-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="53d7e-104">Purpose</span></span>

<span data-ttu-id="53d7e-105">Le service d’accès à distance (RAS) peut être utilisé pour créer des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="53d7e-105">Remote Access Service (RAS) can be used to create client applications.</span></span> <span data-ttu-id="53d7e-106">Ces applications affichent les boîtes de dialogue courantes RAS, gèrent les connexions et les appareils d’accès à distance et manipulent les entrées d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="53d7e-106">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span>

<span data-ttu-id="53d7e-107">Les API de routage permettent de créer des applications pour administrer les fonctionnalités de routage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="53d7e-107">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

<span data-ttu-id="53d7e-108">Les développeurs peuvent utiliser les API de protocole de routage pour implémenter des protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="53d7e-108">Developers can use the Routing Protocol APIs to implement routing protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="53d7e-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="53d7e-109">Developer audience</span></span>

<span data-ttu-id="53d7e-110">Les API de service de routage et d’accès à distance sont conçues pour être utilisées par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="53d7e-110">The Routing and Remote Access Service APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="53d7e-111">Les programmeurs doivent également être familiarisés avec les concepts de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="53d7e-111">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="53d7e-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="53d7e-112">Run-time requirements</span></span>

<span data-ttu-id="53d7e-113">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="53d7e-113">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53d7e-114">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="53d7e-114">In this section</span></span>



| <span data-ttu-id="53d7e-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="53d7e-115">Topic</span></span>                                                                                                             | <span data-ttu-id="53d7e-116">Description</span><span class="sxs-lookup"><span data-stu-id="53d7e-116">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53d7e-117">Architecture des services de routage et d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="53d7e-117">Routing and Remote Access Services Architecture</span></span>](routing-and-remote-access-services-architecture.md)<br/> | <span data-ttu-id="53d7e-118">Vue d’ensemble de l’architecture des services de routage et d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="53d7e-118">Overview of the Routing and Remote Access Services architecture.</span></span><br/>                                           |
| [<span data-ttu-id="53d7e-119">Disposition du Registre du routage et de l’accès distant</span><span class="sxs-lookup"><span data-stu-id="53d7e-119">Routing and Remote Access Registry Layout</span></span>](routing-and-remote-access-registry-layout.md)<br/>             | <span data-ttu-id="53d7e-120">Exemple de disposition du Registre pour le service de routeur</span><span class="sxs-lookup"><span data-stu-id="53d7e-120">An example registry layout for the router service</span></span><br/>                                                          |
| [<span data-ttu-id="53d7e-121">Codes d’erreur de routage et d’accès distant</span><span class="sxs-lookup"><span data-stu-id="53d7e-121">Routing and Remote Access Error Codes</span></span>](routing-and-remote-access-error-codes.md)<br/>                     | <span data-ttu-id="53d7e-122">Liste de tous les codes d’erreur de routage et d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="53d7e-122">List of all routing and remote access error codes.</span></span><br/>                                                         |
| [<span data-ttu-id="53d7e-123">Accès à distance</span><span class="sxs-lookup"><span data-stu-id="53d7e-123">Remote Access</span></span>](remote-access-start-page.md)<br/>                                                          | <span data-ttu-id="53d7e-124">Documentation pour les API d’administration RAS et RAS.</span><span class="sxs-lookup"><span data-stu-id="53d7e-124">Documentation for RAS and RAS Administration APIs.</span></span><br/>                                                         |
| [<span data-ttu-id="53d7e-125">Routage</span><span class="sxs-lookup"><span data-stu-id="53d7e-125">Routing</span></span>](routing-start-page.md)<br/>                                                                      | <span data-ttu-id="53d7e-126">Documentation sur les API de gestion de routeur et de base d’informations de gestion (MIB).</span><span class="sxs-lookup"><span data-stu-id="53d7e-126">Documentation for the Router Management and Management Information Base (MIB) APIs.</span></span><br/>                        |
| [<span data-ttu-id="53d7e-127">Protocoles de routage</span><span class="sxs-lookup"><span data-stu-id="53d7e-127">Routing Protocols</span></span>](routing-protocols-start-page.md)<br/>                                                  | <span data-ttu-id="53d7e-128">Documentation du gestionnaire de groupe de multidiffusion, de l’interface de protocole de routage et des API du gestionnaire de table de routage.</span><span class="sxs-lookup"><span data-stu-id="53d7e-128">Documentation for the Multicast Group Manager, Routing Protocol Interface, and Routing Table Manager APIs.</span></span><br/> |
| [<span data-ttu-id="53d7e-129">Glossaire</span><span class="sxs-lookup"><span data-stu-id="53d7e-129">Glossary</span></span>](glossary.md)<br/>                                                                               | <span data-ttu-id="53d7e-130">Définitions des termes utilisés dans la documentation du service Routage et accès distant.</span><span class="sxs-lookup"><span data-stu-id="53d7e-130">Definitions for terms used in the Routing and Remote Access Service documentation.</span></span><br/>                         |



 

 

 





