---
description: Une exception est un événement qui se produit pendant l’exécution d’un programme et qui requiert l’exécution du code en dehors du déroulement normal du contrôle.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860674"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="c3fa3-103">Gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="c3fa3-103">Structured Exception Handling</span></span>

<span data-ttu-id="c3fa3-104">Une *exception* est un événement qui se produit pendant l’exécution d’un programme et qui requiert l’exécution du code en dehors du déroulement normal du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="c3fa3-105">Il existe deux types d’exceptions : les exceptions matérielles et les exceptions logicielles.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="c3fa3-106">Les *exceptions matérielles* sont initiées par le processeur.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="c3fa3-107">Ils peuvent résulter de l’exécution de certaines séquences d’instructions, telles que la division par zéro ou d’une tentative d’accès à une adresse mémoire non valide.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="c3fa3-108">Les *exceptions logicielles* sont initiées explicitement par les applications ou le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="c3fa3-109">Par exemple, le système peut détecter si une valeur de paramètre non valide est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="c3fa3-110">La *gestion structurée des exceptions* est un mécanisme permettant de gérer les exceptions matérielles et logicielles.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="c3fa3-111">Par conséquent, votre code gère les exceptions matérielles et logicielles de la même manière.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="c3fa3-112">La gestion structurée des exceptions vous permet d’avoir un contrôle complet sur la gestion des exceptions, fournit la prise en charge des débogueurs et est utilisable dans l’ensemble des langages de programmation et des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="c3fa3-113">La *gestion des exceptions vectorisées* est une extension de la gestion structurée des exceptions.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="c3fa3-114">Le système prend également en charge la *gestion des arrêts*, ce qui vous permet de vous assurer que chaque fois qu’un corps de code protégé est exécuté, un bloc de code d’arrêt spécifié est également exécuté.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="c3fa3-115">Le code d’arrêt est exécuté, quelle que soit la façon dont le contrôle de workflow quitte le corps protégé.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="c3fa3-116">Par exemple, un gestionnaire de terminaisons peut garantir que les tâches de nettoyage sont effectuées même si une exception ou une autre erreur se produit pendant l’exécution du corps de code protégé.</span><span class="sxs-lookup"><span data-stu-id="c3fa3-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="c3fa3-117">À propos de la gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="c3fa3-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="c3fa3-118">Utilisation de la gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="c3fa3-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="c3fa3-119">Référence de gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="c3fa3-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



