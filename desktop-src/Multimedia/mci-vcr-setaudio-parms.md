---
title: Structure de MCI_VCR_SETAUDIO_PARMS (VCR. h)
description: La \_ \_ structure SETAUDIO PARMS du magnétoscope MCI contient des \_ paramètres pour la \_ commande MCI SETAUDIO pour les enregistreurs vidéo-cassettes.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- structure MCI_VCR_SETAUDIO_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195032"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>MCI \_ VCR \_ SETAUDIO \_ PARMS

La **structure \_ \_ SETAUDIO \_ PARMS du magnétoscope MCI** contient des paramètres pour la commande [**MCI \_ SETAUDIO**](mci-setaudio.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwTrack**
</dt> <dd>

Piste audio.

</dd> <dt>

**dwTo**
</dt> <dd>

Type d’entrée ou d’entrée analysée.

</dd> <dt>

**dwNumber**
</dt> <dd>

Entrée audio (du type spécifié dans le membre **dwTo** ) à utiliser.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Structures MCI**](mci-structures.md)
</dt> <dt>

[**\_SETAUDIO MCI**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

