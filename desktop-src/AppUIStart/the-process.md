---
title: Vue d’ensemble du développement d’interface utilisateur
description: Cette section décrit les trois phases de conception de l’interface utilisateur et présente les tâches qui sont généralement associées à chaque phase.
ms.assetid: ab544cb9-eed3-4575-a8dd-2f5d7b5c575f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b531fb07a1805c14441c81777bbdddad0739e7cb
ms.sourcegitcommit: e5c43274e96cb8fd1b60fc187ef16723e9258367
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2020
ms.locfileid: "104030719"
---
# <a name="overview-of-the-user-interface-development-process"></a><span data-ttu-id="3c2ad-103">Vue d’ensemble du processus de développement de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3c2ad-103">Overview of the User Interface Development Process</span></span>

<span data-ttu-id="3c2ad-104">Cette section décrit les trois phases de conception de l’interface utilisateur et présente les tâches qui sont généralement associées à chaque phase.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-104">This section outlines the three phases of user interface design and introduces the tasks that are typically associated with each phase.</span></span>

## <a name="the-application-user-interface-and-the-user-experience"></a><span data-ttu-id="3c2ad-105">L’interface utilisateur de l’application et l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="3c2ad-105">The Application User Interface and the User Experience</span></span>

<span data-ttu-id="3c2ad-106">Pour commencer, vous devez préciser les termes « interface utilisateur » et « expérience utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="3c2ad-106">To begin, the terms "user interface" and "user experience" must be clarified.</span></span>

<span data-ttu-id="3c2ad-107">L’interface utilisateur d’une application implique généralement les objets qu’un utilisateur voit et interagit directement sur son écran.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-107">The user interface of an application typically involves those objects that a user sees and interacts with directly on their screen.</span></span> <span data-ttu-id="3c2ad-108">Par exemple, ces objets incluent l’espace de document, les menus, les boîtes de dialogue, les icônes, les images et les animations.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-108">For example, such objects include the document space, menus, dialog boxes, icons, images, and animations.</span></span>

<span data-ttu-id="3c2ad-109">Toutefois, l’interface utilisateur d’une application n’est qu’un aspect de l’expérience utilisateur globale.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-109">However, the user interface of an application is only one aspect of the overall user experience.</span></span> <span data-ttu-id="3c2ad-110">Les autres aspects de l’expérience utilisateur qui ne sont pas visibles par l’utilisateur, mais qui sont intégrés à une application et qui sont essentiels à son utilisation, incluent le temps de démarrage, la latence, la gestion des erreurs et les tâches automatisées qui sont terminées sans interaction directe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-110">Other aspects of the user experience that are not visible to the user, but are integral to an application and critical to its usability, include start up time, latency, error handling, and automated tasks that are completed without direct user interaction.</span></span>

<span data-ttu-id="3c2ad-111">En général, une interface utilisateur requiert une action d’un utilisateur pour accomplir une tâche, tandis qu’une expérience utilisateur exceptionnelle peut être obtenue sans aucune interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-111">In general, a user interface requires action by a user to accomplish a task, while a great user experience can be achieved with no user interface at all.</span></span>

## <a name="user-interface-development"></a><span data-ttu-id="3c2ad-112">Développement de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3c2ad-112">User Interface Development</span></span>

<span data-ttu-id="3c2ad-113">Fournir une expérience utilisateur réussie nécessite une approche équilibrée tout au long du cycle de vie du développement.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-113">Providing a successful user experience requires a balanced approach throughout the development life cycle.</span></span> <span data-ttu-id="3c2ad-114">Pour garantir cet équilibre, vous devez non seulement vous concentrer sur l’implémentation des fonctionnalités requises pour effectuer une tâche, mais également sur la façon dont la tâche est exposée par le biais de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-114">To ensure this balance, you must not only focus on implementing the functionality required to complete a task but also on how the task is exposed through the user interface.</span></span> <span data-ttu-id="3c2ad-115">Rappelez-vous que l’interface utilisateur ne doit pas être fonctionnelle, elle doit également être utilisable.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-115">Remember, the user interface must not only be functional, it must also be usable.</span></span>

<span data-ttu-id="3c2ad-116">L’exemple suivant présente les phases typiques du processus de Dvelopment de l’interface utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3c2ad-116">The following outlines the typical phases of the user interface dvelopment process:</span></span>

### <a name="designing"></a><span data-ttu-id="3c2ad-117">Conception</span><span class="sxs-lookup"><span data-stu-id="3c2ad-117">Designing</span></span>

-   <span data-ttu-id="3c2ad-118">Spécifications fonctionnelles : Déterminez les exigences et les objectifs initiaux de l’application.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-118">Functional requirements – Determine the initial requirements and goals for the application.</span></span>
-   <span data-ttu-id="3c2ad-119">Analyse utilisateur : Identifiez les scénarios utilisateur et comprenez les besoins et les attentes des utilisateurs pour chaque scénario.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-119">User analysis – Identify the user scenarios and understand the needs and expectations of users for each scenario.</span></span>
-   <span data-ttu-id="3c2ad-120">Conception conceptuelle : modélisez l’entreprise sous-jacente que l’application doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-120">Conceptual design – Model the underlying business that the application must support.</span></span>
-   <span data-ttu-id="3c2ad-121">Conception logique : concevez le processus et le workflow d’informations de l’application.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-121">Logical design – Design the process and information flow of the application.</span></span>
-   <span data-ttu-id="3c2ad-122">Conception physique : Déterminez comment la conception logique sera implémentée sur des plateformes physiques spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-122">Physical design – Decide how the logical design will be implemented on specific physical platforms.</span></span>

### <a name="implementing"></a><span data-ttu-id="3c2ad-123">Conféré</span><span class="sxs-lookup"><span data-stu-id="3c2ad-123">Implementing</span></span>

-   <span data-ttu-id="3c2ad-124">Prototype : développez des maquettes de papier ou d’écran interactif qui se concentrent sur l’interface et n’incluez pas d’éléments de conception visuelle gênants.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-124">Prototype – Develop paper or interactive screen mockups that focus on the interface and don't include distracting visual design elements.</span></span>
-   <span data-ttu-id="3c2ad-125">Construct : générez l’application et préparez les demandes de modification de conception.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-125">Construct – Build the application and prepare for design change requests.</span></span>

### <a name="testing"></a><span data-ttu-id="3c2ad-126">Test</span><span class="sxs-lookup"><span data-stu-id="3c2ad-126">Testing</span></span>

-   <span data-ttu-id="3c2ad-127">Test d’utilisabilité : Testez l’application avec divers utilisateurs et scénarios.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-127">Usability testing – Test the application with various users and scenarios.</span></span>
-   <span data-ttu-id="3c2ad-128">Test d’accessibilité : Testez l’application avec des technologies accessibles et des outils de test automatisés.</span><span class="sxs-lookup"><span data-stu-id="3c2ad-128">Accessibility testing – Test the application with accessible technologies and automated test tools.</span></span>

 

 




