---
title: Structure MCI_VD_ESCAPE_PARMS (Mciapi. h)
description: La structure de l' \_ échappement MCI VD \_ \_ contient la commande envoyée à un appareil pour la \_ commande d’échappement MCI pour les appareils videodisc.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- structure MCI_VD_ESCAPE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f9a0fef0e60168d4539756c741527d751fd726ab3d2472cdbaf3b080784e70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783844"
---
# <a name="mci_vd_escape_parms-structure"></a>Structure de l' \_ échappement MCI VD \_ \_

La structure de l' **\_ \_ \_ échappement MCI VD** contient la commande envoyée à un appareil pour la commande d' [**\_ échappement MCI**](mci-escape.md) pour les appareils videodisc.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**lpstrCommand**
</dt> <dd>

Commande à envoyer à l’appareil.

</dd> </dl>

## <a name="remarks"></a>Remarques

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

[**\_échappement MCI**](mci-escape.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

