---
title: Communication entre le client NAP et le composant côté serveur
description: Communication entre le client NAP et le composant côté serveur
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380290"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="b1fe0-103">Communication entre le client NAP et le composant côté serveur</span><span class="sxs-lookup"><span data-stu-id="b1fe0-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="b1fe0-104">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b1fe0-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b1fe0-105">Le composant agent NAP peut communiquer avec le composant serveur d’administration NAP par le biais du processus suivant :</span><span class="sxs-lookup"><span data-stu-id="b1fe0-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="b1fe0-106">L’agent NAP transmet le SSoH à la EC NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="b1fe0-107">La EC NAP transmet le SSoH aux NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="b1fe0-108">La protection NAP des e/s transmet le SSoH au service NPS (Network Policy Server).</span><span class="sxs-lookup"><span data-stu-id="b1fe0-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="b1fe0-109">Le service NPS transmet le SSoH au serveur d’administration NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="b1fe0-110">Un agent SHA peut communiquer avec son validateur d’intégrité de l’un des processus suivants :</span><span class="sxs-lookup"><span data-stu-id="b1fe0-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="b1fe0-111">L’algorithme SHA passe son SoH à l’agent NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="b1fe0-112">L’agent NAP passe l’SoH contenue dans SSoH à la EC NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="b1fe0-113">La EC NAP passe l’SoH aux NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="b1fe0-114">La protection d’accès réseau (NAP) transmet la déclaration d’intégrité au serveur d’administration NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="b1fe0-115">Le serveur d’administration NAP transmet la SoH à l’SHV.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="b1fe0-116">La figure ci-dessous illustre le processus de communication entre les composants clients NAP et les composants côté serveur NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![architecture de communication entre le client et le serveur dans la plateforme NAP](images/nap-client-to-server-comm.png)

<span data-ttu-id="b1fe0-118">Le serveur d’administration NAP peut communiquer avec l’agent NAP par le biais du processus suivant :</span><span class="sxs-lookup"><span data-stu-id="b1fe0-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="b1fe0-119">Le serveur d’administration NAP transmet le SoHRs au service NPS.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="b1fe0-120">Le service NPS transmet le SSoHR aux NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="b1fe0-121">La protection NAP des e/s transmet le SSoHR à la EC NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="b1fe0-122">La EC NAP transmet le SSoHR à l’agent NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="b1fe0-123">Le SHV peut communiquer avec son SHA correspondant par le biais du processus suivant :</span><span class="sxs-lookup"><span data-stu-id="b1fe0-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="b1fe0-124">Le SHV transmet son SoHR au serveur d’administration NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="b1fe0-125">Le serveur d’administration NAP transmet le SoHR au service NPS.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="b1fe0-126">Le service NPS transmet le SoHR, contenu dans le SSoHR, aux NAP ES.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="b1fe0-127">La protection NAP des e/s transmet le SoHR à la EC NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="b1fe0-128">La EC NAP transmet le SoHR à l’agent NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="b1fe0-129">L’agent NAP transmet le SoHR à l’agent SHA.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="b1fe0-130">La figure ci-dessous illustre le processus de communication entre les composants côté serveur NAP et les composants clients NAP.</span><span class="sxs-lookup"><span data-stu-id="b1fe0-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![architecture des communications de serveur à client dans la plateforme NAP](images/nap-server-to-client-comm.png)

 

 




