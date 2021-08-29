---
title: CURSORDIR, structure
description: Contient les dimensions d’une image de curseur individuelle dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Menus de la structure CURSORDIR et autres ressources
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7194d6af764a9f66a2bf1a059f9c387cde13bb05728a7e96ccec470fa3650c81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602169"
---
# <a name="cursordir-structure"></a>CURSORDIR, structure

Contient les dimensions d’une image de curseur individuelle dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a>Membres

<dl> <dt>

**Width**
</dt> <dd>

Type : **Word**

</dd> <dd>

Largeur, en pixels, du curseur. Les valeurs acceptables sont 16, 32 et 64.

</dd> <dt>

**Height**
</dt> <dd>

Type : **Word**

</dd> <dd>

Hauteur, en pixels, du curseur. Les valeurs acceptables sont 16, 32 et 64.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **CURSORDIR** est transmise dans la structure [**RESDIR**](resdir.md) si la structure **RESDIR** décrit un curseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

 





