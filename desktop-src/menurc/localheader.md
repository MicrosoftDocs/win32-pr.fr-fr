---
title: LOCALHEADER, structure
description: Contient les coordonnées x et y d’une zone réactive associée au curseur identifié par une structure RESDIR. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Menus de la structure LOCALHEADER et autres ressources
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384848"
---
# <a name="localheader-structure"></a>LOCALHEADER, structure

Contient les coordonnées x et y d’une zone réactive associée au curseur identifié par une structure [**RESDIR**](resdir.md) . La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**xHotSpot**
</dt> <dd>

Type : **Word**

</dd> <dd>

Coordonnée x de la zone réactive du curseur, en pixels.

</dd> <dt>

**yHotSpot**
</dt> <dd>

Type : **Word**

</dd> <dd>

Coordonnée y de la zone réactive du curseur, en pixels.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure **LOCALHEADER** est la première donnée écrite dans la ressource de [ \_ curseur RT](/windows/desktop/menurc/resource-types) si une structure [**RESDIR**](resdir.md) contient des informations sur un curseur.

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

[**RESDIR**](resdir.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> </dl>

 

