---
title: Commande MCI_LIST (mmsystem. h)
description: La \_ commande MCI List obtient des informations sur le nombre et les types d’entrées disponibles pour l’appareil. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- commande MCI_LIST Windows multimédia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363847"
---
# <a name="mci_list-command"></a>\_Commande de liste MCI

La \_ commande MCI List obtient des informations sur le nombre et les types d’entrées disponibles pour l’appareil. Les appareils vidéo numériques et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificateur de l’appareil MCI qui doit recevoir le message de commande.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI \_ Notify, MCI \_ Wait ou MCI \_ test. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Les indicateurs supplémentaires suivants s’appliquent au type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ List \_ ALG
</dt> <dd>

Le membre **lpstrAlgorithm** de la structure identifiée par *lpList* contient l’adresse d’une mémoire tampon contenant le nom d’un algorithme. Le nom est utilisé pour récupérer les types de descripteurs de qualité associés à un algorithme.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_nombre de \_ listes MCI DGV \_
</dt> <dd>

Retourne le nombre d’options du type spécifié.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_élément de \_ liste \_ DGV MCI
</dt> <dd>

Une constante indiquant que le type de liste est inclus dans le membre **dwItem** de la structure identifiée par *lpList*. Cet indicateur est obligatoire. Utilisez l’une des constantes suivantes pour indiquer le type de liste :

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ liste de l' \_ \_ ALG audio
</dt> <dd>

La commande doit récupérer les noms des algorithmes audio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_ \_ \_ qualité audio de la liste DGV MCI \_
</dt> <dd>

La commande doit récupérer des niveaux de qualité audio. Les niveaux renvoyés sont associés à l’algorithme référencé par le membre **lpstrAlgorithm** de la structure identifiée par *lpList*. Si ce membre est spécifié à l’aide de la chaîne « Current », les qualités associées à l’algorithme actuel sont retournées.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_ \_ flux audio de liste DGV \_ MCI \_
</dt> <dd>

La commande doit récupérer les noms des flux audio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_liste de DGV MCI \_ \_ toujours \_ al
</dt> <dd>

La commande doit récupérer les noms des algorithmes toujours.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>qualité de la \_ liste de DGV MCI \_ \_ \_
</dt> <dd>

La commande doit récupérer des niveaux de qualité. Les niveaux renvoyés sont associés à l’algorithme référencé par le membre **lpstrAlgorithm** de la structure identifiée par *lpList*. Si ce membre est spécifié à l’aide de la chaîne « Current », les qualités associées à l’algorithme actuel sont retournées.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_vidéo de \_ liste MCI DGV \_ \_ ALG
</dt> <dd>

La commande doit récupérer les noms des algorithmes vidéo.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_ \_ \_ qualité vidéo de la liste DGV MCI \_
</dt> <dd>

La commande doit récupérer des niveaux de qualité vidéo. Les niveaux renvoyés sont associés à l’algorithme référencé par le membre **lpstrAlgorithm** de la structure identifiée par *lpList*. Si ce membre est spécifié à l’aide de la chaîne « Current », les qualités associées à l’algorithme actuel sont retournées.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_ \_ \_ source vidéo de la liste DGV MCI \_
</dt> <dd>

La commande doit retourner des informations sur les sources vidéo. En cas d’utilisation \_ avec \_ \_ le nombre de listes MCI DGV, la commande retourne le nombre de sources vidéo. Lorsqu’elle est utilisée \_ avec \_ \_ le numéro de liste MCI DGV, la commande retourne le type d’une source vidéo. MCI définit les types suivants :

-   \_ \_ \_ Generic SETVIDEO SRC \_ DGV MCI
-   MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC
-   \_PAL DGV \_ SETVIDEO \_ src \_
-   MCI \_ DGV \_ SETVIDEO \_ src \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ src \_ Svideo

Plusieurs sources de chaque type peuvent être retournées. Le type de source générique est utilisé lorsque plus un type de signal est autorisé pour ce connecteur.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_ \_ flux vidéo de liste DGV \_ MCI \_
</dt> <dd>

La commande doit récupérer les noms des flux vidéo.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_numéro de \_ liste \_ DGV MCI
</dt> <dd>

Un index est spécifié dans le membre **dwNumber** de la structure identifiée par *lpList*. L’index doit être un entier compris entre 1 et la valeur retournée pour \_ l' \_ indicateur de nombre de listes MCI DGV \_ .

</dd> </dl>

Pour les périphériques vidéo numériques, *lpList* pointe vers une structure [**MCI \_ DGV \_ List \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .

Les indicateurs supplémentaires suivants s’appliquent au type de périphérique **VCR** :

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_ \_ source audio de liste de MAGNÉTOSCOPEs MCI \_ \_
</dt> <dd>

Répertorier les entrées ou les types audio.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_nombre de listes de magnétoscopes MCI \_ \_
</dt> <dd>

Définit le membre **dwReturn** de la structure identifiée par *lpList* sur le nombre total d’entrées vidéo ou audio.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>Numéro de la \_ liste magnétoscope MCI \_ \_
</dt> <dd>

Définit le membre **dwReturn** de la structure identifiée par *lpList* sur le type de l’entrée vidéo ou audio spécifiée par le membre **dwNumber** .

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_ \_ source vidéo de liste de MAGNÉTOSCOPEs MCI \_ \_
</dt> <dd>

Répertorier les entrées ou les types vidéo.

</dd> </dl>

Pour les périphériques VCR, *lpList* pointe vers une structure de [**\_ \_ liste \_ de magnétoscopes MCI**](mci-vcr-list-parms.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 

