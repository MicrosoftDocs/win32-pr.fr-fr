---
description: Spécifie le niveau de protection pour le contenu vidéo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Structure D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515187"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>D3DAUTHENTICATEDCHANNEL \_ , \_ structure d’indicateurs de protection

Spécifie le niveau de protection pour le contenu vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>Membres

<dl> <dt>

**ProtectionEnabled**
</dt> <dd>

Si 1, la protection du contenu vidéo est activée.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Si la valeur est 1, l’application requiert que la vidéo soit affichée à l’aide d’une superposition matérielle ou en mode exclusif plein écran.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé. Affectez à tous les bits la valeur zéro.

</dd> <dt>

**Valeur**
</dt> <dd>

Utilisez ce membre pour accéder à tous les bits de l’Union.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




