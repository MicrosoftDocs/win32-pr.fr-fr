---
description: Si ce bit est défini sur un contrôle d’édition, le programme d’installation crée un contrôle d’édition de plusieurs lignes avec une barre de défilement verticale.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Attribut de contrôle multiligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011837"
---
# <a name="multiline-control-attribute"></a>Attribut de contrôle multiligne

Si ce bit est défini sur un [contrôle d’édition](edit-control.md), le programme d’installation crée un contrôle d’édition de plusieurs lignes avec une barre de défilement verticale.

Si ce bit n’est pas défini, il spécifie l’affichage d’un contrôle d’édition normal.

## <a name="valid-controls"></a>Contrôles valides

[Contrôle d’édition](edit-control.md).



| Decimal | Valeur hexadécimale | Constante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit multiligne dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



