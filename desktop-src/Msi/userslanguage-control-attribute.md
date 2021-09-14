---
description: Si cet indicateur de bit est défini, les polices sont créées à l’aide de la page de codes de l’interface utilisateur par défaut de l’utilisateur. Si l’indicateur binaire n’est pas défini, les polices sont créées à l’aide de la page de codes de la base de données.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Attribut de contrôle UsersLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009601"
---
# <a name="userslanguage-control-attribute"></a>Attribut de contrôle UsersLanguage

Si cet indicateur de bit est défini, les polices sont créées à l’aide de la page de codes de l’interface utilisateur par défaut de l’utilisateur. Si l’indicateur binaire n’est pas défini, les polices sont créées à l’aide de la page de codes de la base de données.

## <a name="valid-controls"></a>Contrôles valides

[Text](text-control.md)

 

[ListBox](listbox-control.md)

 

[ComboBox](combobox-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                |
|---------|-------------|-----------------------------------------|
| 1 048 576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

## <a name="remarks"></a>Notes

Cet attribut de contrôle peut être utilisé pour afficher le texte que l’utilisateur a entré dans un contrôle [Edit](edit-control.md) ou [PathEdit](pathedit-control.md) .

Le contrôle d’édition, le contrôle PathEdit, le contrôle [DirectoryList](directorylist-control.md) et le [contrôle DirectoryCombo](directorycombo-control.md) utilisent toujours les polices créées dans la page de codes de l’interface utilisateur par défaut de l’utilisateur. Cela peut entraîner des problèmes si des langues supplémentaires ont été installées sur le système d’exploitation. Dans ce cas, les polices sur l’ordinateur peuvent ne pas être en mesure de représenter tous les caractères dans les langues ajoutées. pour déterminer les polices qui peuvent être utilisées, recherchez les valeurs dans **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SystemLink**.

Pour plus d’informations, consultez [contrôles](controls.md)et [attributs](control-attributes.md) .

 

 



