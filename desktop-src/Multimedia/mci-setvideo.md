---
title: Commande MCI_SETVIDEO (mmsystem. h)
description: La \_ commande MCI SETVIDEO définit les valeurs associées à la lecture vidéo. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Commande MCI_SETVIDEO Windows multimédia
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465418"
---
# <a name="mci_setvideo-command"></a>\_Commande MCI SETVIDEO

La \_ commande MCI SETVIDEO définit les valeurs associées à la lecture vidéo. Les appareils vidéo numériques et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
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

**MCI \_ NOTIFY**, **l' \_ attente MCI** ou **le \_ test MCI**. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Pointeur vers une structure de [**\_ \_ PARMS générique MCI**](mci-generic-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « Digitalvideo » :

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ DGV \_ SETVIDEO \_ ALG
</dt> <dd>

Le membre **lpstrAlgorithm** de la structure identifiée par *lpSetVideo* contient l’adresse d’une mémoire tampon contenant le nom d’un algorithme de compression vidéo. L’algorithme de compression est utilisé par les commandes de [ \_ réserve MCI](mci-reserve.md) ou d' [ \_ enregistrement MCI](mci-record.md) suivantes. Les algorithmes disponibles dépendent du périphérique.

Si l’algorithme spécifié est incompatible avec le format de fichier actuel, le format de fichier est remplacé par le format par défaut de l’algorithme.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ DGV \_ SETVIDEO \_ CLOCKTIME
</dt> <dd>

Lorsqu’il est utilisé avec **MCI \_ DGV \_ SETVIDEO \_ sur**, indique que l’heure est spécifiée en millisecondes et est l’heure absolue. (Cette heure n’est pas à l’étape de la diffusion de l’espace de travail.)

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_entrée MCI DGV \_ SETVIDEO \_
</dt> <dd>

Modifie la **\_ \_ \_ teinte** **MCI \_ DGV \_ SETVIDEO \_ Brightness**, **MCI \_ DGV \_ SETVIDEO \_ Color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ net** ou MCI DGV SETVIDEO, afin qu’elle affecte le signal d’entrée et modifie ce qui est enregistré. Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_ \_ élément SETVIDEO DGV \_ MCI
</dt> <dd>

Une constante vidéo est spécifiée dans le membre **dwItem** de la structure identifiée par *lpSetVideo*. La constante identifie la valeur qui est définie. Vous pouvez spécifier les constantes suivantes avec cet indicateur :

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_procédure de dessin MCI AVI \_ SETVIDEO \_ \_
</dt> <dd>

Une nouvelle adresse de procédure de dessin est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. Vous pouvez spécifier une nouvelle procédure de dessin uniquement lorsque l’appareil est inactif. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI. Il n’existe aucun équivalent à cet indicateur dans l’interface de commande de chaîne.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_couleur de \_ la \_ palette SETVIDEO AVI \_ MCI
</dt> <dd>

Une nouvelle couleur de palette est spécifiée dans les membres **dwOver** et **dwValue** de la structure identifiée par *lpSetVideo*. Le membre **dwOver** spécifie l’index de palette de la couleur à modifier et le membre **dwValue** spécifie la nouvelle couleur, sous la forme d’une valeur RVB. Vous devez également spécifier les indicateurs de **\_ \_ \_ valeur** **MCI \_ DGV \_ SETVIDEO \_ sur** et MCI DGV avec **l' \_ \_ \_ élément MCI DGV SETVIDEO** lorsque vous utilisez cette constante. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_demi- \_ \_ \_ teinte de la palette SETVIDEO AVI MCI
</dt> <dd>

Indique que la palette de demi-teintes doit être utilisée au lieu de la palette par défaut. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ DGV \_ SETVIDEO \_ BITSPERPEL
</dt> <dd>

Le nombre de bits par pixel est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. Le nombre de bits par pixel est utilisé pour enregistrer les données capturées ou enregistrées

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_luminosité de \_ SETVIDEO \_ DGV MCI
</dt> <dd>

Le niveau de luminosité de la vidéo est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_couleur MCI DGV \_ SETVIDEO \_
</dt> <dd>

Le niveau de saturation de la couleur vidéo est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_ \_ contraste SETVIDEO DGV \_ MCI
</dt> <dd>

Le niveau de contraste vidéo est spécifié en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_fréquence d’images MCI DGV \_ SETVIDEO \_ \_
</dt> <dd>

Une fréquence d’images est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. Le taux est spécifié en unités d’images par seconde (1000). Par exemple, 29,97 images par seconde sont spécifiées sous la forme 29970.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_DGV MCI \_ SETVIDEO \_ gamma
</dt> <dd>

Une valeur d’exposant de correction gamma est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. La correction gamma ajuste le mappage entre l’intensité encodée dans la source de présentation et la luminosité affichée. La valeur est l’exposant multiplié par 1000. Par exemple, 2200 indique un exposant de 2,2. Une valeur de 1000 indique un exposant de 1, qui n’applique aucune correction gamma.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_couleur de \_ \_ clé SETVIDEO DGV MCI \_
</dt> <dd>

Une couleur de clé est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. La couleur de la clé est une valeur RVB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_index de \_ \_ clé SETVIDEO DGV MCI \_
</dt> <dd>

Une valeur d’index de clé est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. Le paramètre d’index est un index de palette physique.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ DGV \_ SETVIDEO \_ PALHANDLE
</dt> <dd>

Un descripteur de palette est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. Le descripteur de palette est contenu dans le mot de poids faible. Les périphériques vidéo numériques ne doivent pas libérer la palette transmise avec cette commande. Les applications doivent le libérer après avoir fermé l’appareil. Cet indicateur est pris en charge uniquement par les appareils qui utilisent des palettes. Si le handle de palette spécifié est égal à zéro, la palette par défaut est utilisée.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_ \_ netteté MCI DGV SETVIDEO \_
</dt> <dd>

Une valeur de netteté vidéo est spécifiée en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_source MCI DGV \_ SETVIDEO \_
</dt> <dd>

Une constante qui spécifie la source de l’entrée vidéo est spécifiée dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. Les constantes suivantes sont définies :

-   **MCI \_ DGV \_ SETVIDEO \_ src \_ NTSC**: télévision NTSC.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ PAL : PAL Television.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ RGB : vidéo RVB.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ SECAM : SECAM Television.
-   MCI \_ DGV \_ SETVIDEO \_ src \_ SVIDEO : S-Video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_flux MCI DGV \_ SETVIDEO \_
</dt> <dd>

Un flux vidéo est spécifié dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. La valeur entière spécifie le flux vidéo lu de l’espace de travail. Si le flux n’est pas spécifié et que le format de fichier ne définit pas de flux par défaut, le premier flux vidéo entrelacé physiquement est lu.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_ \_ teinte MCI DGV SETVIDEO \_
</dt> <dd>

Une valeur de teinte vidéo est spécifiée en tant que facteur dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. En règle générale, cet ajustement est modélisé après le contrôle de la teinte de nombreux jeux de télévision couleur, avec 250 défini en vert, 750 défini en rouge et 0 (ou 1000) défini en bleu. La valeur nominale est toujours 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_sortie MCI DGV \_ SETVIDEO \_
</dt> <dd>

La **couleur \_ MCI \_ DGV SETVIDEO \_ Brightness**, **MCI \_ DGV \_ SETVIDEO \_ Color**, **MCI \_ DGV \_ SETVIDEO \_ Contrast**, **MCI \_ DGV \_ SETVIDEO \_ gamma**, **MCI \_ DGV \_ SETVIDEO \_ net** ou **MCI \_ DGV \_ SETVIDEO \_** est modifiée de sorte qu’elle affecte uniquement le signal affiché et non ce qui est enregistré. Si possible, il s’agit de la valeur par défaut lors de l’analyse d’un fichier.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ DGV \_ SETVIDEO \_
</dt> <dd>

Un paramètre de longueur de transition est inclus dans le membre **dwOver** de la structure identifiée par *lpSetVideo*. La longueur de transition spécifie la durée (dans le format d’heure actuel) à appliquer pour apporter une modification. Si cet indicateur n’est pas utilisé, la modification se produit immédiatement.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_DGV MCI \_ SETVIDEO \_
</dt> <dd>

Le membre **lpstrQuality** de la structure identifiée par *lpSetVideo* contient l’adresse d’une mémoire tampon décrivant la qualité de la vidéo. Une chaîne de texte dans la mémoire tampon spécifie les caractéristiques de l’algorithme de compression vidéo.

L’indicateur **MCI \_ DGV \_ SETVIDEO \_ ALG** peut être utilisé pour sélectionner un descripteur de qualité pour l’algorithme spécifié. Si cet indicateur est omis, l’algorithme actuel est utilisé.

Les algorithmes et les noms de descripteurs disponibles dépendent du périphérique. Chaque appareil fournit de la documentation pour les algorithmes disponibles et une description des noms de descripteur applicables. La commande [MCI \_ Quality](mci-quality.md) peut définir des noms de descripteurs supplémentaires. Tous les appareils prennent en charge les descripteurs « Low », « medium » et « High ». La valeur par défaut est spécifique au pilote.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_enregistrement MCI DGV \_ SETVIDEO \_
</dt> <dd>

Spécifie si l’enregistrement inclut ou exclut les données vidéo. Lorsqu’elles sont combinées avec **MCI \_ \_** activé, les données vidéo sont enregistrées. Lorsqu’elle est associée à l' **\_ \_ option MCI désactivée**, les données vidéo sont exclues. La valeur par défaut comprend les données vidéo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ numéro SRC du SETVIDEO DGV \_ MCI \_
</dt> <dd>

Un nombre pour la source vidéo est spécifié dans le membre **dwSourceNumber** de la structure identifiée par *lpSetVideo*. S’il existe plusieurs entrées du type spécifié par la **\_ \_ \_ valeur SETVIDEO de MCI DGV**, la valeur sélectionne l’entrée. Cet indicateur doit toujours être utilisé avec **la \_ \_ \_ source MCI DGV SETVIDEO**. Toutefois, si la **\_ \_ \_ valeur de SETVIDEO DGV MCI** est omise, le numéro de source spécifié indique la source absolue à utiliser comme indiqué dans la commande de [ \_ liste MCI](mci-list.md) .

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ DGV \_ SETVIDEO \_ toujours
</dt> <dd>

Le nom de l’algorithme ou la valeur de qualité spécifiée s’applique aux images fixes.

Chaque pilote de périphérique doit prendre en charge l’algorithme « None », ce qui signifie qu’aucune compression n’est nécessaire. Il s’agit de la valeur par défaut. Dans ce cas, les périphériques vidéo numériques enregistrent des images fixes sous forme de bitmaps indépendantes des appareils RVB (DIB).

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ valeur SETVIDEO de DGV MCI \_
</dt> <dd>

Une valeur est incluse dans le membre **dwValue** de la structure identifiée par *lpSetVideo*. La signification de la valeur est spécifiée par l’indicateur **MCI \_ DGV \_ SETVIDEO \_ Item** .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ \_ désactivé
</dt> <dd>

Désactive la sortie vidéo. Pour les périphériques vidéo numériques, la désactivation de la vidéo définit les pixels du rectangle de destination défini par la commande [ \_ put de MCI](mci-put.md) (ou la région cliente de la fenêtre active) sur une couleur unie, mais elle n’a aucun effet sur la mémoire tampon de trame. Si vous le souhaitez, vous pouvez masquer la fenêtre avec la commande de [ \_ fenêtre MCI](mci-window.md) . La source de vidéo, qu’il s’agisse de l’espace de travail ou d’une entrée externe, peut continuer à stocker de nouvelles images dans la mémoire tampon de trame, mais elles ne sont pas affichées tant que la vidéo n’est pas activée. Alors que les applications doivent utiliser la \_ commande MCI SETVIDEO pour contrôler cette fonction, les appareils vidéo numériques doivent toujours prendre en charge cet indicateur. La valeur par défaut après une ouverture est activée.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ activé \_
</dt> <dd>

Active la sortie vidéo.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpSetVideo* pointe vers une structure [**MCI \_ DGV \_ SETVIDEO \_ PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil « VCR » :

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_ \_ enregistrement SETVIDEO magnétoscope \_ MCI
</dt> <dd>

Définit l’enregistrement vidéo sur on ou OFF. Utilisé conjointement avec l’un des indicateurs suivants :

-   **MCI \_ DÉFINI \_ sur**. Enregistrement vidéo activé.
-   **MCI \_ \_désactivée**. Enregistrement vidéo désactivé. Il peut être nécessaire de désactiver d’abord l’enregistrement de l’assembly (à l’aide de la commande [ \_ Set MCI](mci-set.md) avec l’indicateur de l' **\_ \_ \_ \_ enregistrement assembler** de l’ensemble magnétoscope MCI défini sur OFF) avant que l’enregistrement vidéo puisse être désactivé.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>\_piste MCI
</dt> <dd>

Le membre **dwTrack** de la structure identifiée par *lpSetVideo* spécifie la piste qui est affectée par la commande.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_ \_ source SETVIDEO magnétoscope \_ MCI
</dt> <dd>

Définit la source vidéo et doit être utilisé avec le **magnétoscope MCI \_ \_ SETVIDEO \_ pour** signaler.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_ \_ moniteur SETVIDEO magnétoscope \_ MCI
</dt> <dd>

Définit le moniteur de source vidéo et doit être utilisé avec le \_ magnétoscope MCI \_ SETVIDEO \_ pour signaler.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_magnétoscope MCI \_ SETVIDEO \_ à
</dt> <dd>

Le membre **dwTo** de la structure identifiée par *lpSetVideo* contient l’une des constantes suivantes :

<dl> <dd>**\_tuner de \_ \_ type SRC magnétoscope MCI \_**</dd> <dd>**\_ligne de \_ \_ type SRC magnétoscope MCI \_**</dd> <dd>**\_magnétoscope MCI \_ type de source \_ \_ aux**</dd> <dd>**\_type de source de magnétoscope MCI \_ \_ \_ générique**</dd> <dd>**\_type de source de magnétoscope MCI \_ \_ \_ muet**</dd> <dd>**\_sortie de \_ \_ type SRC magnétoscope MCI \_**</dd> <dd>**\_type de source de magnétoscope MCI \_ \_ \_ RGB**</dd> <dd>**\_ \_ numéro SETVIDEO magnétoscope \_ MCI**</dd> </dl>

Le membre **dwNumber** de la structure identifiée par *lpSetVideo* contient l’entrée vidéo (du type spécifié dans le membre **dwTo** ) à utiliser.

</dd> </dl>

Pour les périphériques VCR, le paramètre *lpSetVideo* pointe vers une structure [**MCI \_ VCR \_ SETVIDEO \_ PARMS**](mci-vcr-setvideo-parms.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Commandes MCI](mci-commands.md)
</dt> </dl>

 

