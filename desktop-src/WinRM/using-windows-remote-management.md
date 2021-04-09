---
title: Utilisation de Windows Remote Management
description: Windows Remote Management est conçu pour améliorer la gestion du matériel dans un environnement réseau avec différents appareils exécutant différents systèmes d’exploitation.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102000"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="b4022-103">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b4022-103">Using Windows Remote Management</span></span>

<span data-ttu-id="b4022-104">Windows Remote Management est conçu pour améliorer la gestion du matériel dans un environnement réseau avec différents appareils exécutant différents systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b4022-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="b4022-105">La conception du service repose sur la surveillance et la gestion des ordinateurs distants par implémentation d’un protocole standard interopérable.</span><span class="sxs-lookup"><span data-stu-id="b4022-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="b4022-106">Étant donné que l' [API de script WinRM](winrm-scripting-api.md) et l' [API C++ WinRM](winrm-c---api.md) implémentent et modélisent étroitement les opérations définies pour le protocole WS-Management, les scripts et les applications reçoivent des flux de données XML en réponse aux requêtes.</span><span class="sxs-lookup"><span data-stu-id="b4022-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="b4022-107">Les paramètres d’entrée des appels de méthode doivent être construits en XML.</span><span class="sxs-lookup"><span data-stu-id="b4022-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="b4022-108">Vous pouvez utiliser les méthodes de l’API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) pour afficher ou construire des chaînes XML.</span><span class="sxs-lookup"><span data-stu-id="b4022-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="b4022-109">Pour obtenir un exemple, consultez [affichage de la sortie XML des scripts WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="b4022-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="b4022-110">La liste suivante contient des rubriques qui décrivent comment utiliser les scripts WinRM :</span><span class="sxs-lookup"><span data-stu-id="b4022-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="b4022-111">Détection de la prise en charge du protocole WS-Management par un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="b4022-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="b4022-112">Obtention de données à partir de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="b4022-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="b4022-113">Obtention de données à partir d’un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="b4022-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="b4022-114">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="b4022-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="b4022-115">Interrogation d’instances spécifiques d’une ressource</span><span class="sxs-lookup"><span data-stu-id="b4022-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="b4022-116">Affichage de la sortie XML des scripts WinRM</span><span class="sxs-lookup"><span data-stu-id="b4022-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="b4022-117">Activité de suivi WinRM</span><span class="sxs-lookup"><span data-stu-id="b4022-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="b4022-118">Étant donné que WinRM obtient des données via [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), vous pouvez suivre l’activité WMI qui résulte des messages WinRM.</span><span class="sxs-lookup"><span data-stu-id="b4022-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="b4022-119">À compter de Windows Vista, le service WMI n’utilise plus les [fichiers journaux WMI](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="b4022-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="b4022-120">Au lieu de cela, il utilise le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) et les événements sont disponibles par le biais de l’interface utilisateur **Observateur d’événements** ou de l’outil en ligne de commande Evtutil.</span><span class="sxs-lookup"><span data-stu-id="b4022-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4022-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4022-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4022-122">Gestion à distance de Windows</span><span class="sxs-lookup"><span data-stu-id="b4022-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="b4022-123">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b4022-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b4022-124">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b4022-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="b4022-125">Scripts dans Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b4022-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 