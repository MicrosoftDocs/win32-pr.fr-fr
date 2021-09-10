---
title: Structure MCI_STATUS_PARMS (Mciapi. h)
description: La \_ \_ structure de l’état de MCI contient des informations sur la \_ commande d’État MCI.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- structure MCI_STATUS_PARMS Windows multimédia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363908"
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

## <a name="remarks"></a>Remarques

L' \_ indicateur d’élément d’État MCI \_ doit être défini dans le paramètre *fdwCommand* de la fonction [**MciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider le membre **dwItem** , qui doit contenir l’une des constantes indiquant les informations d’État demandées.

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

[**\_État MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

