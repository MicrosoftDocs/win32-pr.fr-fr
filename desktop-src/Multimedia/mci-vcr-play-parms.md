---
title: Structure de MCI_VCR_PLAY_PARMS (VCR. h)
description: La \_ structure des paramètres MCI VCR \_ Play contient des \_ paramètres pour la \_ commande MCI Play pour les enregistreurs vidéo-cassettes.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- structure MCI_VCR_PLAY_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363800"
---
# <a name="mci_vcr_play_parms-structure"></a>La \_ \_ structure des PARMS de lecture MCI VCR \_

La structure des paramètres **MCI \_ VCR \_ Play \_** contient des paramètres pour la commande [**MCI \_ Play**](mci-play.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position à partir de laquelle effectuer la lecture.

</dd> <dt>

**dwTo**
</dt> <dd>

Position de lecture.

</dd> <dt>

**dwAt**
</dt> <dd>

Valeur de temps qui affecte la commande [**MCI \_ Play**](mci-play.md) ou [**MCI \_ CUE**](mci-cue.md) . Pour la lecture [**MCI \_**](mci-play-parms.md), il s’agit de l’heure de début de la lecture. Pour **le \_ signal MCI**, il s’agit de l’heure à laquelle l’appareil de passage atteint la position donnée dans **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les positions sont spécifiées dans le format d’heure actuel.

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

[**\_signal MCI**](mci-cue.md)
</dt> <dt>

[**\_lecture MCI**](mci-play.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

