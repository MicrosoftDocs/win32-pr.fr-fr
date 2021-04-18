---
description: Un outil de fusion évalue la table ModuleAdminExecuteSequence, puis insère les actions calculées dans la table AdminExecuteSequence avec un numéro de séquence correct.
ms.assetid: 26cc5e15-8dfd-4bf5-8830-225164302278
title: Table ModuleAdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0f062f552f92ec667a2889d2bf26a98900e152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536545"
---
# <a name="moduleadminexecutesequence-table"></a>Table ModuleAdminExecuteSequence

Un outil de fusion évalue la table ModuleAdminExecuteSequence, puis insère les actions calculées dans la [table AdminExecuteSequence](adminexecutesequence-table.md) avec un numéro de séquence correct.

La table ModuleAdminExecuteSequence contient les colonnes suivantes.



| Colonne     | Type                         | Clé | Nullable |
|------------|------------------------------|-----|----------|
| Action     | [Identificateur](identifier.md) | O   | N        |
| Séquence   | [Integer](integer.md)       |     | O        |
| BaseAction | [Identificateur](identifier.md) |     | O        |
| After      | [Integer](integer.md)       |     | O        |
| Condition  | [Condition](condition.md)   |     | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Action à insérer dans la séquence. Fait référence à l’une des [actions standard](standard-actions.md)du programme d’installation ou à une entrée de la table ou de la table de [boîtes de dialogue](dialog-table.md) [CustomAction](customaction-table.md) du module de fusion.

Si une [action standard](standard-actions.md) est utilisée dans la colonne action d’une table de séquence de module de fusion, les colonnes BaseAction et after de cet enregistrement doivent avoir la valeur null.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Numéro de séquence d’une action standard. Si une action ou une boîte de dialogue personnalisée est entrée dans la colonne action de cette ligne, ce champ doit avoir la valeur null.

Lorsque vous utilisez des [actions standard](standard-actions.md) dans les tables de séquence de module de fusion, la valeur dans la colonne Sequence doit être le numéro de séquence d’action recommandé. Si le numéro de séquence du module de fusion diffère de celui de la même action dans le tableau séquence de fichiers. msi, l’outil de fusion utilise le numéro de séquence du fichier. msi. Consultez les séquences suggérées dans [à l’aide d’une table de séquences](using-a-sequence-table.md) pour connaître les numéros de séquence recommandés pour les actions standard.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La colonne BaseAction peut contenir une action standard, une action personnalisée spécifiée dans la table d’actions personnalisée du module de fusion ou une boîte de dialogue spécifiée dans la table de boîte de dialogue du module. La colonne BaseAction est une clé dans la colonne action de ce tableau. Il ne peut pas s’agir d’une clé étrangère dans une autre table ou table de fusion du fichier. msi. Cela signifie que chaque action standard, action personnalisée ou boîte de dialogue figurant dans la colonne BaseAction doit également figurer dans la colonne action d’un autre enregistrement dans ce tableau.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Postérieur
</dt> <dd>

Valeur booléenne indiquant si l’action vient avant ou après BaseAction.



| Valeur | Signification                          |
|-------|----------------------------------|
| 0     | Action à venir avant BaseAction |
| 1     | Action à venir après BaseAction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Instruction conditionnelle qui indique si l’action est exécutée. NULL prend la valeur true.

</dd> </dl>

## <a name="remarks"></a>Notes

Si cette table est présente, la [table AdminExecuteSequence](adminexecutesequence-table.md) doit également être présente dans le module de fusion.

 

 



