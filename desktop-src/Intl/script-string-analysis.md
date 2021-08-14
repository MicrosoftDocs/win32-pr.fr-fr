---
description: Définit une partie ou l’ensemble des attributs de caractères, des glyphes, des largeurs d’avance, des positions x et y, des mappages caractère à glyphe, etc., pour une chaîne.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390298"
---
# <a name="script_string_analysis"></a>\_analyse de chaîne de script \_

Définit une partie ou l’ensemble des attributs de caractères, des glyphes, des largeurs d’avance, des positions x et y, des mappages caractère à glyphe, etc., pour une chaîne.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Remarques

Il s’agit d’une structure opaque qui est allouée dynamiquement et récupérée par [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). Elle est également requise pour toutes les autres fonctions **ScriptString \*** .

Étant donné que l’analyse peut être volumineuse, il est important que votre application appelle [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) dès qu’elle a terminé avec la chaîne.

## <a name="requirements"></a>Configuration requise



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

 

 




