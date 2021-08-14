---
description: Si ce bit est défini sur un contrôle d’édition, le programme d’installation crée un contrôle d’édition de plusieurs lignes avec une barre de défilement verticale.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Attribut de contrôle multiligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474bf8a9b765f402924a554c9da064a8c60a01f6af910a3fd24c81d377978a93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943430"
---
# <a name="multiline-control-attribute"></a>Attribut de contrôle multiligne

Si ce bit est défini sur un [contrôle d’édition](edit-control.md), le programme d’installation crée un contrôle d’édition de plusieurs lignes avec une barre de défilement verticale.

Si ce bit n’est pas défini, il spécifie l’affichage d’un contrôle d’édition normal.

## <a name="valid-controls"></a>Contrôles valides

[Contrôle d’édition](edit-control.md).



| Decimal | Valeur hexadécimale | Constante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit multiligne dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



