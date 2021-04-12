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
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385127"
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

## <a name="remarks"></a>Notes

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

 

 





