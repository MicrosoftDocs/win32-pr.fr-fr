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
# <a name="distributed-file-system-control-codes"></a>Codes de contrôle système de fichiers DFS

Les codes de contrôle du système de fichiers DFS (DFS) sont les suivants :

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

Le code de contrôle [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) peut obtenir les mêmes informations que la fonction [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mais peut fournir de meilleures performances dans certaines configurations avec des latences élevées aux serveurs DFS. Il n’est pas recommandé d’utiliser le code de contrôle **FSCTL_DFS_GET_PKT_ENTRY_STATE** , sauf s’il existe des problèmes de performances.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

</dd> </dl>