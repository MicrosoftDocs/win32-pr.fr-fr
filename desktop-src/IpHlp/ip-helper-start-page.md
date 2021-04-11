---
description: L’API Internet Protocol Helper (assistance IP) permet d’extraire et de modifier les paramètres de configuration réseau de l’ordinateur local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Assistance IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862446"
---
# <a name="ip-helper"></a><span data-ttu-id="92dd1-103">Assistance IP</span><span class="sxs-lookup"><span data-stu-id="92dd1-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="92dd1-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="92dd1-104">Purpose</span></span>

<span data-ttu-id="92dd1-105">L’API Internet Protocol Helper (assistance IP) permet d’extraire et de modifier les paramètres de configuration réseau de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="92dd1-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="92dd1-106">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="92dd1-106">Where applicable</span></span>

<span data-ttu-id="92dd1-107">L’API d’assistance IP est applicable dans tout environnement informatique dans lequel la manipulation par programmation de la configuration réseau et TCP/IP est utile.</span><span class="sxs-lookup"><span data-stu-id="92dd1-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="92dd1-108">Les applications typiques incluent les protocoles de routage IP et les agents SNMP (simple Network Management Protocol).</span><span class="sxs-lookup"><span data-stu-id="92dd1-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="92dd1-109">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="92dd1-109">Developer audience</span></span>

<span data-ttu-id="92dd1-110">L’API d’assistance IP est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="92dd1-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="92dd1-111">Les programmeurs doivent également être familiarisés avec les concepts de mise en réseau Windows et TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="92dd1-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="92dd1-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="92dd1-112">Run-time requirements</span></span>

<span data-ttu-id="92dd1-113">L’API d’assistance IP peut être utilisée sur toutes les plateformes Windows.</span><span class="sxs-lookup"><span data-stu-id="92dd1-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="92dd1-114">Tous les systèmes d’exploitation ne prennent pas en charge toutes les fonctions.</span><span class="sxs-lookup"><span data-stu-id="92dd1-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="92dd1-115">Lorsque certaines implémentations ou fonctionnalités des restrictions de plateforme Windows Sockets 2 existent, elles sont clairement notées dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="92dd1-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="92dd1-116">Si une fonction d’assistance IP est appelée sur une plateforme qui ne prend pas en charge la fonction, l’erreur \_ non \_ prise en charge est retournée.</span><span class="sxs-lookup"><span data-stu-id="92dd1-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="92dd1-117">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="92dd1-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92dd1-118">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="92dd1-118">In this section</span></span>



| <span data-ttu-id="92dd1-119">Rubrique</span><span class="sxs-lookup"><span data-stu-id="92dd1-119">Topic</span></span>                                                              | <span data-ttu-id="92dd1-120">Description</span><span class="sxs-lookup"><span data-stu-id="92dd1-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92dd1-121">Nouveautés du programme d’assistance IP</span><span class="sxs-lookup"><span data-stu-id="92dd1-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="92dd1-122">Informations sur les nouvelles fonctionnalités de l’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="92dd1-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="92dd1-123">À propos de l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="92dd1-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="92dd1-124">Informations générales sur les considérations et les fonctionnalités de programmation d’assistance IP disponibles pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="92dd1-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="92dd1-125">Utilisation de l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="92dd1-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="92dd1-126">Procédures et techniques de programmation utilisées avec l’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="92dd1-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="92dd1-127">Cette section comprend des techniques de base de programmation d’assistance IP, telles que [prise en main avec IP Helper](getting-started-with-ip-helper.md).</span><span class="sxs-lookup"><span data-stu-id="92dd1-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="92dd1-128">Informations de référence sur l’assistance IP</span><span class="sxs-lookup"><span data-stu-id="92dd1-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="92dd1-129">Documentation de référence pour les fonctions, structures et énumérations d’assistance IP.</span><span class="sxs-lookup"><span data-stu-id="92dd1-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="92dd1-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92dd1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92dd1-131">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="92dd1-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="92dd1-132">Service de routage et d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="92dd1-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 

