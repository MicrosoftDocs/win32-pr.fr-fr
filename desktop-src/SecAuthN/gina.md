---
description: L’objectif d’une DLL GINA est de fournir une identification utilisateur personnalisable et des procédures d’authentification. Par défaut, GINA effectue cette opération en déléguant l’analyse des événements SAS à Winlogon, qui reçoit et traite les séquences de touches de sécurité + ALT + SUPPR (SASs).
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758266"
---
# <a name="gina"></a><span data-ttu-id="791bf-104">GINA</span><span class="sxs-lookup"><span data-stu-id="791bf-104">GINA</span></span>

<span data-ttu-id="791bf-105">La bibliothèque [*Gina*](/windows/desktop/SecGloss/g-gly) fonctionne dans le [*contexte*](/windows/desktop/SecGloss/c-gly) du processus [*Winlogon*](/windows/desktop/SecGloss/w-gly) et, par conséquent, la DLL GINA est chargée très tôt dans le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="791bf-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="791bf-106">La DLL GINA doit suivre les règles afin que l’intégrité du système soit maintenue, en particulier en ce qui concerne l’interaction avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="791bf-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="791bf-107">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="791bf-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="791bf-108">L’utilisation la plus courante de GINA consiste à communiquer avec un périphérique externe tel qu’un [*lecteur*](/windows/desktop/SecGloss/r-gly)de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="791bf-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="791bf-109">Il est essentiel de définir le paramètre de démarrage du pilote de périphérique sur System (Winnt. h : SERVICE \_ System \_ Start) pour vous assurer que le pilote est chargé au moment de l’appel de Gina.</span><span class="sxs-lookup"><span data-stu-id="791bf-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="791bf-110">L’objectif d’une DLL GINA est de fournir une identification utilisateur personnalisable et des procédures d’authentification.</span><span class="sxs-lookup"><span data-stu-id="791bf-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="791bf-111">Par défaut, GINA effectue cette opération en déléguant l’analyse des événements SAS à Winlogon, qui reçoit et traite les [*séquences*](/windows/desktop/SecGloss/s-gly) de touches de sécurité + ALT + SUPPR (SASS).</span><span class="sxs-lookup"><span data-stu-id="791bf-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="791bf-112">Un GINA personnalisé est chargé de configurer lui-même de recevoir des événements SAS (autres que l’événement SAS CTRL + ALT + DEL par défaut) et de notifier Winlogon lorsque des événements SAS se produisent.</span><span class="sxs-lookup"><span data-stu-id="791bf-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="791bf-113">Winlogon évalue son état pour déterminer ce qui est requis pour traiter la SAP de la GINA personnalisée.</span><span class="sxs-lookup"><span data-stu-id="791bf-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="791bf-114">Ce traitement comprend généralement des appels aux fonctions de traitement SAS de la GINA.</span><span class="sxs-lookup"><span data-stu-id="791bf-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="791bf-115">Pour plus d’informations sur les fonctions d’exportation GINA spécifiques, consultez [fonctions d’exportation Gina](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="791bf-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="791bf-116">Pour plus d’informations sur l’utilisation des structures GINA pour transmettre des informations, consultez [structures Gina](authentication-structures.md).</span><span class="sxs-lookup"><span data-stu-id="791bf-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="791bf-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="791bf-117">Topic</span></span>                                                                             | <span data-ttu-id="791bf-118">Description</span><span class="sxs-lookup"><span data-stu-id="791bf-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="791bf-119">Chargement et exécution d’une DLL GINA</span><span class="sxs-lookup"><span data-stu-id="791bf-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="791bf-120">Valeur de clé de Registre à modifier pour charger et exécuter une DLL GINA personnalisée.</span><span class="sxs-lookup"><span data-stu-id="791bf-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="791bf-121">Génération et test d’une DLL GINA</span><span class="sxs-lookup"><span data-stu-id="791bf-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="791bf-122">Comment tester une DLL GINA.</span><span class="sxs-lookup"><span data-stu-id="791bf-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

