---
title: Structure de MCI_VCR_SET_PARMS (VCR. h)
description: La structure de l' \_ ensemble de paramètres MCI magnétoscope \_ contient des \_ paramètres pour la \_ commande MCI Set pour les enregistreurs vidéo-cassettes.
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- structure MCI_VCR_SET_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe32f93500ae4c294bad372868e9f7818c672824611bcbc29c3315eb75a9742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802984"
---
# <a name="mci_vcr_set_parms-structure"></a>La \_ structure de l’ensemble de magnétoscopes MCI \_ \_

La structure de l’ensemble de paramètres **MCI \_ magnétoscope \_ \_** contient des paramètres pour la commande [**MCI \_ Set**](mci-set.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Format de l’heure actuelle.

</dd> <dt>

**dwAudio**
</dt> <dd>

Non utilisé.

</dd> <dt>

**dwTimeMode**
</dt> <dd>

Constante qui spécifie la source de minutage utilisée par l’appareil. La source de minutage est soit un code temporel enregistré sur bande vidéo, soit les compteurs de l’appareil qui détectent le mouvement des cassettes vidéo.

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

Taux d’enregistrement.

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

Format d’une nouvelle valeur de temps de compteur.

</dd> <dt>

**dwIndex**
</dt> <dd>

Contenu de l’affichage à l’écran.

</dd> <dt>

**dwTracking**
</dt> <dd>

Réglage de la vitesse utilisé pour le suivi de la vitesse de lecture des MAGNÉTOSCOPEs.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Vitesse de lecture utilisée par l’appareil en tant qu’entier. La vitesse de lecture normale est de 1000, la double vitesse est de 2000, et la demi-vitesse est de 500.

</dd> <dt>

**dwLength**
</dt> <dd>

Longueur de bande vidéo lorsque la longueur n’est pas détectable par l’appareil.

</dd> <dt>

**dwCounter**
</dt> <dd>

Nouvelle valeur de compteur.

</dd> <dt>

**dwClock**
</dt> <dd>

Nouvelle heure de l’horloge.

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Nouvelle valeur de délai d’attente pour la commande pause.

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

Longueur de bande vidéo nécessaire pour stabiliser la sortie du magnétoscope.

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

La longueur des cassettes vidéo est nécessaire pour freiner le transport du magnétoscope lors de l’émission d’une commande [**MCI \_ Stop**](mci-stop.md) ou [**MCI \_ Pause**](mci-pause.md) .

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

[**\_Pause MCI**](mci-pause.md)
</dt> <dt>

[**jeu de MCI \_**](mci-set.md)
</dt> <dt>

[**\_arrêt MCI**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

