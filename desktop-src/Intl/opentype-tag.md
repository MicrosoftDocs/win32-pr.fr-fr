---
description: Définit un tableau de 4 octets qui contient les valeurs ASCII 4 8 bits de l’espace, A-Z ou a-z pour identifier les balises de fonctionnalité de script, de langue et de police OpenType.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519804"
---
# <a name="opentype_tag"></a>\_balise OpenType

Définit un tableau de 4 octets qui contient les valeurs ASCII 4 8 bits de l’espace, A-Z ou a-z pour identifier les balises de fonctionnalité de script, de langue et de police OpenType.


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a>Notes

Les exemples suivants définissent des représentations de balises de fonctionnalités OpenType.

-   La balise de fonctionnalité pour la fonctionnalité de ligature est « Liga ».
-   Les balises de langue pour roumain, ourdou et persan sont respectivement « ROM », « URD » et « FAR ». Notez que chacune de ces balises se termine par un espace.
-   Les balises de script pour les scripts latins et arabes sont respectivement « LATN » et « arabe ».

Pour plus d’informations sur les balises de fonctionnalités OpenType et la spécification OpenType, consultez <https://www.microsoft.com/typography/otspec/featuretags.htm> .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| Composant redistribuable<br/>          | Usp10.dll version 1,600 ou supérieure onWindows velopper plus tard<br/>                |
| En-tête<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Structures Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




