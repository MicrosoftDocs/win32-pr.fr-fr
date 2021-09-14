---
description: Définit une partie ou l’ensemble des attributs de caractères, des glyphes, des largeurs d’avance, des positions x et y, des mappages caractère à glyphe, etc., pour une chaîne.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121890"
---
# <a name="script_string_analysis"></a>\_analyse de chaîne de script \_

Définit une partie ou l’ensemble des attributs de caractères, des glyphes, des largeurs d’avance, des positions x et y, des mappages caractère à glyphe, etc., pour une chaîne.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Notes

Il s’agit d’une structure opaque qui est allouée dynamiquement et récupérée par [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). Elle est également requise pour toutes les autres fonctions **ScriptString \*** .

Étant donné que l’analyse peut être volumineuse, il est important que votre application appelle [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) dès qu’elle a terminé avec la chaîne.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| Composant redistribuable<br/>          | Internet Explorer 5 ou version ultérieure onWindows me/98/95<br/>                         |
| En-tête<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Structures Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




