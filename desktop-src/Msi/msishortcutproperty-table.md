---
description: La table MsiShortcutProperty permet au programme d’installation de Windows de définir des propriétés pour les raccourcis qui sont également des objets de shell Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Table MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529799"
---
# <a name="msishortcutproperty-table"></a>Table MsiShortcutProperty

La table MsiShortcutProperty permet au programme d’installation de Windows de définir des propriétés pour les raccourcis qui sont également des objets de [shell Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . À compter de Windows Vista et de Windows Server 2008, le shell Windows fournit une interface IPropertyStore pour les objets Shell tels que les raccourcis. Un package Windows Installer 5,0 s’exécutant sur Windows Server 2008 R2 ou Windows 7 peut définir ces propriétés lors de l’installation du raccourci.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. Cette table est disponible à partir de Windows Installer 5,0.

La table MsiShortcutProperty contient les colonnes suivantes.



| Colonne              | Type                         | Clé | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identificateur](identifier.md) | O   | N        |
| Raccourci\_          | [Identificateur](identifier.md) | N   | N        |
| PropertyKey         | [Correct](formatted.md)   | N   | N        |
| PropVariantValue    | [Correct](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

Identificateur unique de cette ligne de la table MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Gestionnaires\_
</dt> <dd>

Clé dans le tableau de [raccourcis](shortcut-table.md) qui identifie le raccourci ayant un jeu de propriétés.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Valeur de chaîne qui fournit des informations pour la structure [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . Les informations contenues dans ce champ doivent faire référence au nom canonique d’une propriété inscrite auprès du système de propriétés Windows. Pour plus d’informations sur le système de propriétés Windows, consultez [vue d’ensemble du système de propriétés](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Valeur de chaîne qui fournit des informations pour la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

Plusieurs propriétés peuvent être définies sur un raccourci. Si la même propriété est définie plusieurs fois sur le même raccourci, la valeur est définie dans un ordre non spécifié.

Windows Installer pouvez définir des propriétés de raccourci uniquement lors de l’installation ou de la réinstallation du raccourci. Un correctif qui ne réinstalle pas un raccourci qui a déjà été installé ne met pas à jour les propriétés du raccourci. Un correctif peut mettre à jour les propriétés en incluant un tableau de [raccourcis](shortcut-table.md) dans le package correctif et en réinstallant le raccourci.

## <a name="remarks"></a>Notes

[Windows Installer message d’erreur](windows-installer-error-messages.md) 1946 est retourné en tant qu’avertissement et l’installation se poursuit, si Windows Installer ne parvient pas à définir une propriété de raccourci spécifiée dans la table MsiShortcutProperty.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
</dl>

 

 
