---
description: la table MsiShortcutProperty permet au programme d’installation de windows de définir des propriétés pour les raccourcis qui sont également Windows les objets Shell.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Table MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7cf51d8016cdc87008a6cc9a20daee1f35131af7ea0f5827c67da7f45a6e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944426"
---
# <a name="msishortcutproperty-table"></a>Table MsiShortcutProperty

la table MsiShortcutProperty permet au programme d’installation de windows de définir des propriétés pour les raccourcis qui sont également Windows les objets [Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . à partir de Windows Vista et Windows Server 2008, le shell Windows fournit une Interface IPropertyStore pour les objets shell tels que les raccourcis. un package Windows Installer 5,0 s’exécutant sur Windows Server 2008 R2 ou Windows 7 peut définir ces propriétés lors de l’installation du raccourci.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette table est disponible à partir de Windows Installer 5,0.

La table MsiShortcutProperty contient les colonnes suivantes.



| Colonne              | Type                         | Clé | Nullable |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identificateur](identifier.md) | O   | N        |
| Gestionnaires\_          | [Identificateur](identifier.md) | N   | N        |
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

Valeur de chaîne qui fournit des informations pour la structure [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . les informations contenues dans ce champ doivent faire référence au nom canonique d’une propriété inscrite auprès du système de propriétés Windows. pour plus d’informations sur le système de propriétés Windows, consultez [vue d’ensemble du système de propriétés](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Valeur de chaîne qui fournit des informations pour la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

Plusieurs propriétés peuvent être définies sur un raccourci. Si la même propriété est définie plusieurs fois sur le même raccourci, la valeur est définie dans un ordre non spécifié.

Windows Le programme d’installation peut définir des propriétés de raccourci uniquement lorsque le raccourci est installé ou réinstallé. Un correctif qui ne réinstalle pas un raccourci qui a déjà été installé ne met pas à jour les propriétés du raccourci. Un correctif peut mettre à jour les propriétés en incluant un tableau de [raccourcis](shortcut-table.md) dans le package correctif et en réinstallant le raccourci.

## <a name="remarks"></a>Remarques

[Windows Installer Message d’erreur](windows-installer-error-messages.md) 1946 est retourné en tant qu’avertissement et l’installation se poursuit, si Windows Installer ne parvient pas à définir une propriété de raccourci spécifiée dans la table MsiShortcutProperty.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
</dl>

 

 
