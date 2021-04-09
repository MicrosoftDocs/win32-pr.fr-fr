---
description: Si ce bit est défini sur un contrôle ProgressBar, la barre est dessinée sous la forme d’une série de petits rectangles. Si ce bit n’est pas défini, la barre de l’indicateur de progression est dessinée sous la forme d’un rectangle continu unique.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Attribut de contrôle Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2242dde671484274be946802ba4fd4c1cfd687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867038"
---
# <a name="progress95-control-attribute"></a>Attribut de contrôle Progress95

Si ce bit est défini sur un [contrôle ProgressBar](progressbar-control.md), la barre est dessinée sous la forme d’une série de petits rectangles. Si ce bit n’est pas défini, la barre de l’indicateur de progression est dessinée sous la forme d’un rectangle continu unique.

## <a name="valid-controls"></a>Contrôles valides

[Barre de progression](progressbar-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit Progress95 dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



