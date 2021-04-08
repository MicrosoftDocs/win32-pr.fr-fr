---
title: Structure MCI_WAVE_SET_PARMS (Mciapi. h)
description: La structure de l' \_ ensemble des sons MCI Wave \_ contient des \_ informations pour la \_ commande MCI Set pour les périphériques audio Waveform.
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- Structure de MCI_WAVE_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844226"
---
# <a name="mci_wave_set_parms-structure"></a>Définition de la \_ \_ structure des PARMS MCI Wave \_

La structure de l' **\_ ensemble des sons MCI Wave \_ \_** contient des informations pour la commande [**MCI \_ Set**](mci-set.md) pour les périphériques audio Waveform.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Format d’heure de l’appareil.

</dd> <dt>

**dwAudio**
</dt> <dd>

Numéro de canal pour la sortie audio. Généralement utilisé lors de l’activation ou de la désactivation d’un canal.

</dd> <dt>

**wInput**
</dt> <dd>

Canal d’entrée audio.

</dd> <dt>

**wOutput**
</dt> <dd>

Périphérique de sortie à utiliser. Par exemple, cette valeur peut être 2 si deux cartes son ont été installées sur un système.

</dd> <dt>

**wFormatTag**
</dt> <dd>

Format des données Waveform-Audio, telles que le \_ format Wave \_ PCM. Les valeurs possibles sont définies dans mmreg. h.

</dd> <dt>

**wReserved2**
</dt> <dd>

Réservé.

</dd> <dt>

**nChannels**
</dt> <dd>

Mono (1) ou stéréo (2).

</dd> <dt>

**wReserved3**
</dt> <dd>

Réservé.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Échantillons par seconde.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Taux d’échantillonnage en octets par seconde.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

L’alignement des données est bloqué.

</dd> <dt>

**wReserved4**
</dt> <dd>

Réservé.

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits par échantillon.

</dd> <dt>

**wReserved5**
</dt> <dd>

Réservé.

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

[**jeu de MCI \_**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

