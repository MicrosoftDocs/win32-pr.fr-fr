---
description: Les analyses sont conçues pour utiliser les Windows Management Instrumentation (WMI) pour déclencher des événements sur des ordinateurs locaux ou distants.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Surveiller les événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485145"
---
# <a name="monitor-events"></a><span data-ttu-id="65ff0-103">Surveiller les événements</span><span class="sxs-lookup"><span data-stu-id="65ff0-103">Monitor Events</span></span>

<span data-ttu-id="65ff0-104">Les analyses sont conçues pour utiliser les [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) pour déclencher des événements sur des ordinateurs locaux ou distants.</span><span class="sxs-lookup"><span data-stu-id="65ff0-104">Monitors are designed to use [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to fire events to local or remote computers.</span></span>

> [!Note]  
> <span data-ttu-id="65ff0-105">Étant donné que les analyses utilisent une capture en temps réel, elles peuvent uniquement capturer des données sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="65ff0-105">Because monitors use a real-time capture they can only capture data at the local computer.</span></span> <span data-ttu-id="65ff0-106">Il s’agit d’une limitation de l’interface **IRTC** du fournisseur de paquets réseau.</span><span class="sxs-lookup"><span data-stu-id="65ff0-106">This is a limitation of the network packet provider's **IRTC** interface.</span></span> <span data-ttu-id="65ff0-107">Toutefois, à l’aide d’événements WMI, les données capturées peuvent être examinées localement, tandis que les événements peuvent être envoyés à des ordinateurs locaux ou distants.</span><span class="sxs-lookup"><span data-stu-id="65ff0-107">However, by using WMI events, the captured data can be examined locally while events can be sent to local or remote computers.</span></span>

 

<span data-ttu-id="65ff0-108">Les analyses ne communiquent pas directement avec WMI.</span><span class="sxs-lookup"><span data-stu-id="65ff0-108">Monitors do not communicate directly with WMI.</span></span> <span data-ttu-id="65ff0-109">Le [*service de contrôle d’analyse*](m.md) (MCSVC) fournit une interface (appelée [IMonitorEventer](imonitoreventer.md)), que l’analyse peut utiliser pour obtenir une structure de données d’événement et la remplir avec les informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="65ff0-109">The [*Monitor Control Service*](m.md) (MCSVC) provides an interface (called [IMonitorEventer](imonitoreventer.md)), which the monitor can use to obtain an event data structure and fill it with the relevant information.</span></span> <span data-ttu-id="65ff0-110">Le MCSVC peut ensuite envoyer la structure des données d’événement à WMI, qui à son tour déclenche l’événement.</span><span class="sxs-lookup"><span data-stu-id="65ff0-110">The MCSVC can then send the event data structure to WMI, which in turn fires the event.</span></span>

 

 
