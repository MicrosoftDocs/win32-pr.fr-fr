---
title: RESDIR, structure
description: Contient des informations sur une icône individuelle ou un composant curseur dans un groupe de ressources. Il existe une structure RESDIR pour chaque composant de groupe. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Menus de la structure RESDIR et autres ressources
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9033e1f30e8f497b202fa8e3f84d4ecb582bb60c166f396a50ce194c9783075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825579"
---
# <a name="resdir-structure"></a>RESDIR, structure

Contient des informations sur une icône individuelle ou un composant curseur dans un groupe de ressources. Il existe une structure **RESDIR** pour chaque composant de groupe. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a>Membres

<dl> <dt>

**Icône**
</dt> <dd>

Type : **[ **ICONRESDIR**](iconresdir.md)**

</dd> <dd>

La largeur, la hauteur et le nombre de couleurs de l’icône indiquée.

</dd> <dt>

**Curseur**
</dt> <dd>

Type : **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Largeur et hauteur du curseur indiqué.

</dd> <dt>

**Appareils**
</dt> <dd>

Type : **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Nombre de plans de couleur dans l’icône ou la bitmap de curseur.

</dd> <dt>

**BitCount**
</dt> <dd>

Type : **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Nombre de bits par pixel dans l’icône ou la bitmap de curseur.

</dd> <dt>

**BytesInRes**
</dt> <dd>

Type : **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Taille de la ressource, en octets.

</dd> <dt>

**IconCursorId**
</dt> <dd>

Type : **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

Icône ou curseur avec un identificateur ordinal unique.

</dd> </dl>

## <a name="remarks"></a>Remarques

Une ou plusieurs structures **RESDIR** suivent immédiatement la structure [**NEWHEADER**](newheader.md) dans le fichier. res. Le membre **ResCount** de la structure **NEWHEADER** spécifie le nombre de structures **RESDIR** . Notez que la structure **RESDIR** se compose d’une structure [**ICONRESDIR**](iconresdir.md) ou d’une structure [**CURSORDIR**](cursordir.md) suivie des **plans**, **BitCount**, **BytesInRes** et **IconCursorId** . Si la **structure RESDIR** contient des informations sur un curseur, les deux premiers **mots** que le compilateur de ressources écrit dans la ressource de [ \_ curseur RT](/windows/desktop/menurc/resource-types) sont les membres **xHotSpot** et **yHotSpot** de la structure [**LOCALHEADER**](localheader.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**ICONRESDIR**](iconresdir.md)
</dt> <dt>

[**LOCALHEADER**](localheader.md)
</dt> <dt>

[**NEWHEADER**](newheader.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

