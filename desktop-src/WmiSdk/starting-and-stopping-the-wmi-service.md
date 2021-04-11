---
description: WMI s’exécute en tant que service portant le nom d’affichage &\# 0034 ; Windows Management Instrumentation&\# 0034 ; et le nom du service &\# 0034 ; winmgmt&\# 0034 ;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Démarrage et arrêt du service WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202163"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="85d3b-103">Démarrage et arrêt du service WMI</span><span class="sxs-lookup"><span data-stu-id="85d3b-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="85d3b-104">WMI s’exécute en tant que service portant le nom d’affichage « Windows Management Instrumentation » et le nom de service « WinMgmt ».</span><span class="sxs-lookup"><span data-stu-id="85d3b-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="85d3b-105">WMI s’exécute automatiquement au démarrage du système sous le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="85d3b-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="85d3b-106">Si WMI n’est pas en cours d’exécution, il démarre automatiquement lorsque la première application ou le script de gestion demande une connexion à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="85d3b-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="85d3b-107">Plusieurs autres services dépendent du service WMI, en fonction de la version du système d’exploitation exécutée par le système.</span><span class="sxs-lookup"><span data-stu-id="85d3b-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="85d3b-108">Démarrage du service WinMgmt</span><span class="sxs-lookup"><span data-stu-id="85d3b-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="85d3b-109">La procédure suivante décrit comment démarrer le service WMI.</span><span class="sxs-lookup"><span data-stu-id="85d3b-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="85d3b-110">**Pour démarrer le service WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="85d3b-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="85d3b-111">À l’invite de commandes, entrez **net** **Start** **winmgmt** \[ */<switch>* \] .</span><span class="sxs-lookup"><span data-stu-id="85d3b-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="85d3b-112">Pour plus d’informations sur les commutateurs disponibles, consultez [winmgmt](winmgmt.md).</span><span class="sxs-lookup"><span data-stu-id="85d3b-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="85d3b-113">Vous utilisez le compte administrateur intégré ou un compte dans le groupe administrateurs s’exécutant avec des droits élevés pour démarrer le service WMI.</span><span class="sxs-lookup"><span data-stu-id="85d3b-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="85d3b-114">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="85d3b-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="85d3b-115">Les autres services qui dépendent du service WMI, tels que l’hôte de l’agent SMS ou le pare-feu Windows, ne sont pas redémarrés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="85d3b-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="85d3b-116">Arrêt du service WinMgmt</span><span class="sxs-lookup"><span data-stu-id="85d3b-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="85d3b-117">La procédure suivante décrit comment arrêter le service WMI.</span><span class="sxs-lookup"><span data-stu-id="85d3b-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="85d3b-118">**Pour arrêter le service WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="85d3b-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="85d3b-119">À l’invite de commandes, entrez **net stop winmgmt**.</span><span class="sxs-lookup"><span data-stu-id="85d3b-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="85d3b-120">D’autres services qui dépendent du service WMI s’arrêtent également, tels que l’hôte de l’agent SMS ou le pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="85d3b-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="85d3b-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="85d3b-121">Examples</span></span>

<span data-ttu-id="85d3b-122">La Galerie TechNet contient le [script de la surveillance du service WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), qui décrit comment arrêter par programmation et redémarrer le service WinMgmt avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85d3b-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85d3b-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85d3b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85d3b-124">Utilisation des outils de Command-Line WMI</span><span class="sxs-lookup"><span data-stu-id="85d3b-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



