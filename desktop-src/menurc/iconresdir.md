---
title: ICONRESDIR, structure
description: Contient les dimensions et le format de couleur d’une image d’icône individuelle dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Menus de la structure ICONRESDIR et autres ressources
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f81f8b0a530e7c6c85f2ad1749e0a7373f68b0bf902b71a86889b92184806ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034277"
---
# <a name="iconresdir-structure"></a>ICONRESDIR, structure

Contient les dimensions et le format de couleur d’une image d’icône individuelle dans un groupe de ressources. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>Membres

<dl> <dt>

**Width**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Largeur de l’icône, en pixels. Les valeurs acceptables sont 16, 32 et 64.

</dd> <dt>

**Height**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Hauteur, en pixels, de l’icône. Les valeurs acceptables sont 16, 32 et 64.

</dd> <dt>

**ColorCount**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Nombre de couleurs dans l’icône. Les valeurs acceptables sont 2, 8 et 16.

</dd> <dt>

**reserved**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Réservé doit être défini sur la même valeur que celle du champ réservé dans l’en-tête du fichier icône.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **ICONRESDIR** est transmise dans la structure [**RESDIR**](resdir.md) si la structure **RESDIR** décrit une icône.

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

 

 





