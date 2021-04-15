---
title: Traçage réseau dans Windows 7
description: Windows 7 s’étend sur l’infrastructure de diagnostic réseau (NDF) pour fournir une méthode rapide pour résoudre les problèmes de connectivité réseau en permettant la collecte de toutes les informations nécessaires en une seule étape et en tirant parti d’Suivi d’v nements pour Windows (ETW) pour consigner les paquets d’événements réseau dans un fichier unique.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382800"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="d0dd0-103">Traçage réseau dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0dd0-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="d0dd0-104">À mesure que la complexité de la pile de mise en réseau augmente, il est souvent difficile de suivre et de diagnostiquer rapidement les problèmes au sein de la pile.</span><span class="sxs-lookup"><span data-stu-id="d0dd0-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="d0dd0-105">Windows 7 s’étend sur l’infrastructure de diagnostic réseau (NDF) pour fournir une méthode rapide pour résoudre les problèmes de connectivité réseau en permettant la collecte de toutes les informations nécessaires en une seule étape et en tirant parti d' [suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour consigner les événements réseau & les paquets dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="d0dd0-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="d0dd0-106">Les événements et les paquets associés sont regroupés pour une activité donnée, par exemple la navigation dans un site Web, sur les différents composants de la pile de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="d0dd0-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="d0dd0-107">La sortie de ce processus est un fichier journal de suivi d’événements (ETL).</span><span class="sxs-lookup"><span data-stu-id="d0dd0-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="d0dd0-108">En autorisant l’affichage à la fois de tous les événements liés à une activité spécifique dans ce fichier, le temps nécessaire pour isoler et diagnostiquer les problèmes réseau peut être très réduit.</span><span class="sxs-lookup"><span data-stu-id="d0dd0-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d0dd0-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d0dd0-109">In This Section</span></span>



| <span data-ttu-id="d0dd0-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d0dd0-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0dd0-111">Traçage réseau dans Windows 7 : architecture</span><span class="sxs-lookup"><span data-stu-id="d0dd0-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="d0dd0-112">Outils de résolution des problèmes à l’aide du suivi réseau dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0dd0-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="d0dd0-113">Traçage réseau dans Windows 7 : scénarios</span><span class="sxs-lookup"><span data-stu-id="d0dd0-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 