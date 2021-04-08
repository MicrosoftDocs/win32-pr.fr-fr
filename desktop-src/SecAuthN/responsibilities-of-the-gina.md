---
description: Répertorie et explique les responsabilités du GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilités du GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034472"
---
# <a name="responsibilities-of-the-gina"></a><span data-ttu-id="be7bc-103">Responsabilités du GINA</span><span class="sxs-lookup"><span data-stu-id="be7bc-103">Responsibilities of the GINA</span></span>

> [!Note]  
> <span data-ttu-id="be7bc-104">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be7bc-104">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="be7bc-105">Une dll [*Gina*](../secgloss/g-gly.md) a les responsabilités suivantes :</span><span class="sxs-lookup"><span data-stu-id="be7bc-105">A [*GINA*](../secgloss/g-gly.md) DLL has the following responsibilities:</span></span>

-   <span data-ttu-id="be7bc-106">Analyse SAS</span><span class="sxs-lookup"><span data-stu-id="be7bc-106">SAS monitoring</span></span>

    <span data-ttu-id="be7bc-107">La GINA est chargée de reconnaître une [*séquence de sécurité sécurisée*](../secgloss/s-gly.md) (SAS), de surveiller les événements SAS et de notifier Winlogon quand une SAP s’est produite.</span><span class="sxs-lookup"><span data-stu-id="be7bc-107">The GINA is responsible for recognizing a [*secure attention sequence*](../secgloss/s-gly.md) (SAS), monitoring for SAS events, and notifying Winlogon when a SAS has occurred.</span></span> <span data-ttu-id="be7bc-108">Notez qu’il peut y avoir plus d’une SAP définie et que l’ensemble de SASs défini peut changer au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="be7bc-108">Note that there can be more than one SAS defined, and the set of defined SASs can change over time.</span></span> <span data-ttu-id="be7bc-109">Par exemple, il peut y avoir un jeu de SASs lorsque [*Winlogon*](../secgloss/w-gly.md) est dans l’état de déconnexion et un autre ensemble lorsqu’il se trouve à l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="be7bc-109">For example, there can be one set of SASs when [*Winlogon*](../secgloss/w-gly.md) is in the logged-off state and another set when it is in the logged-on state.</span></span>

    <span data-ttu-id="be7bc-110">Winlogon fournit des services pour assister le GINA dans à l’aide de la combinaison de touches CTRL + ALT + DEL SAS.</span><span class="sxs-lookup"><span data-stu-id="be7bc-110">Winlogon provides services to assist the GINA in using the CTRL+ALT+DEL SAS.</span></span>

-   <span data-ttu-id="be7bc-111">Traitement SAS</span><span class="sxs-lookup"><span data-stu-id="be7bc-111">SAS processing</span></span>

    <span data-ttu-id="be7bc-112">L’une des raisons qui justifient le remplacement de GINA est de fournir d’autres mécanismes d’identification et d’authentification.</span><span class="sxs-lookup"><span data-stu-id="be7bc-112">One reason for making the GINA replaceable is to provide alternative identification and authentication mechanisms.</span></span> <span data-ttu-id="be7bc-113">Pour ce faire, GINA doit présenter toutes les interfaces utilisateur résultant de la reconnaissance d’une signature d’accès partagé.</span><span class="sxs-lookup"><span data-stu-id="be7bc-113">To do this, the GINA must present all user interfaces resulting from the recognition of a SAS.</span></span> <span data-ttu-id="be7bc-114">Quand aucun utilisateur n’est connecté, GINA est responsable de la présentation des options d’identification et d’authentification, ainsi que de toutes les autres options autorisées qui ne sont pas authentifiées.</span><span class="sxs-lookup"><span data-stu-id="be7bc-114">When no user is logged on, the GINA is responsible for presenting identification and authentication options as well as any other permissible options that are not authenticated.</span></span> <span data-ttu-id="be7bc-115">Lorsqu’un utilisateur a ouvert une session, GINA est responsable de la présentation des options pertinentes à l’utilisateur, ainsi que de la réalisation des actions jugées appropriées.</span><span class="sxs-lookup"><span data-stu-id="be7bc-115">When a user is logged on, the GINA is responsible for presenting the relevant options to the user as well as taking whatever actions are deemed appropriate.</span></span> <span data-ttu-id="be7bc-116">Par exemple, dans un système qui comprend une [*carte à puce*](../secgloss/s-gly.md), il peut être approprié de verrouiller automatiquement la station de travail si l’utilisateur supprime la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="be7bc-116">For example, in a system that includes a [*smart card*](../secgloss/s-gly.md), it may be appropriate to automatically lock the workstation if the user removes the smart card.</span></span>

-   <span data-ttu-id="be7bc-117">Activation du shell</span><span class="sxs-lookup"><span data-stu-id="be7bc-117">Shell activation</span></span>

    <span data-ttu-id="be7bc-118">Lorsqu’un utilisateur ouvre une session, GINA est responsable de la création d’un ou plusieurs processus initiaux pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be7bc-118">When a user logs on, the GINA is responsible for creating one or more initial processes for that user.</span></span> <span data-ttu-id="be7bc-119">(Dans cette documentation, on suppose que ces processus initiaux présentent une interface à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be7bc-119">(In this documentation, it is assumed that these initial processes present an interface to the user.</span></span> <span data-ttu-id="be7bc-120">Toutefois, les processus peuvent être des processus et n’ont pas nécessairement besoin d’interagir avec l’utilisateur.) Ces processus sont appelés Shell de l' *utilisateur* ou simplement l' *interpréteur* de commandes.</span><span class="sxs-lookup"><span data-stu-id="be7bc-120">However, the processes can actually be any processes and do not necessarily have to interact with the user.) These processes are referred to as the *user shell* or just the *shell*.</span></span> <span data-ttu-id="be7bc-121">Dans le cadre de l’activation de l’interpréteur de commandes, le GINA doit affecter le jeton de l’utilisateur qui vient d’être connecté aux processus.</span><span class="sxs-lookup"><span data-stu-id="be7bc-121">As part of shell activation, the GINA must assign the newly logged-on user's token to the processes.</span></span> <span data-ttu-id="be7bc-122">Winlogon fournit un service pour aider la GINA à assigner le jeton.</span><span class="sxs-lookup"><span data-stu-id="be7bc-122">Winlogon provides a service to assist the GINA in assigning the token.</span></span>

 

 
