---
description: Si ce bit est défini sur un contrôle de texte, l’occurrence du caractère &\# 0034 ; &&\# 0034 ; dans une chaîne de texte s’affiche comme lui-même. Si ce bit n’est pas défini, le caractère suivant &\# 0034 ; &&\# 0034 ; dans la chaîne de texte est affiché sous la forme d’un caractère de soulignement.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix (attribut de contrôle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15345bb56ad85ec654cffe7a0bf2173973e032ac33aca633105d3a220647cf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065879"
---
# <a name="noprefix-control-attribute"></a>NoPrefix (attribut de contrôle)

Si ce bit est défini sur un contrôle de texte, l’occurrence du caractère « & » dans une chaîne de texte s’affiche comme lui-même. Si ce bit n’est pas défini, le caractère qui suit « & » dans la chaîne de texte est affiché sous la forme d’un caractère de soulignement.

## <a name="valid-controls"></a>Contrôles valides

[Text](text-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit de préfixe dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



