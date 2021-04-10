---
title: Journal des événements Windows
description: L’API du journal des événements Windows définit le schéma que vous utilisez pour écrire un manifeste d’instrumentation.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842706"
---
# <a name="windows-event-log"></a><span data-ttu-id="ed627-103">Journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="ed627-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="ed627-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="ed627-104">Purpose</span></span>

<span data-ttu-id="ed627-105">L’API du journal des événements Windows définit le schéma que vous utilisez pour écrire un manifeste d’instrumentation.</span><span class="sxs-lookup"><span data-stu-id="ed627-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="ed627-106">Un manifeste d’instrumentation identifie votre fournisseur d’événements et les événements qu’il enregistre.</span><span class="sxs-lookup"><span data-stu-id="ed627-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="ed627-107">L’API comprend également les fonctions qu’un consommateur d’événements, tel que le [Observateur d’événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), utiliserait pour lire et restituer les événements.</span><span class="sxs-lookup"><span data-stu-id="ed627-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="ed627-108">Pour écrire les événements définis dans le manifeste, utilisez les fonctions incluses dans l’API de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="ed627-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="ed627-109">Le journal des événements Windows remplace l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) en commençant par le système d’exploitation Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed627-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ed627-110">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="ed627-110">Developer audience</span></span>

<span data-ttu-id="ed627-111">Le journal des événements Windows est conçu pour les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="ed627-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ed627-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="ed627-112">Run-time requirements</span></span>

<span data-ttu-id="ed627-113">Le journal des événements Windows est inclus dans le système d’exploitation à compter de Windows Vista et de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ed627-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="ed627-114">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ed627-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="ed627-115">Pour obtenir un historique complet des versions, consultez [Nouveautés](what-s-new.md).</span><span class="sxs-lookup"><span data-stu-id="ed627-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed627-116">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="ed627-116">In this section</span></span>


| <span data-ttu-id="ed627-117">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ed627-117">Topic</span></span>                                                        | <span data-ttu-id="ed627-118">Description</span><span class="sxs-lookup"><span data-stu-id="ed627-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed627-119">Utilisation du journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="ed627-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="ed627-120">Guide procédural qui montre comment utiliser l’API du journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="ed627-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="ed627-121">Informations de référence sur le journal des événements Windows</span><span class="sxs-lookup"><span data-stu-id="ed627-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="ed627-122">Les types de données, les fonctions, les énumérations, les structures, les constantes et les schémas inclus dans l’API.</span><span class="sxs-lookup"><span data-stu-id="ed627-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|