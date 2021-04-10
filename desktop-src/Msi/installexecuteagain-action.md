---
description: L’action InstallExecuteAgain exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecuteAgain ou de la dernière action InstallExecute.
ms.assetid: 60ff844f-f8bf-4a55-9523-ba526dac9e29
title: Action InstallExecuteAgain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57865c3eec28afa454e440e056d1ee964528f889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951100"
---
# <a name="installexecuteagain-action"></a>Action InstallExecuteAgain

L’action InstallExecuteAgain exécute un script contenant toutes les opérations de la séquence d’action depuis le début de l’installation ou de la dernière action InstallExecuteAgain ou de la dernière [action InstallExecute](installexecute-action.md). L’action InstallExecute met à jour le système sans mettre fin à la transaction. InstallExecuteAgain effectue la même opération que l' [action InstallExecute](installexecute-action.md) , mais ne doit être utilisée qu’après InstallExecute.

InstallExecuteAgain doit toujours être défini de manière à ce qu’il ne s’exécute pas pendant la suppression. Pour plus d’informations, consultez [utilisation des propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallExecute intervient entre l' [action InstallInitialize](installinitialize-action.md) et l’action [InstallFinalize](installfinalize-action.md).

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action InstallExecuteAgain effectue la même opération que l' [action InstallExecute](installexecute-action.md). Étant donné que les tables de séquence n’ont qu’une seule clé primaire, la colonne d’action, la même action ne peut pas être répétée dans une table de séquences particulière. Il existe deux actions qui font la même chose, InstallExecute et InstallExecuteAgain, dans les cas où la fonctionnalité de InstallExecute est nécessaire deux fois dans la [table InstallExecuteSequence](installexecutesequence-table.md). Pour plus d’informations, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

 

 



