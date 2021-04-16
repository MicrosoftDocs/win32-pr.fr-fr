---
title: Terminologie des canaux essentiels
description: Comme les autres types de paramètres pour les appels de procédure distante, les canaux peuvent être \ dans \ ou \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508069"
---
# <a name="essential-pipe-terminology"></a><span data-ttu-id="1fa80-103">Terminologie des canaux essentiels</span><span class="sxs-lookup"><span data-stu-id="1fa80-103">Essential Pipe Terminology</span></span>

<span data-ttu-id="1fa80-104">Comme les autres types de paramètres pour les appels de procédure distante, les canaux peuvent être \[ [**des**](/windows/desktop/Midl/in) \] paramètres in ou \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="1fa80-104">Like other types of parameters to remote procedure calls, pipes can be \[ [**in**](/windows/desktop/Midl/in)\] or \[ [**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="1fa80-105">Étant donné que le serveur contrôle le transfert de données via un canal, les canaux avec l' \[  \] attribut in sont dits pour *extraire* des données vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="1fa80-105">Since the server controls the transfer of data through a pipe, pipes with the \[**in**\] attribute are said to *pull* data to the server.</span></span> <span data-ttu-id="1fa80-106">De même, les canaux de sortie *poussent* les données du serveur vers le client.</span><span class="sxs-lookup"><span data-stu-id="1fa80-106">Similarly, output pipes *push* data from the server to the client.</span></span> <span data-ttu-id="1fa80-107">Les procédures de transfert de données sont appelées « *procédure pull* » et « *Push Procedure »*, respectivement.</span><span class="sxs-lookup"><span data-stu-id="1fa80-107">The procedures that do the data transfer are called the *pull procedure* and the *push procedure*, respectively.</span></span>

<span data-ttu-id="1fa80-108">Le compilateur MIDL génère les procédures push et pull pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="1fa80-108">The MIDL compiler generates the push and pull procedures for the server.</span></span> <span data-ttu-id="1fa80-109">En outre, il gère l’allocation des tampons de données en mémoire.</span><span class="sxs-lookup"><span data-stu-id="1fa80-109">In addition, it manages the allocation of data buffers in memory.</span></span> <span data-ttu-id="1fa80-110">Toutefois, le client doit fournir ses propres procédures push et pull.</span><span class="sxs-lookup"><span data-stu-id="1fa80-110">However, the client must provide its own push and pull procedures.</span></span> <span data-ttu-id="1fa80-111">Il doit également fournir une procédure pour l’allocation des mémoires tampons utilisées par le canal.</span><span class="sxs-lookup"><span data-stu-id="1fa80-111">It must also provide a procedure for allocating the memory buffers used by the pipe.</span></span> <span data-ttu-id="1fa80-112">Celles-ci sont appelées automatiquement au moment approprié par le stub client.</span><span class="sxs-lookup"><span data-stu-id="1fa80-112">These are automatically called at the appropriate time by the client stub.</span></span> <span data-ttu-id="1fa80-113">La procédure d’allocation est souvent appelée procédure Alloc ou Alloc.</span><span class="sxs-lookup"><span data-stu-id="1fa80-113">The allocation procedure is often called the alloc procedure or the alloc function.</span></span>

 

 