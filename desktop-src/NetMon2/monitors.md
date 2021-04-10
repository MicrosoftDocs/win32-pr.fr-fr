---
description: Une analyse est une bibliothèque de liens dynamiques (DLL) qui examine les captures en temps réel du trafic réseau.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Analyses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951264"
---
# <a name="monitors"></a><span data-ttu-id="8a726-103">Analyses</span><span class="sxs-lookup"><span data-stu-id="8a726-103">Monitors</span></span>

<span data-ttu-id="8a726-104">Une analyse est une bibliothèque de liens dynamiques (DLL) qui examine les captures en temps réel du trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="8a726-104">A monitor is a dynamic-link library (DLL) that examines real-time captures of network traffic.</span></span> <span data-ttu-id="8a726-105">Il recherche des conditions prédéfinies, puis génère des événements lorsque ces conditions sont détectées.</span><span class="sxs-lookup"><span data-stu-id="8a726-105">It searches for pre-defined conditions and then generates events when those conditions are detected.</span></span> <span data-ttu-id="8a726-106">Par exemple, un événement peut être déclenché en cas de tentative d’interruption du réseau, lorsqu’un poste de travail non autorisé est en charge d’adresses IP ou en cas de défaillance d’un routeur.</span><span class="sxs-lookup"><span data-stu-id="8a726-106">For example, an event may be fired when a network break-in is attempted, when a rogue workstation is handing out IP addresses, or when a router fails.</span></span>

> [!Note]  
> <span data-ttu-id="8a726-107">Si vous devez effectuer des analyses détaillées sur les données réseau qui nécessitent une analyse après capture, vous devez utiliser des applications d' [*analyse*](p.md) et d' [*experts*](e.md) .</span><span class="sxs-lookup"><span data-stu-id="8a726-107">If you need to perform detailed analyses on network data that requires a post-capture analysis, you must use [*expert*](e.md) and [*parser*](p.md) applications.</span></span>

 

<span data-ttu-id="8a726-108">Le [*service de contrôle d’analyse*](m.md) (MCSVC) fournit l’infrastructure permettant de gérer vos analyses.</span><span class="sxs-lookup"><span data-stu-id="8a726-108">The [*Monitor Control Service*](m.md) (MCSVC) provides the framework for managing your monitors.</span></span> <span data-ttu-id="8a726-109">Il fournit des fonctions pour charger les dll du moniteur et une interface de communication à l’outil de contrôle de l’analyse afin que vous puissiez créer, configurer, démarrer, arrêter et désactiver plusieurs instances de vos moniteurs.</span><span class="sxs-lookup"><span data-stu-id="8a726-109">It provides functions to load the monitor DLLs, and a communications interface to the Monitor Control Tool so that you can create, configure, start, stop, and disable multiple instances of your monitors.</span></span>

<span data-ttu-id="8a726-110">Les analyses s’exécutent dans deux threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8a726-110">Monitors run in two threads of execution.</span></span> <span data-ttu-id="8a726-111">Le MCSVC fournit le premier thread, qui fournit le contrôle direct de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a726-111">The MCSVC provides the first thread, which provides direct control of the monitor.</span></span> <span data-ttu-id="8a726-112">Le deuxième thread est fourni par le [*fournisseur de paquets réseau*](n.md) (NPP), qui permet de transmettre les données réseau capturées, les statistiques et l’état de la capture du NPP à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="8a726-112">The second thread is provided by the [*network packet provider*](n.md) (NPP), which provides a way to pass the captured network data, statistics, and the status of the capture from the NPP back to the monitor.</span></span>

<span data-ttu-id="8a726-113">Plusieurs instances du même moniteur peuvent exister pour chaque interface NPP au moment de l’exécution utilisée pour capturer des données.</span><span class="sxs-lookup"><span data-stu-id="8a726-113">More than one instance of the same monitor can exist for each run-time NPP interface used to capture data.</span></span>

 

 



