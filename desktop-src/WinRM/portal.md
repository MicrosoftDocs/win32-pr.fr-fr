---
title: gestion à distance de Windows
description: Windows Remote Management (Windows Remote Management) est l’implémentation Microsoft du protocole WS-Management, un protocole SOAP standard, compatible avec un pare-feu qui permet l’interopérabilité du matériel et des systèmes d’exploitation de différents fournisseurs.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows Remote Management (WinRM), page de démarrage
- Gestion des services Web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941022"
---
# <a name="windows-remote-management"></a><span data-ttu-id="a9a42-105">gestion à distance de Windows</span><span class="sxs-lookup"><span data-stu-id="a9a42-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="a9a42-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="a9a42-106">Purpose</span></span>

<span data-ttu-id="a9a42-107">La gestion à distance de Windows (WinRM) est l’implémentation Microsoft du [protocole Gestion des services web](ws-management-protocol.md), un protocole SOAP (Simple Object Access Protocol) standard, compatible avec un pare-feu qui permet l’interaction entre du matériel et des systèmes d’exploitation de différents fabricants.</span><span class="sxs-lookup"><span data-stu-id="a9a42-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="a9a42-108">La spécification de protocole WS-Management permet aux systèmes d’accéder et d’échanger des informations de gestion à travers une infrastructure informatique.</span><span class="sxs-lookup"><span data-stu-id="a9a42-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="a9a42-109">WinRM et l' [*interface de gestion de plateforme intelligente (IPMI)*](windows-remote-management-glossary.md), ainsi que le [collecteur d’événements](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) , sont des composants des fonctionnalités de [gestion matérielle de Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="a9a42-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a9a42-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="a9a42-110">Where applicable</span></span>

<span data-ttu-id="a9a42-111">Vous pouvez utiliser les objets de script WinRM, l’outil en ligne de commande WinRM ou l’outil en ligne de commande Windows Remote Shell WinRS pour obtenir des données de gestion à partir d’ordinateurs locaux et distants qui peuvent avoir des [*contrôleurs de gestion*](windows-remote-management-glossary.md)de la carte de contrôleurs BMC.</span><span class="sxs-lookup"><span data-stu-id="a9a42-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a9a42-112">Si l’ordinateur exécute une version du système d’exploitation Windows qui comprend WinRM, les données de gestion sont fournies par [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="a9a42-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="a9a42-113">Vous pouvez également obtenir des données système et matériel d’implémentations du protocole Gestion des services Web qui exécutent des systèmes d’exploitation autres que Windows dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="a9a42-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="a9a42-114">WinRM établit une session avec un ordinateur distant via le protocole Gestion des services Web SOAP plutôt que via DCOM, comme le fait WMI.</span><span class="sxs-lookup"><span data-stu-id="a9a42-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="a9a42-115">Les données retournées au protocole Gestion des services Web sont au format XML plutôt que des objets.</span><span class="sxs-lookup"><span data-stu-id="a9a42-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="a9a42-116">Le fournisseur WMI de l' [interface IPMI (Intelligent Platform Management Interface)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) est un fournisseur WMI standard avec des classes qui obtiennent les données de capteur BMC des ordinateurs équipés du matériel approprié.</span><span class="sxs-lookup"><span data-stu-id="a9a42-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="a9a42-117">Les données IPMI sont accessibles via l’API de script WinRM, les [scripts](/windows/desktop/WmiSdk/scripting-api-for-wmi)WMI ou les API [com](/windows/desktop/WmiSdk/com-api-for-wmi) .</span><span class="sxs-lookup"><span data-stu-id="a9a42-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a9a42-118">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a9a42-118">Developer audience</span></span>

<span data-ttu-id="a9a42-119">L’audience du développeur est le professionnel de l’informatique qui écrit des scripts pour automatiser la gestion des serveurs ou le développeur ISV qui obtient des données pour les applications de gestion.</span><span class="sxs-lookup"><span data-stu-id="a9a42-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a9a42-120">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="a9a42-120">Run-time requirements</span></span>

<span data-ttu-id="a9a42-121">WinRM fait partie du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a9a42-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="a9a42-122">Toutefois, pour obtenir des données à partir d’ordinateurs distants, vous devez configurer un [*écouteur*](windows-remote-management-glossary.md#l)WinRM.</span><span class="sxs-lookup"><span data-stu-id="a9a42-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="a9a42-123">Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="a9a42-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="a9a42-124">Si un contrôleur BMC est détecté au démarrage du système, le fournisseur IPMI se charge ; Sinon, les objets de script WinRM et l’outil en ligne de commande WinRM sont toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="a9a42-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9a42-125">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a9a42-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a9a42-126">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="a9a42-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="a9a42-127">Liaison à la spécification du protocole WS-Management public, à l’architecture WinRM, à la relation avec WMI, à la gestion du matériel avec le fournisseur IPMI, à la configuration et à l’installation.</span><span class="sxs-lookup"><span data-stu-id="a9a42-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="a9a42-128">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="a9a42-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="a9a42-129">Prise en main de l’API de script WinRM et de la gestion du matériel.</span><span class="sxs-lookup"><span data-stu-id="a9a42-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="a9a42-130">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="a9a42-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="a9a42-131">Liste des interfaces de script définies par Microsoft Web Services for Management (WS-Management) Automation et les définitions de classe des classes WMI créées par le fournisseur IPMI et les classes qui communiquent avec le pilote IPMI pour obtenir les données du contrôleur de gestion de la [carte de gestion (BMC)](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a42-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 