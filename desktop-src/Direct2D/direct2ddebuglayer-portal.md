---
title: Couche de débogage Direct2D
description: Extension d’exécution pour Direct2D qui fournit des messages d’erreur descriptifs, la détection des fuites d’objets, des notifications de performances et d’autres signaux pour vous aider à créer des applications Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379679"
---
# <a name="direct2d-debug-layer"></a><span data-ttu-id="d4db0-103">Couche de débogage Direct2D</span><span class="sxs-lookup"><span data-stu-id="d4db0-103">Direct2D Debug Layer</span></span>

## <a name="purpose"></a><span data-ttu-id="d4db0-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="d4db0-104">Purpose</span></span>

<span data-ttu-id="d4db0-105">La couche de débogage Direct2D, implémentée séparément de Direct2D dans sa propre DLL nommée d2d1debug.dll, fournit des messages de débogage au moment du design pour réduire l’échec de l’application Runtime.</span><span class="sxs-lookup"><span data-stu-id="d4db0-105">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="d4db0-106">Les messages de débogage résultent souvent de violations de contrats d’API telles que les paramètres non valides (qui peuvent être liés à Direct3D), de ressources non valides, de violations de threads et d’autres problèmes de performances, tels que l’utilisation d’une couche quand un clip suffit.</span><span class="sxs-lookup"><span data-stu-id="d4db0-106">The debug messages often result from violations of API contracts such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and other performance issues such as using a layer when a clip would suffice.</span></span>

<span data-ttu-id="d4db0-107">Pour vous aider à déterminer la quantité d’informations qui est tracée par la couche de débogage, la couche de débogage offre trois niveaux de débogage : informations, avertissement et erreur.</span><span class="sxs-lookup"><span data-stu-id="d4db0-107">To help you decide how much information is traced by the debug layer, the debug layer offers three debug levels: information, warning, and error.</span></span> <span data-ttu-id="d4db0-108">Ces trois niveaux sont interprétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="d4db0-108">These three levels are interpreted as follows:</span></span>

-   <span data-ttu-id="d4db0-109">**Erreur :** Direct2D envoie des messages d’erreur graves à la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="d4db0-109">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="d4db0-110">Par exemple, l’interruption d’une contrainte de thread génère une erreur grave.</span><span class="sxs-lookup"><span data-stu-id="d4db0-110">For example, breaking a threading constraint will generate a severe error.</span></span>

    <span data-ttu-id="d4db0-111">En outre, un message d’erreur de niveau déclenche le point d’arrêt pour vous aider à effectuer le débogage.</span><span class="sxs-lookup"><span data-stu-id="d4db0-111">Further, a message of level error triggers the breakpoint to help you debug.</span></span>

-   <span data-ttu-id="d4db0-112">**Avertissement :** Direct2D envoie des messages d’erreur et des avertissements à la couche de débogage pour vous permettre de traiter l’un de ces messages.</span><span class="sxs-lookup"><span data-stu-id="d4db0-112">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="d4db0-113">**Informations :** Direct2D envoie des messages d’erreur, des avertissements et des informations de diagnostic supplémentaires à la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="d4db0-113">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="d4db0-114">Par exemple, les messages d’amélioration des performances seront envoyés à ce niveau de débogage.</span><span class="sxs-lookup"><span data-stu-id="d4db0-114">For example, performance improvement messages will be sent at this debug level.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4db0-115">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d4db0-115">In this section</span></span>



| <span data-ttu-id="d4db0-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d4db0-116">Topic</span></span>                                                                                     | <span data-ttu-id="d4db0-117">Description</span><span class="sxs-lookup"><span data-stu-id="d4db0-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d4db0-118">Installation de la couche de débogage Direct2D</span><span class="sxs-lookup"><span data-stu-id="d4db0-118">Installing the Direct2D Debug Layer</span></span>](installing-the-direct2d-debug-layer.md)<br/> | <span data-ttu-id="d4db0-119">Décrit comment installer la couche de débogage Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d4db0-119">Describes how to install the Direct2D debug layer.</span></span><br/>      |
| [<span data-ttu-id="d4db0-120">Vue d’ensemble de la couche de débogage Direct2D</span><span class="sxs-lookup"><span data-stu-id="d4db0-120">Direct2D Debug Layer Overview</span></span>](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [<span data-ttu-id="d4db0-121">Messages de débogage</span><span class="sxs-lookup"><span data-stu-id="d4db0-121">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)<br/>                         | <span data-ttu-id="d4db0-122">Répertorie les messages de débogage de la couche de débogage Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d4db0-122">Lists the debug messages from the Direct2D Debug Layer.</span></span><br/> |



 

 

 





