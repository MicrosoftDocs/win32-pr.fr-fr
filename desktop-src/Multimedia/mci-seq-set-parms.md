---
title: Structure MCI_SEQ_SET_PARMS (Mciapi. h)
description: La \_ structure MCI Seq \_ Set \_ PARMS contient des informations pour la \_ commande MCI Set pour les périphériques MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- structure MCI_SEQ_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363787"
---
# <a name="mci_seq_set_parms-structure"></a>MCI \_ Seq \_ définir la \_ structure des PARMS

La structure **MCI \_ Seq \_ Set \_ PARMS** contient des informations pour la commande [**MCI \_ Set**](mci-set.md) pour les périphériques MIDI Sequencer.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Format d’heure de Sequencer.

</dd> <dt>

**dwAudio**
</dt> <dd>

Canal de sortie audio.

</dd> <dt>

**dwTempo**
</dt> <dd>

Tempo.

</dd> <dt>

**dwPort**
</dt> <dd>

Port.

</dd> <dt>

**dwSlave**
</dt> <dd>

Type de synchronisation utilisé par Sequencer pour l’opération subordonnée.

</dd> <dt>

**dwMaster**
</dt> <dd>

Type de synchronisation utilisé par Sequencer pour l’opération maître.

</dd> <dt>

**dwOffset**
</dt> <dd>

Décalage des données.

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

[**jeu de MCI \_**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

