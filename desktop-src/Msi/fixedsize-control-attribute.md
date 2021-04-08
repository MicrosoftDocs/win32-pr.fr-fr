---
description: Si le bit de contrôle FixedSize est défini, l’image est rognée ou centrée dans le contrôle sans modifier sa forme ou sa taille.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Attribut de contrôle FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751141"
---
# <a name="fixedsize-control-attribute"></a>Attribut de contrôle FixedSize

Si le bit de contrôle FixedSize est défini, l’image est rognée ou centrée dans le contrôle sans modifier sa forme ou sa taille.

Si ce bit n’est pas défini, l’image est étirée pour s’ajuster au contrôle.

## <a name="valid-controls"></a>Contrôles valides

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Icône](icon-control.md)

[Boutons](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                            |
|---------|-------------|-------------------------------------|
| 1 048 576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit FixedSize dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

La définition du bit FixedSize n’a aucun effet sur une [case à cocher](checkbox-control.md), un [PUSHBUTTON](pushbutton-control.md)ou un [RadioButtonGroup](radiobuttongroup-control.md) si ni la [bitmap](bitmap-control-attribute.md) ni l' [icône](icon-control-attribute.md) n’a été définie.

La définition du bit FixedSize n’a aucun effet sur un contrôle Icon, ou un bouton de commande associé à une icône, [si les bits](iconsize-control-attribute.md) d’icône ne sont pas définis.

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



