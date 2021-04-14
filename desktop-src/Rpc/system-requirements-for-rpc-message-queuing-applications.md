---
title: Configuration système requise pour les applications RPC-Message Queuing
description: Pour utiliser le transport de mise en file d’attente de messages dans une application client/serveur RPC, le serveur et les ordinateurs clients doivent disposer de la plateforme du système d’exploitation appropriée et du logiciel Message Queuing installé.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382491"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="a7c47-103">Configuration système requise pour les applications RPC-Message Queuing</span><span class="sxs-lookup"><span data-stu-id="a7c47-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="a7c47-104">Pour utiliser le transport de mise en file d’attente de messages dans une application client/serveur RPC, le serveur et les ordinateurs clients doivent disposer de la plateforme du système d’exploitation appropriée et du logiciel Message Queuing installé.</span><span class="sxs-lookup"><span data-stu-id="a7c47-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="a7c47-105">La configuration requise pour les ordinateurs serveurs est la suivante :</span><span class="sxs-lookup"><span data-stu-id="a7c47-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="a7c47-106">Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7c47-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="a7c47-107">SQL Server version 6,5 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7c47-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="a7c47-108">Message Queuing contrôleur principal d’entreprise ou contrôleur principal de site.</span><span class="sxs-lookup"><span data-stu-id="a7c47-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="a7c47-109">DLL de transport RPC côté serveur (RpcMqSvr.dll).</span><span class="sxs-lookup"><span data-stu-id="a7c47-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="a7c47-110">La configuration requise pour les ordinateurs clients est la suivante :</span><span class="sxs-lookup"><span data-stu-id="a7c47-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="a7c47-111">Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7c47-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="a7c47-112">Client Microsoft Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="a7c47-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="a7c47-113">DLL de transport RPC côté client (RpcMqCl.dll).</span><span class="sxs-lookup"><span data-stu-id="a7c47-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="a7c47-114">Lorsque les composants MSMQ sont installés sur les ordinateurs clients et serveurs, les registres système sont automatiquement configurés pour inclure le protocole de transport [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) Message-Queuing pour les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="a7c47-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="a7c47-115">Pour générer votre application RPC-MSMQ, vous devez disposer des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a7c47-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="a7c47-116">Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a7c47-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="a7c47-117">MIDL version 3.1.76 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7c47-117">MIDL version 3.1.76 or later.</span></span>

 

 