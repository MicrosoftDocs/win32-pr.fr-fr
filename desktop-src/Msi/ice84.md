---
description: ICE84 vérifie la table AdvtExecuteSequence, la table AdminExecuteSequence et la table InstallExecuteSequence pour vérifier que les actions standard suivantes n’ont pas été définies avec des conditions dans le champ condition.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af31c343db973481bd69599fadc9c632bbc6dc58a473a69015b3eb0fbe781d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894999"
---
# <a name="ice84"></a>ICE84

ICE84 vérifie la table [AdvtExecuteSequence](advtexecutesequence-table.md), la [table AdminExecuteSequence](adminexecutesequence-table.md)et la [table InstallExecuteSequence](installexecutesequence-table.md) pour vérifier que les [actions standard](standard-actions.md) suivantes n’ont pas été définies avec des conditions dans le champ condition.

-   [Action CostInitialize](costinitialize-action.md)
-   [Action CostFinalize](costfinalize-action.md)
-   [Action FileCost](filecost-action.md)
-   [Action InstallValidate](installvalidate-action.md)
-   [Action InstallInitialize](installinitialize-action.md)
-   [Action InstallFinalize](installfinalize-action.md)
-   [Action ProcessComponents](processcomponents-action.md)
-   [Action PublishFeatures](publishfeatures-action.md)
-   [Action PublishProduct](publishproduct-action.md)
-   [Action RegisterProduct](registerproduct-action.md)
-   [Action UnpublishFeatures](unpublishfeatures-action.md)

Si des conditions sont trouvées, ICE84 publie un avertissement.

## <a name="result"></a>Résultat

ICE84 publie l’avertissement suivant.



| Erreur ICE84                                                             | Description                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| L’action « \[ 1 \] » trouvée dans la table% s est une action requise avec une condition. | Une action requise a été créée avec une condition. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



