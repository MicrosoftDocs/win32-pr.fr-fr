---
title: Prise en main du développement de l’interface utilisateur pour les applications Windows
description: .
ms.assetid: 29d6f67b-46fa-4f39-a319-306c832eff9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c3d1a182aef6354901f0fa71f94b39ecdc58f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729109"
---
# <a name="getting-started-developing-user-interfaces-for-windows-applications"></a><span data-ttu-id="3ee5b-103">Prise en main développement d’interfaces utilisateur pour les applications Windows</span><span class="sxs-lookup"><span data-stu-id="3ee5b-103">Getting Started Developing User Interfaces for Windows Applications</span></span>

## <a name="purpose"></a><span data-ttu-id="3ee5b-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="3ee5b-104">Purpose</span></span>

<span data-ttu-id="3ee5b-105">Les sections suivantes proposent des conseils généraux pour les développeurs qui conçoivent, implémentent et testent l’interface utilisateur d’une application Windows.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-105">The following sections offer general guidance to developers who are designing, implementing, and testing the user interface of a Windows application.</span></span>

<span data-ttu-id="3ee5b-106">En plus des principes de conception de l’interface utilisateur de base, de nombreuses recommandations et suggestions sont fournies pour aider les développeurs à fournir une expérience utilisateur aussi simple, efficace et agréable que possible.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-106">In addition to basic user interface design principles, numerous recommendations and suggestions are provided that will help developers provide a user experience that is as simple, efficient, and enjoyable as possible.</span></span>

> [!Note]  
> <span data-ttu-id="3ee5b-107">Ces recommandations ne sont pas destinées à être exhaustives et sont soumises à la portée et aux fonctionnalités spécifiques d’une application.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-107">These guidelines are not intended to be comprehensive and are subject to the specific scope and functionality of an application.</span></span> <span data-ttu-id="3ee5b-108">Pour obtenir des instructions plus complètes, consultez les [instructions relatives à l’interaction avec l’expérience utilisateur Windows](../uxguide/guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="3ee5b-108">For more comprehensive guidelines, see the [Windows User Experience Interaction Guidelines](../uxguide/guidelines.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="3ee5b-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3ee5b-109">In this section</span></span>



| <span data-ttu-id="3ee5b-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3ee5b-110">Topic</span></span>                                                                            | <span data-ttu-id="3ee5b-111">Description</span><span class="sxs-lookup"><span data-stu-id="3ee5b-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ee5b-112">Vue d’ensemble du processus de développement de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3ee5b-112">Overview of the User Interface Development Process</span></span>](the-process.md)<br/> | <span data-ttu-id="3ee5b-113">Cette section décrit les trois phases de conception de l’interface utilisateur et présente les tâches qui sont généralement associées à chaque phase.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-113">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span><br/>                                              |
| [<span data-ttu-id="3ee5b-114">Conception d’une interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3ee5b-114">Designing a User Interface</span></span>](designing-a-user-interface.md)<br/>          | <span data-ttu-id="3ee5b-115">Cette section décrit en détail certaines des tâches associées à la conception d’une interface utilisateur pour une application Windows.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-115">This section describes in detail some of the tasks associated with designing a UI for a Windows application.</span></span><br/>                                                                         |
| [<span data-ttu-id="3ee5b-116">Implémentation d’une interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3ee5b-116">Implementing a User Interface</span></span>](implementing-a-user-interface.md)<br/>    | <span data-ttu-id="3ee5b-117">Cette section décrit certaines des tâches associées à l’implémentation d’une interface utilisateur pour une application Windows.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-117">This section describes some of the tasks associated with implementing a user interface for a Windows application.</span></span><br/>                                                                    |
| [<span data-ttu-id="3ee5b-118">Test d’une interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3ee5b-118">Testing a User Interface</span></span>](testing-a-user-interface.md)<br/>              | <span data-ttu-id="3ee5b-119">Cette section décrit en détail certaines des tâches associées au test d’une interface utilisateur pour une application Windows.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-119">This section describes in detail some of the tasks associated with testing a UI for a Windows application.</span></span><br/>                                                                           |
| [<span data-ttu-id="3ee5b-120">Considérations relatives à la sécurité : interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="3ee5b-120">Security Considerations: Windows User Interface</span></span>](sec-ui.md)<br/>         | <span data-ttu-id="3ee5b-121">Cette rubrique fournit des informations sur les considérations relatives à la sécurité dans l’interface utilisateur de Windows.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-121">This topic provides information about security considerations in the Windows User Interface.</span></span><br/>                                                                                         |
| [<span data-ttu-id="3ee5b-122">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="3ee5b-122">Other Resources</span></span>](other-resources.md)<br/>                                | <span data-ttu-id="3ee5b-123">Cette section contient la liste des manuels et des ressources recommandés en rapport avec la conception de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3ee5b-123">This section contains a list of recommended books and resources related to user interface design.</span></span> <span data-ttu-id="3ee5b-124">(Ces livres et ressources peuvent ne pas être disponibles dans certaines langues et certains pays.)</span><span class="sxs-lookup"><span data-stu-id="3ee5b-124">(These books and resources may not be available in some languages and countries.)</span></span> <br/> |



 

 

