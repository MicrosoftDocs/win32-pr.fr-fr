---
description: Si ce bit est défini sur un contrôle de texte, l’occurrence du caractère &\# 0034 ; &&\# 0034 ; dans une chaîne de texte s’affiche comme lui-même. Si ce bit n’est pas défini, le caractère suivant &\# 0034 ; &&\# 0034 ; dans la chaîne de texte est affiché sous la forme d’un caractère de soulignement.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix (attribut de contrôle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201956"
---
# <a name="noprefix-control-attribute"></a>NoPrefix (attribut de contrôle)

Si ce bit est défini sur un contrôle de texte, l’occurrence du caractère « & » dans une chaîne de texte s’affiche comme lui-même. Si ce bit n’est pas défini, le caractère qui suit « & » dans la chaîne de texte est affiché sous la forme d’un caractère de soulignement.

## <a name="valid-controls"></a>Contrôles valides

[Text](text-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit de préfixe dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



