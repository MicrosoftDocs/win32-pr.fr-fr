---
title: Structure MCI_VD_PLAY_PARMS (Mciapi. h)
description: La \_ structure des PARMS de lecture MCI VD contient des \_ \_ informations de position et de vitesse pour la \_ commande MCI Play pour les appareils videodisc.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- structure MCI_VD_PLAY_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c2aef6915d1e3cc325d5b9f8e1c7fe176a878c2d84080b5f8a77eaf034afc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783864"
---
# <a name="mci_vd_play_parms-structure"></a>\_Structure des \_ PARMS de lecture MCI VD \_

La structure des **\_ PARMS de \_ lecture \_ MCI VD** contient des informations de position et de vitesse pour la commande [**MCI \_ Play**](mci-play.md) pour les appareils videodisc.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position à partir de laquelle effectuer la lecture.

</dd> <dt>

**dwTo**
</dt> <dd>

Position de lecture.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Vitesse de lecture en images par seconde.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

Vous pouvez utiliser la structure des [**\_ \_ parms de lecture MCI**](mci-play-parms.md) à la place des **\_ \_ \_ parms de lecture MCI** , si vous n’utilisez pas les membres de données étendus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Structures MCI**](mci-structures.md)
</dt> <dt>

[**\_lecture MCI**](mci-play.md)
</dt> <dt>

[**\_jeux de lecture MCI \_**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

