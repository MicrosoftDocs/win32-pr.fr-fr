---
description: La table UIText contient les versions localisées de certaines chaînes utilisées dans l’interface utilisateur. Ces chaînes ne font pas partie d’une autre table. La table UIText est destinée aux chaînes qui n’ont pas d’emplacement logique dans une autre table.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Table UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111983"
---
# <a name="uitext-table"></a>Table UIText

La table UIText contient les versions localisées de certaines chaînes utilisées dans l’interface utilisateur. Ces chaînes ne font pas partie d’une autre table. La table UIText est destinée aux chaînes qui n’ont pas d’emplacement logique dans une autre table.

La table UIText contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| Clé    | [Identificateur](identifier.md) | O   | N        |
| Texte   | [Text](text.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel
</dt> <dd>

Clé unique qui identifie la chaîne particulière.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Financière
</dt> <dd>

Version localisée du type de la chaîne.

</dd> </dl>

## <a name="remarks"></a>Notes

Certains contrôles utilisent la table UIText comme source de chaînes. Pour plus d’informations sur les chaînes requises dans ce tableau pour chaque contrôle particulier, consultez les contrôles individuels dans la référence de l' [interface utilisateur](user-interface-reference.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



