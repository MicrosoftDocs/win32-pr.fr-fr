---
description: L’action ExecuteAction lance la séquence d’exécution à l’aide de la propriété EXECUTEACTION pour déterminer le type d’installation à effectuer.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Action ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091293"
---
# <a name="executeaction-action"></a>Action ExecuteAction

L’action ExecuteAction lance la séquence d’exécution à l’aide de la propriété [**ExecuteAction**](executeaction.md) pour déterminer le type d’installation à effectuer.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Cette action doit être séquencée une fois que toutes les informations nécessaires pour commencer l’installation sont terminées. Les actions supplémentaires peuvent être séquencées après l’action ExecuteAction dans la [table InstallUISequence](installuisequence-table.md)et la [table AdminUISequence](adminuisequence-table.md). Une séquence commence généralement par des actions d' [*évaluation du coût*](c-gly.md) , telles que l' [action CostInitialize](costinitialize-action.md), suivie des actions de l’interface utilisateur, puis de l’action ExecuteAction.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action ExecuteAction est exécutée avec des privilèges système si le service d’installation est activé. Les actions de niveau supérieur, telles que l' [action d’installation](install-action.md), l' [action de publication](advertise-action.md)et l' [action d’administration](admin-action.md) incluent une logique interne qui détermine si l’appel de l’action ExecuteAction requiert la séquence d’exécution ou la séquence d’interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table InstallUISequence](installuisequence-table.md)
</dt> <dt>

[Table AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Action CostInitialize](costinitialize-action.md)
</dt> </dl>

 

 



