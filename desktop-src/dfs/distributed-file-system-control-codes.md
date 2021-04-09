---
title: Codes de contrôle système de fichiers DFS
description: système de fichiers DFS les codes de contrôle DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941121"
---
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="b7791-103">Codes de contrôle système de fichiers DFS</span><span class="sxs-lookup"><span data-stu-id="b7791-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="b7791-104">Les codes de contrôle du système de fichiers DFS (DFS) sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b7791-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b7791-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b7791-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b7791-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="b7791-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="b7791-107">Le code de contrôle [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) peut obtenir les mêmes informations que la fonction [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mais peut fournir de meilleures performances dans certaines configurations avec des latences élevées aux serveurs DFS.</span><span class="sxs-lookup"><span data-stu-id="b7791-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="b7791-108">Il n’est pas recommandé d’utiliser le code de contrôle **FSCTL_DFS_GET_PKT_ENTRY_STATE** , sauf s’il existe des problèmes de performances.</span><span class="sxs-lookup"><span data-stu-id="b7791-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="b7791-109">Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="b7791-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>