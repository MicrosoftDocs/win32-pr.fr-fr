---
title: Structure MCI_OVLY_WINDOW_PARMS (Mciapi. h)
description: La \_ structure PARMS de la fenêtre OVLY MCI \_ contient des \_ informations de fenêtre pour la \_ commande de fenêtre MCI pour les périphériques de superposition vidéo.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Structure de MCI_OVLY_WINDOW_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941650"
---
# <a name="mci_ovly_window_parms-structure"></a>\_OVLY \_ fenêtre PARMS des fenêtres MCI \_

La structure PARMS de la **\_ \_ \_ fenêtre OVLY MCI** contient des informations de fenêtre pour la commande de [**\_ fenêtre MCI**](mci-window.md) pour les périphériques de superposition vidéo.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**hWnd**
</dt> <dd>

Handle vers la fenêtre d’affichage.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Commande Window-Display.

</dd> <dt>

**lpstrText**
</dt> <dd>

Titre de la fenêtre.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

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

[**\_fenêtre MCI**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

