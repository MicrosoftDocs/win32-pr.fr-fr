---
description: Le tableau TextStyle répertorie les différents styles de police utilisés dans les contrôles contenant du texte.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Table TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951320"
---
# <a name="textstyle-table"></a>Table TextStyle

Le tableau TextStyle répertorie les différents styles de police utilisés dans les contrôles contenant du texte.

La table TextStyle contient les colonnes suivantes.



| Colonne    | Type                               | Clé | Nullable |
|-----------|------------------------------------|-----|----------|
| TextStyle | [Identificateur](identifier.md)       | O   | N        |
| FaceName  | [Text](text.md)                   | N   | N        |
| Taille      | [Integer](integer.md)             | N   | N        |
| Couleur     | [DoubleInteger](doubleinteger.md) | N   | O        |
| StyleBits | [Integer](integer.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle
</dt> <dd>

Cette colonne correspond au nom du style de police. Ce nom peut être incorporé dans la chaîne de texte pour indiquer une modification de style. Notez que le nom de style de police utilisé dans ce champ ne doit pas se terminer par les caractères suivants : \_ UL. Consultez [Ajout de contrôles et de texte](adding-controls-and-text.md).

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

Chaîne qui indique le nom de la police. La longueur de la chaîne ne doit pas dépasser 31 caractères.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Corps
</dt> <dd>

Taille de la police mesurée en points. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Couleur
</dt> <dd>

Cette colonne spécifie la couleur de texte affichée par un [contrôle de texte](text-control.md). Tous les autres types de contrôles utilisent toujours la couleur de texte par défaut. La valeur placée dans cette colonne doit être calculée à l’aide de la formule suivante : 65536 \* Blue + 256 \* vert + rouge, où Red, Green et Blue se trouvent dans la plage de 0-255. La valeur ne doit pas dépasser 16777215, qui est la valeur de blanc. La valeur est 0 pour le noir, 255 pour rouge, 65280 pour le vert, 16711680 pour bleu et 8421504 pour gris. Si vous laissez le champ vide, vous spécifiez la couleur par défaut.

Ne placez pas de [contrôles de texte](text-control.md) transparent par-dessus les bitmaps de couleur. Le texte peut ne pas être visible si l’utilisateur modifie le modèle de couleurs d’affichage. Par exemple, le texte peut devenir invisible si l’utilisateur définit le paramètre de contraste élevé pour l’accessibilité.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Combinaison de bits indiquant la mise en forme du texte.

Les bits de style individuels ont les valeurs suivantes.



| Constante                             | Valeur hexadécimale | Decimal | Style      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Gras       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Italique     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Souligner  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Strike |



 

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



