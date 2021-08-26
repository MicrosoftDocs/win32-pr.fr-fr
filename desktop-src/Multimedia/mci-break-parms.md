---
title: Structure MCI_BREAK_PARMS (Mciapi. h)
description: La \_ structure des interruptions MCI \_ contient le code de clé virtuelle et les informations de fenêtre pour la \_ commande MCI Break.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- structure MCI_BREAK_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efaff8841e0e8ef0387535aa8d42723cf9477887511b7111f02a6ee0cb2b527b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039509"
---
# <a name="mci_break_parms-structure"></a>\_Structure des arrêts MCI \_

La structure des **\_ interruptions \_ MCI** contient le code de clé virtuelle et les informations de fenêtre pour la commande [**MCI \_ break**](mci-break.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**nVirtKey**
</dt> <dd>

Code de la touche virtuelle pour la touche arrêt.

</dd> <dt>

**hwndBreak**
</dt> <dd>

Handle de la fenêtre qui doit être la fenêtre active pour la détection des arrêts.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres. Les indicateurs suivants sont définis :

\_HWND de pause MCI \_

Valide le membre **hwndBreak** qui spécifie la fenêtre qui doit avoir le focus pour activer la détection de rupture.

\_touche pause \_ MCI

Valide le membre **nVirtKey** spécifiant le code de la touche virtuelle à utiliser pour la touche Attn.

\_Pause MCI \_

Désactive une clé d’arrêt existante.

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

[**\_Pause MCI**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

