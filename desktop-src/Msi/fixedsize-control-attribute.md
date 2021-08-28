---
description: Si le bit de contrôle FixedSize est défini, l’image est rognée ou centrée dans le contrôle sans modifier sa forme ou sa taille.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Attribut de contrôle FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40094001115dc6e196e66075abe7ace7c93c8e715818ad34235f80caf8306a06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649699"
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



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit FixedSize dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

La définition du bit FixedSize n’a aucun effet sur une [case à cocher](checkbox-control.md), un [PUSHBUTTON](pushbutton-control.md)ou un [RadioButtonGroup](radiobuttongroup-control.md) si ni la [bitmap](bitmap-control-attribute.md) ni l' [icône](icon-control-attribute.md) n’a été définie.

La définition du bit FixedSize n’a aucun effet sur un contrôle Icon, ou un bouton de commande associé à une icône, [si les bits](iconsize-control-attribute.md) d’icône ne sont pas définis.

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



