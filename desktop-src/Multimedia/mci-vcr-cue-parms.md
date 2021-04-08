---
title: Structure de MCI_VCR_CUE_PARMS (VCR. h)
description: La \_ structure de paramètres MCI VCR \_ CUE contient des \_ paramètres pour la \_ commande MCI CUE pour les enregistreurs vidéo-cassette.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- Structure de MCI_VCR_CUE_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844229"
---
# <a name="mci_vcr_cue_parms-structure"></a>La \_ \_ structure des \_ PARMS du magnétoscope MCI

La structure de paramètres **MCI \_ VCR \_ CUE \_** contient des paramètres pour la commande [**MCI \_ CUE**](mci-cue.md) pour les enregistreurs vidéo-cassette.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position de départ.

</dd> <dt>

**dwTo**
</dt> <dd>

Position à laquelle signaler.

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Configuration requise



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

[**\_signal MCI**](mci-cue.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

