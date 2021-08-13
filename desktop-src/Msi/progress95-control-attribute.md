---
description: Si ce bit est défini sur un contrôle ProgressBar, la barre est dessinée sous la forme d’une série de petits rectangles. Si ce bit n’est pas défini, la barre de l’indicateur de progression est dessinée sous la forme d’un rectangle continu unique.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Attribut de contrôle Progress95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e6fa8f2c0cd0e1622db4bb406d3ada1b63229e92b60a35e915bf0dacc72fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627348"
---
# <a name="progress95-control-attribute"></a>Attribut de contrôle Progress95

Si ce bit est défini sur un [contrôle ProgressBar](progressbar-control.md), la barre est dessinée sous la forme d’une série de petits rectangles. Si ce bit n’est pas défini, la barre de l’indicateur de progression est dessinée sous la forme d’un rectangle continu unique.

## <a name="valid-controls"></a>Contrôles valides

[ProgressBar](progressbar-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit Progress95 dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



