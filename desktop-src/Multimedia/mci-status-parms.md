---
title: Structure MCI_STATUS_PARMS (Mciapi. h)
description: La \_ \_ structure de l’état de MCI contient des informations sur la \_ commande d’État MCI.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Structure de MCI_STATUS_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941783"
---
# <a name="mci_status_parms-structure"></a>Structure de l' \_ État MCI \_

La structure de l' **\_ état \_ de MCI** contient des informations sur la commande d' [**\_ État MCI**](mci-status.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Contient des informations sur le retour.

</dd> <dt>

**dwItem**
</dt> <dd>

Fonctionnalité en cours d’interrogation.

</dd> <dt>

**dwTrack**
</dt> <dd>

Longueur ou nombre de pistes.

</dd> </dl>

## <a name="remarks"></a>Notes

L' \_ indicateur d’élément d’État MCI \_ doit être défini dans le paramètre *fdwCommand* de la fonction [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider le membre **dwItem** , qui doit contenir l’une des constantes indiquant les informations d’État demandées.

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

[**\_État MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

