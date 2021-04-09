---
description: Le tableau d’affichage répertorie les contrôles de tableau blanc affichés dans l’interface utilisateur complète.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tableau d’panneaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951752"
---
# <a name="billboard-table"></a>Tableau d’panneaux

Le tableau d’affichage répertorie les contrôles de tableau [blanc](billboard-control.md) affichés dans l’interface utilisateur complète.

La table du tableau blanc contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Blanc | [Identificateur](identifier.md) | O   | N        |
| Fonctionnalité\_ | [Identificateur](identifier.md) | N   | N        |
| Action    | [Identificateur](identifier.md) | N   | O        |
| Classement  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Blanc
</dt> <dd>

Nom du contrôle de tableau [blanc](billboard-control.md).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé externe de la première colonne de la [table de fonctionnalités](feature-table.md). Le panneau s’affiche uniquement si cette fonctionnalité est en cours d’installation.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom d’une action. Le panneau s’affiche pendant les messages de progression reçus de cette action.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Commandé
</dt> <dd>

Si plusieurs panneaux d’affichage correspondent à une action, ils sont affichés dans l’ordre défini par cette colonne. Ce nombre ne doit pas être négatif.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



