---
title: Détection et prévention de la latence de réplication
description: La latence de réplication est un fait de la vie dans un système distribué faiblement couplé.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671346"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="89be3-103">Détection et prévention de la latence de réplication</span><span class="sxs-lookup"><span data-stu-id="89be3-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="89be3-104">La latence de réplication est un fait de la vie dans un système distribué faiblement couplé.</span><span class="sxs-lookup"><span data-stu-id="89be3-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="89be3-105">Les applications doivent prendre en charge ce.</span><span class="sxs-lookup"><span data-stu-id="89be3-105">Applications must accommodate this.</span></span> <span data-ttu-id="89be3-106">La meilleure façon de prendre en charge la latence de réplication consiste à concevoir des applications pour réduire les effets.</span><span class="sxs-lookup"><span data-stu-id="89be3-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="89be3-107">L’application idéale pour les annuaires :</span><span class="sxs-lookup"><span data-stu-id="89be3-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="89be3-108">N’est pas sensible au décalage de version.</span><span class="sxs-lookup"><span data-stu-id="89be3-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="89be3-109">Ne dépend pas des relations entre plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="89be3-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="89be3-110">N’a aucune exigence de cohérence intra-ou inter-objets.</span><span class="sxs-lookup"><span data-stu-id="89be3-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="89be3-111">Les applications et services qui correspondent à ce profil n’ont pas besoin de la latence de réplication.</span><span class="sxs-lookup"><span data-stu-id="89be3-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="89be3-112">D’autres applications doivent être conçues avec une latence de réplication à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="89be3-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="89be3-113">La clé de la réussite de la conception d’une telle application est la reconnaissance du processus de réplication.</span><span class="sxs-lookup"><span data-stu-id="89be3-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="89be3-114">Étapes effectuées au moment de la conception pour réduire les dépendances entre les objets et réduire le nombre de retards de mise à jour partielle au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="89be3-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="89be3-115">Les approches de la latence de la réplication sont divisées en deux classes : des stratégies d’évitement qui réduisent l’impact des stratégies de latence et de détection qui permettent à une application de détecter les États induits par la latence.</span><span class="sxs-lookup"><span data-stu-id="89be3-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




