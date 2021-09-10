---
title: Structure de MCI_VCR_STATUS_PARMS (VCR. h)
description: La \_ structure d’état des magnétoscopes MCI contient des \_ \_ paramètres pour la \_ commande d’État MCI pour les enregistreurs vidéo-cassettes.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- structure MCI_VCR_STATUS_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363899"
---
# <a name="mci_vcr_status_parms-structure"></a>Structure de l' \_ État des magnétoscopes MCI \_ \_

La structure d' **\_ \_ état \_ des magnétoscopes MCI** contient des paramètres pour la commande d' [**\_ État MCI**](mci-status.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Valeur renvoyée par la commande d' [**\_ État MCI**](mci-status.md) . La valeur de retour varie en fonction de la recherche de la commande. Pour plus d’informations, consultez la description de la commande d' [**\_ État MCI**](mci-status-parms.md) .

</dd> <dt>

**dwItem**
</dt> <dd>

Type d’informations demandées.

</dd> <dt>

**dwTrack**
</dt> <dd>

Piste audio ou vidéo qui stocke les informations lors de l’enregistrement suivant. Ce membre est utilisé pour retourner des informations lorsque la commande d' [**\_ État MCI**](mci-status-parms.md) se renseigne sur l’état de l’enregistrement vidéo ou audio.

</dd> <dt>

**dwNumber**
</dt> <dd>

Tuner logique auquel le canal actuel est associé. Ce membre est utilisé pour retourner des informations lorsque la commande d' [**\_ État MCI**](mci-status.md) se renseigne sur le numéro de canal actuel.

</dd> </dl>

## <a name="remarks"></a>Remarques

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

[**\_État MCI**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

