---
description: L’action InstallExecute exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecute ou de l’action InstallExecuteAgain.
ms.assetid: a124e9fb-f9fa-4ed3-8f32-4f1fab392530
title: Action InstallExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76417a4f188849f9a5af5a90b08e1f4bb5977afc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012072"
---
# <a name="installexecute-action"></a>Action InstallExecute

L’action InstallExecute exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecute ou de l’action [InstallExecuteAgain](installexecuteagain-action.md). L’action InstallExecute met à jour le système sans mettre fin à la transaction.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallExecute intervient entre l' [action InstallInitialize](installinitialize-action.md) et l’action [InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L' [action InstallExecuteAgain](installexecuteagain-action.md) effectue la même opération que l’action InstallExecute. Étant donné que les tables de séquence n’ont qu’une seule clé primaire, la colonne d’action, la même action ne peut pas être répétée dans une table de séquences particulière. Il existe deux actions qui font la même chose, InstallExecute et InstallExecuteAgain, dans les cas où la fonctionnalité de InstallExecute est nécessaire deux fois dans la [table InstallExecuteSequence](installexecutesequence-table.md). Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

 

 



