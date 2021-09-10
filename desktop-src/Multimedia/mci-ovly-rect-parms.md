---
title: Structure MCI_OVLY_RECT_PARMS (Mciapi. h)
description: La \_ structure MCI OVLY \_ rect \_ PARMS contient des informations de positionnement pour les \_ commandes MCI put et MCI pour les \_ périphériques de superposition vidéo.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- structure MCI_OVLY_RECT_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363771"
---
# <a name="mci_ovly_rect_parms-structure"></a>MCI \_ OVLY \_ rect \_ PARMS, structure

La structure **MCI \_ OVLY \_ rect \_ PARMS** contient des informations de positionnement pour les commandes [**MCI \_ put**](mci-put.md) et [**MCI \_**](mci-where.md) pour les périphériques de superposition vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**Release**
</dt> <dd>

Rectangle contenant les informations de positionnement. Les structures [Rect](/previous-versions//ms536136(v=vs.85)) sont gérées différemment dans MCI et dans d’autres parties de Windows ; dans MCI, **RC. Right** contient la largeur du rectangle et **RC. Bottom** contient sa hauteur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Spécifications



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

[**\_put MCI**](mci-put.md)
</dt> <dt>

[**MCI \_ où**](mci-where.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECTANGULAIRE](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

