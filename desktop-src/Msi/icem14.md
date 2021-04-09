---
description: ICEM14 valide la colonne valeur de la table ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114331"
---
# <a name="icem14"></a>ICEM14

ICEM14 valide la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

## <a name="result"></a>Résultats

ICEM14 publie les erreurs suivantes.



| Error                                                                                                                                                         | Signification                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Chaîne de remplacement dans la colonne ModuleSubstitution. Value de la ligne \[ 1 \] . \[ 2 \] . \[ 3 \] est introuvable dans la table ModuleConfiguration.                                 | \[1 \] . \[ 2 \] . \[ 3 \] fait référence à une clé primaire *table. Row. colonne* pour une ligne de la table ModuleSubstitution. Le modèle de mise en forme dans le champ valeur de cette ligne ne correspond pas à une ligne d’attributs configurables dans la [table ModuleConfiguration](moduleconfiguration-table.md).                                                            |
| Dans la table ModuleSubstitution de la ligne \[ 1 \] . \[ 2 \] . \[ 3 \] , un élément configurable est indiqué dans la table'% s'. La table'% s’ne doit pas contenir d’éléments configurables. | L’une des tables suivantes est indiquée dans la colonne table de la table ModuleSubstitution : [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)ou [ModuleSignature](modulesignature-table.md). Ces tables ne peuvent pas contenir de champs configurables. |
| Dans la table ModuleSubstitution de la ligne \[ 1 \] . \[ 2 \] . \[ 3 \] , une chaîne de remplacement vide est spécifiée.                                                               | Le modèle de mise en forme dans le champ valeur de cette ligne ne correspond pas à une ligne d’attributs configurables dans la [table ModuleConfiguration](moduleconfiguration-table.md).                                                                                                                                                                    |



 

ICEM14 publie l’avertissement suivant.



| Avertissement                                                                  | Signification                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| La table ModuleSubstitution existe mais la table ModuleConfiguration est manquante | La table ModuleConfiguration est absente. |



 

## <a name="table-used-during-execution"></a>Table utilisée pendant l’exécution

[Table ModuleSubstitution](modulesubstitution-table.md)

[Table ModuleConfiguration](moduleconfiguration-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



