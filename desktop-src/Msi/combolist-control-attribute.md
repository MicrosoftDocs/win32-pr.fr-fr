---
description: Si le bit de contrôle ComboList est défini sur une zone de liste déroulante, le champ d’édition est remplacé par un champ de texte statique. Cela empêche un utilisateur d’entrer une nouvelle valeur et oblige l’utilisateur à choisir uniquement l’une des valeurs prédéfinies.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Attribut de contrôle ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092181"
---
# <a name="combolist-control-attribute"></a>Attribut de contrôle ComboList

Si le bit de contrôle ComboList est défini sur une zone de liste déroulante, le champ d’édition est remplacé par un champ de texte statique. Cela empêche un utilisateur d’entrer une nouvelle valeur et oblige l’utilisateur à choisir uniquement l’une des valeurs prédéfinies.

Si ce bit n’est pas défini, la zone de liste déroulante contient un champ d’édition.

## <a name="valid-controls"></a>Contrôles valides

[ComboBox](combobox-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Description                     |
|---------|-------------|---------------------------------|
| 131 072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit ComboList dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



