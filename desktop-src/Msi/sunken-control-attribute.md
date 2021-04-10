---
description: Si ce bit est défini, le contrôle s’affiche avec une apparence 3D enfoncé.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Attribut de contrôle enfoncé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114158"
---
# <a name="sunken-control-attribute"></a>Attribut de contrôle enfoncé

Si ce bit est défini, le contrôle s’affiche avec une apparence 3D enfoncé. L’effet de ce bit de style est différent sur les différents contrôles et versions de Windows. Sur certains contrôles, il n’a aucun effet visible. Si le système ne prend pas en charge l’attribut de contrôle enfoncé, le contrôle est affiché dans le style visuel par défaut. Si ce bit n’est pas défini, le contrôle est affiché avec le style visuel par défaut.

## <a name="valid-controls"></a>Contrôles valides

Tous les contrôles.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit enfoncé dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



