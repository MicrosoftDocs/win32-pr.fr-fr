---
description: Le tableau de cases à cocher répertorie les valeurs des cases à cocher.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Table de cases à cocher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544809"
---
# <a name="checkbox-table"></a>Table de cases à cocher

Le tableau de cases à cocher répertorie les valeurs des cases à cocher.

La table de cases à cocher contient les colonnes suivantes.



| Colonne   | Type                         | Clé | Nullable |
|----------|------------------------------|-----|----------|
| Propriété | [Identificateur](identifier.md) | O   | N        |
| Valeur    | [Correct](formatted.md)   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriété
</dt> <dd>

Propriété nommée à être liée à cet élément.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Chaîne de valeur associée à cet élément.

</dd> </dl>

## <a name="remarks"></a>Notes

Si la case à cocher est activée, la propriété correspondante est définie sur la valeur spécifiée. Si aucune valeur n’est spécifiée ou si cette table n’existe pas, la propriété est définie sur sa valeur d’origine lorsque la case à cocher est activée. Si la valeur d’origine est null, la propriété a la valeur « 1 ».

Le contenu de la colonne de valeur est mis en forme par la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) lorsque le contrôle est créé. Par conséquent, il peut contenir n’importe quelle expression que la fonction **MsiFormatRecord** peut interpréter. La colonne de valeur est mise en forme uniquement lorsque le contrôle est créé et n’est pas mise à jour si une propriété impliquée dans une expression est modifiée pendant la durée de vie du contrôle.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



