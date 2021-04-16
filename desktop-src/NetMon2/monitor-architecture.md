---
description: L’illustration suivante montre la relation entre les analyses et les autres composants de l’architecture Moniteur réseau.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Analyser l’architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550911"
---
# <a name="monitor-architecture"></a><span data-ttu-id="0673b-103">Analyser l’architecture</span><span class="sxs-lookup"><span data-stu-id="0673b-103">Monitor Architecture</span></span>

<span data-ttu-id="0673b-104">L’illustration suivante montre la relation entre les [*analyses*](m.md) et les autres composants de l’architecture Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="0673b-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![relation entre les moniteurs et d’autres composants du moniteur réseau](images/nmarch2.png)

<span data-ttu-id="0673b-106">Le trafic réseau est collecté (sous forme de trames individuelles) à partir du pilote NDIS.</span><span class="sxs-lookup"><span data-stu-id="0673b-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="0673b-107">Le pilote de Moniteur réseau (Nmnt.sys) achemine ensuite les trames vers un fournisseur de paquets réseau (NPP), qui à son tour capture les données en temps réel.</span><span class="sxs-lookup"><span data-stu-id="0673b-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="0673b-108">Le NPP est une collection d’interfaces COM utilisées pour capturer des données.</span><span class="sxs-lookup"><span data-stu-id="0673b-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="0673b-109">Dans ce cas, l’interface [**IRTC**](irtc.md) est utilisée pour effectuer une capture en temps réel.</span><span class="sxs-lookup"><span data-stu-id="0673b-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="0673b-110">Le NPP est utilisé pour les captures retardées et en temps réel.</span><span class="sxs-lookup"><span data-stu-id="0673b-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="0673b-111">Pour les captures différées utilisées par les experts et les analyseurs, l’interface [**IDelaydC**](idelaydc.md) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="0673b-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="0673b-112">Le moniteur examine ensuite les données capturées en temps réel, en détectant les conditions réseau spécifiques et en générant les événements nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0673b-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="0673b-113">Trois autres composants sont utilisés par les applications de surveillance : l’outil de contrôle de l’analyse, le service de contrôle d’analyse (MCSVC) et le observateur d’événements :</span><span class="sxs-lookup"><span data-stu-id="0673b-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="0673b-114">L’outil de contrôle de l’analyse est utilisé pour gérer vos applications de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0673b-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="0673b-115">Cela comprend la configuration et l’exécution de toutes les applications du moniteur.</span><span class="sxs-lookup"><span data-stu-id="0673b-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="0673b-116">Le service de contrôle de l’analyse (MCSVC) déclenche des événements, fournit un lien de communication vers WMI pour l’affichage des événements et coordonne le traitement des opérations du moniteur.</span><span class="sxs-lookup"><span data-stu-id="0673b-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="0673b-117">Le observateur d’événements affiche les événements déclenchés par le service de contrôle de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="0673b-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0673b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0673b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0673b-119">**IMonitor**</span><span class="sxs-lookup"><span data-stu-id="0673b-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="0673b-120">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="0673b-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="0673b-121">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="0673b-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



