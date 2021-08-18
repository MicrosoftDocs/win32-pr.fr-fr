---
title: Structure de MCI_VCR_CUE_PARMS (VCR. h)
description: La \_ structure de paramètres MCI VCR \_ CUE contient des \_ paramètres pour la \_ commande MCI CUE pour les enregistreurs vidéo-cassette.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- structure MCI_VCR_CUE_PARMS Windows multimédia
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
ms.openlocfilehash: 2ff14bf6db2fee24b2cee426114b460dc5e4682bd00e14f7b68a91695bab1f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038239"
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

## <a name="remarks"></a>Remarques

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

 

