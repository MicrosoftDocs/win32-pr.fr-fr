---
title: Commande MCI_STATUS (mmsystem. h)
description: La \_ commande d’État MCI récupère des informations sur un périphérique MCI. Tous les appareils reconnaissent cette commande. Les informations sont retournées dans le membre dwReturn de la structure identifiée par le paramètre lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Commande MCI_STATUS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2021
ms.locfileid: "104321253"
---
# <a name="mci_status-command"></a>\_Commande d’État MCI

> [!NOTE]
> Communication sans biais Microsoft prend en charge un environnement diversifié et un environnement d’inclusion.  Dans ce document, il existe des références au mot « esclave ». Le [Guide de style de Microsoft pour les Communications Bias-Free](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconnaît cela comme un mot d’exclusion.  Ce libellé est utilisé, car il s’agit actuellement de la formulation utilisée dans les commandes. Pour des fins de cohérence, ce document contient ce mot. Lorsque ce mot est modifié dans les commandes, nous allons corriger ce document pour qu’il soit aligné.

La \_ commande d’État MCI récupère des informations sur un périphérique MCI. Tous les appareils reconnaissent cette commande. Les informations sont retournées dans le membre **dwReturn** de la structure identifiée par le paramètre *lpStatus* .

Pour envoyer cette commande, appelez la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) avec les paramètres suivants.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
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

MCI \_ Notify, MCI \_ Wait ou, pour les appareils vidéo numériques et VCR, test MCI \_ . Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ État MCI**](mci-status-parms.md) . (Les appareils avec des jeux de commandes étendus peuvent remplacer cette structure par une structure spécifique à l’appareil.)

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Les indicateurs standard et spécifiques à la commande suivants s’appliquent à tous les appareils prenant en charge l' \_ État MCI :

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_élément d’État MCI \_
</dt> <dd>

Spécifie que le membre **dwItem** de la structure identifiée par *lpStatus* contient une constante qui spécifie l’élément d’État à obtenir. Les constantes suivantes définissent l’élément d’État à retourner dans le membre **dwReturn** de la structure :

\_ \_ piste active de l’État MCI \_

Le membre **dwReturn** est défini sur le numéro de suivi actuel. MCI utilise des numéros de pistes continus.

longueur de l' \_ État MCI \_

Le membre **dwReturn** est défini sur la longueur totale du média.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_mode d’État MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur le mode actuel de l’appareil. Les modes sont les suivants :

-   \_mode MCI \_ non \_ prêt
-   \_pause en mode MCI \_
-   \_lecture en mode MCI \_
-   \_arrêt en mode MCI \_
-   \_mode MCI \_ ouvert
-   \_enregistrement en mode MCI \_
-   \_recherche en mode MCI \_

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_ \_ nombre d’États MCI \_ des \_ pistes
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre total de pistes lisibles.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>POSITION de l' \_ État MCI \_
</dt> <dd>

Le membre **dwReturn** est défini à la position actuelle.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>\_État MCI \_ prêt
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’appareil est prêt ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>FORMAT de l’heure de l' \_ État MCI \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le format d’heure actuel de l’appareil. Les formats d’heure sont les suivants :

-   \_octets au format MCI \_
-   \_images au format MCI \_
-   \_format MCI \_ HMS
-   FORMAT MCI en \_ \_ millisecondes
-   FORMAT MCI ( \_ \_ MSF)
-   \_exemples de format MCI \_
-   \_format MCI \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>démarrage de l' \_ État MCI \_
</dt> <dd>

Obtient la position de départ du média. Pour atteindre la position de départ, associez cet indicateur à l' \_ élément d’État MCI \_ et définissez le membre **dwItem** de la structure identifiée par *lpStatus* sur la position d' \_ État MCI \_ .

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>\_piste MCI
</dt> <dd>

Indique qu’un paramètre de suivi d’État est inclus dans le membre **dwTrack** de la structure identifiée par *lpStatus*. Vous devez utiliser cet indicateur avec les \_ \_ constantes position d’État MCI ou \_ longueur d’État MCI \_ . Lorsqu’elle est utilisée avec la \_ position d’État MCI \_ , \_ la piste MCI obtient la position de départ de la piste spécifiée. Lorsqu’elle est utilisée avec la \_ \_ durée d’État MCI, \_ la piste MCI obtient la longueur de la piste spécifiée. MCI utilise des numéros de pistes continus.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **cdaudio** . Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_piste de \_ type d’État MCI CDA \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’une des valeurs suivantes :

-   MCI \_ CDA \_ piste \_ audio
-   MCI \_ CDA- \_ piste \_ autre

Pour utiliser cet indicateur, l' \_ indicateur de piste MCI doit être défini et le membre **dwTrack** de la structure identifié par *lpStatus* doit contenir un numéro de suivi valide.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Digitalvideo** :

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>\_DGV d' \_ état \_ MCI
</dt> <dd>

Le membre **lpstrDrive** de la structure identifiée par *lpStatus* spécifie un lecteur de disque ou, dans certaines implémentations, un chemin d’accès. La \_ commande d’État MCI retourne la quantité approximative d’espace disque qui peut être obtenue par la commande de [ \_ réserve MCI](mci-reserve.md) dans le membre **dwReturn** de la structure identifiée par *lpStatus*. L’espace disque est mesuré en unités du format d’heure actuel.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_ \_ entrée d’État MCI DGV \_
</dt> <dd>

La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique à l’entrée.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>État de DGV MCI à \_ \_ \_ gauche
</dt> <dd>

La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique au canal audio de gauche.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>\_ \_ état \_ nominal de MCI DGV
</dt> <dd>

La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* demande la valeur nominale plutôt que la valeur actuelle.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>sortie de l' \_ État MCI DGV \_ \_
</dt> <dd>

La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique à la sortie.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_enregistrement d' \_ État MCI DGV \_
</dt> <dd>

La fréquence d’images renvoyée pour l' \_ indicateur de fréquence d’images d’État MCI DGV \_ \_ \_ est le taux utilisé pour la compression.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>informations de référence sur l' \_ État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** de la structure identifiée par *lpStatus* retourne l’image de l’image clé la plus proche qui précède le frame spécifié dans le membre **dwReference** .

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>État de DGV MCI- \_ \_ \_ droit
</dt> <dd>

La constante spécifiée par le membre **dwItem** de la structure identifiée par *lpStatus* s’applique au canal audio approprié.

</dd> </dl>

Les constantes suivantes sont utilisées avec le type d’appareil **Digitalvideo** dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ sauts audio d’État AVI \_ MCI
</dt> <dd>

Le membre **dwReturn** retourne le nombre de fois que la partie audio de la dernière séquence AVI est tombée. Le système compte un saut audio chaque fois qu’il tente d’écrire des données audio sur le pilote de périphérique et découvre que le pilote a déjà lu toutes les données disponibles. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>\_images d' \_ État AVI MCI \_ \_ ignorées
</dt> <dd>

Le membre **dwReturn** retourne le nombre d’images qui n’ont pas été dessinées lorsque la dernière séquence AVI a été lue. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_vitesse de \_ \_ lecture du dernier État AVI \_ MCI \_
</dt> <dd>

Le membre **dwReturn** retourne une valeur représentant le degré de précision de la durée de l’exécution réelle de la dernière séquence AVI correspondant à la durée d’exécution de la cible. La valeur 1000 indique que l’heure cible et l’heure réelle étaient les mêmes. Une valeur de 2000, par exemple, indique que la séquence AVI prenait deux fois plus de temps que nécessaire. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>\_ \_ État audio MCI \_ DGV
</dt> <dd>

Le membre **dwReturn** retourne la valeur MCI \_ on ou MCI \_ off selon l’option MCI Set audio la plus récente \_ \_ pour la commande [ \_ Set MCI](mci-set.md) . Elle retourne MCI \_ sur si l’un ou l’autre ou les deux enceintes sont activées, et l' \_ option MCI désactivée dans le cas contraire.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_ \_ \_ entrée audio d’État MCI DGV \_
</dt> <dd>

Le membre **dwReturn** retourne le niveau audio instantané approximatif du signal audio analogique. Une valeur supérieure à 1000 signifie qu’il y a une distorsion de découpage. Certains appareils peuvent déterminer cette valeur uniquement lors de l’enregistrement audio. Cette valeur d’État n’a pas de commande **MCI \_ Set** ou [MCI \_ SETAUDIO](mci-setaudio.md) associée. Cette valeur est associée à, mais normalisée différemment de, le niveau d’état de l’onde MCI Wave de commande Waveform Audio \_ \_ \_ .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_ \_ enregistrement audio d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la \_ valeur MCI on ou MCI en \_ reflétant l’état défini par l' \_ \_ indicateur d’enregistrement MCI DGV SETAUDIO \_ de la commande **MCI \_ SETAUDIO** .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_ \_ source audio d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la source de digitaliseur audio actuelle :

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_moyenne de \_ SETAUDIO \_ DGV MCI
</dt> <dd>

Spécifie la moyenne des canaux audio de gauche et de droite.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ SETAUDIO \_ gauche
</dt> <dd>

Spécifie le canal audio de gauche.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>MCI \_ DGV \_ SETAUDIO \_ Right
</dt> <dd>

Spécifie le canal audio approprié.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>MCI \_ DGV \_ SETAUDIO \_ stéréo
</dt> <dd>

Spécifie le stéréo.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_ \_ flux audio d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le numéro de flux audio actuel.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>\_État DGV \_ MCI \_ AVGBYTESPERSEC
</dt> <dd>

Le membre **dwReturn** retourne le nombre moyen d’octets par seconde utilisés pour l’enregistrement.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>\_État DGV MCI- \_ \_ basses
</dt> <dd>

Le membre **dwReturn** retourne le niveau de basses audio actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>\_État DGV \_ MCI \_ BITSPERPEL
</dt> <dd>

Le membre **dwReturn** retourne le nombre de bits par pixel utilisé pour enregistrer les données capturées ou enregistrées.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>\_État DGV \_ MCI \_ BitsPerSample
</dt> <dd>

Le membre **dwReturn** retourne le nombre de bits par échantillon que l’appareil utilise pour l’enregistrement. Cela s’applique uniquement aux appareils prenant en charge le format PCM.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>\_État DGV \_ MCI \_ BLOCKALIGN
</dt> <dd>

Le membre **dwReturn** retourne l’alignement des blocs de données par rapport au début de la forme d’onde d’entrée.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>luminosité de l' \_ État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le niveau de luminosité vidéo actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>\_couleur d' \_ État MCI DGV \_
</dt> <dd>

Le membre **dwReturn** retourne le niveau de couleur actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>contraste de l' \_ État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le niveau de contraste actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_État d’DGV MCI \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le format de fichier actuel pour l’enregistrement ou l’enregistrement.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_mode de \_ fichier d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne l’état de l’opération de fichier :

\_modification du \_ mode de fichier DGV \_ MCI \_

Renvoyé pendant les opérations couper, copier, supprimer, coller et annuler.

\_mode de \_ fichier DGV MCI \_ \_ inactif

Renvoyé lorsque le fichier est prêt pour l’opération suivante.

\_ \_ \_ chargement en mode de fichier DGV MCI \_

Retourné lors du chargement du fichier.

\_ \_ \_ enregistrement en mode de fichier DGV MCI \_

Retourné lors de l’enregistrement du fichier.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_exécution du \_ fichier d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le pourcentage estimé pendant lequel l’opération de chargement, d’enregistrement, de capture, de couper, de copier, de suppression, de collage ou d’annulation a progressé. (Les applications peuvent l’utiliser pour fournir un indicateur visuel de la progression.) Cet indicateur n’est pas pris en charge par tous les périphériques vidéo numériques.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_État de DGV MCI \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la **valeur true** si la direction de l’appareil est vers l’avant ou si l’appareil n’est pas en train de fonctionner.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_fréquence d' \_ images d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** doit être utilisé avec l' \_ État DGV de l' \_ état \_ nominal, MCI \_ DGV \_ \_ , ou les deux. Lorsqu' \_ il est utilisé avec \_ l’enregistrement d’État MCI DGV \_ , la fréquence d’images actuelle utilisée pour l’enregistrement est retournée. En cas d’utilisation avec les \_ enregistrements d’État MCI DGV et les \_ \_ \_ États MCI DGV \_ \_ , la fréquence d’images nominale associée au signal vidéo d’entrée est retournée. Lorsqu' \_ il est utilisé avec \_ l’État nominal de l’DGV MCI \_ , la fréquence d’images nominale associée au fichier est retournée. Dans tous les cas, les unités sont en images par seconde multiplié par 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>\_ \_ État gamma des DGV MCI \_
</dt> <dd>

Le membre **dwReturn** retourne la valeur gamma actuelle. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>\_État DGV \_ MCI \_ HPAL
</dt> <dd>

Le membre **dwReturn** retourne la valeur décimale ASCII pour le handle de palette actuel. Le descripteur est contenu dans le mot de poids faible de la valeur retournée.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_HWND DGV \_ état \_ HWND
</dt> <dd>

Le membre **dwReturn** retourne la valeur décimale ASCII pour le handle de fenêtre explicite ou par défaut actuellement associé à cette instance de pilote de périphérique. Le descripteur est contenu dans le mot de poids faible de la valeur retournée.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>couleur de la clé d’État MCI \_ DGV \_ \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la valeur de la couleur de la clé actuelle.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>INDEX de la clé d’État MCI \_ DGV \_ \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la valeur actuelle de l’index de clé.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_moniteur d' \_ État MCI DGV \_
</dt> <dd>

Le membre **dwReturn** retourne une constante indiquant la source de la présentation actuelle. Les constantes suivantes sont définies :

\_fichier d' \_ analyse \_ DGV MCI

Un fichier est la source.

\_entrée du \_ moniteur MCI DGV \_

L’entrée est la source.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_méthode du \_ moniteur d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne une constante indiquant la méthode utilisée pour la surveillance d’entrée. Les constantes suivantes sont définies :

\_ \_ mode direct MCI \_ DGV

Surveillance directe des entrées.

publication de la \_ méthode DGV MCI \_ \_

Surveillance après entrée.

\_pré- \_ méthode \_ DGV MCI

Surveillance de pré-entrée.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_ \_ \_ mode pause de l’État MCI DGV \_
</dt> <dd>

Le membre **dwReturn** retourne le \_ mode \_ lecture MCI si l’appareil a été interrompu lors de la lecture et retourne l' \_ enregistrement en mode MCI \_ si l’appareil a été mis en pause pendant l’enregistrement. La commande retourne la \_ \_ fonction non applicable MCIERR comme une erreur de retour si l’appareil n’est pas suspendu.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>\_État DGV \_ MCI \_ SAMPLESPERSECOND
</dt> <dd>

Le membre **dwReturn** retourne le nombre d’échantillons par seconde enregistrés.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>\_État de DGV MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** retourne **true** ou **false** indiquant si le format Seek exact est défini. (Les applications peuvent définir ce format à l’aide de la commande [MCI \_ Set](mci-set.md) avec l' \_ indicateur MCI DGV \_ Set \_ Seek \_ exact.)

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_netteté de l’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le niveau de netteté actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>taille de l' \_ État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la durée de lecture approximative des données compressées que l’espace de travail réservé contiendra. Les unités de durée sont au format d’heure actuel. Elle retourne zéro s’il n’y a pas d’espace disque réservé. La taille retournée est approximative, car l’espace disque précis pour les données compressées ne peut pas, en général, être prédit tant que les données n’ont pas été compressées.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>\_État DGV \_ MCI \_
</dt> <dd>

Le membre **dwReturn** retourne le code de temps SMPTE associé à la position actuelle dans l’espace de travail.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>Vitesse d’état de MCI \_ DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne la vitesse de lecture actuelle.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>\_État de DGV MCI \_ \_ toujours \_ en cours
</dt> <dd>

Le membre **dwReturn** retourne le format de fichier actuel pour la commande de [ \_ capture MCI](mci-capture.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_teinte de l’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le niveau de teinte vidéo actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>\_État des \_ \_ aigus MCI DGV
</dt> <dd>

Le membre **dwReturn** retourne le niveau de aigu audio actuel. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_État de DGV MCI \_ \_ non enregistré
</dt> <dd>

Le **membre dwReturn** retourne la **valeur true** s’il y a des données enregistrées dans l’espace de travail qui peuvent être perdues suite à une [ \_ fermeture MCI](mci-close.md), une [ \_ charge MCI](mci-load.md), un [ \_ enregistrement MCI](mci-record.md), une [ \_ réservation MCI](mci-reserve.md), une [ \_ coupure](mci-cut.md)MCI, une [ \_ suppression MCI](mci-delete.md)ou une commande de [ \_ Collage MCI](mci-paste.md) . Dans le cas contraire, le membre retourne la **valeur false** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>\_vidéo d' \_ État MCI DGV \_
</dt> <dd>

Le membre **dwReturn** retourne MCI \_ si la vidéo est activée ou MCI \_ si elle est désactivée.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_ \_ enregistrement vidéo d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne \_ la valeur MCI on ou MCI, en \_ reflétant l’état défini par l' \_ \_ indicateur d’enregistrement MCI DGV SETVIDEO \_ de la commande [MCI \_ SETVIDEO](mci-setvideo.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_ \_ source vidéo d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne une constante indiquant le type de source vidéo défini par l' \_ indicateur de source MCI DGV \_ SETVIDEO \_ de la commande **MCI \_ SETVIDEO** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_vidéo d’État MCI DGV \_ \_ \_ src \_ num
</dt> <dd>

Le membre **dwReturn** retourne le nombre dans son type de source d’entrée vidéo actuellement actif.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_ \_ flux vidéo d’État MCI DGV \_ \_
</dt> <dd>

Le membre **dwReturn** retourne le numéro de flux vidéo actuel.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>\_volume d' \_ État MCI DGV \_
</dt> <dd>

Le membre **dwReturn** retourne la moyenne du volume aux haut-parleurs gauche et droit. Utilisez \_ \_ \_ l’état de l’DGV MCI avec cet indicateur pour obtenir le niveau nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>\_fenêtre d' \_ État MCI DGV \_ \_ visible
</dt> <dd>

Le membre **dwReturn** retourne la **valeur true** si la fenêtre n’est pas masquée.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>\_fenêtre d' \_ État MCI DGV \_ \_ réduite
</dt> <dd>

Le membre **dwReturn** retourne la **valeur true** si la fenêtre est réduite.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>\_fenêtre d’État MCI DGV \_ \_ \_ agrandie
</dt> <dd>

Le membre **dwReturn** retourne la **valeur true** si la fenêtre est agrandie.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent
</dt> <dd>

Le membre **dwReturn** retourne la **valeur true**.

</dd> </dl>

Pour les périphériques vidéo numériques, le paramètre *lpStatus* pointe vers une structure de paramètres d' [**\_ \_ état \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **Sequencer** . Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>\_ \_ DIVTYPE état de l’MCI Seq \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’une des valeurs suivantes indiquant le type de division actuel d’une séquence :

-   MCI \_ Seq \_ div \_ PPQN
-   MCI \_ Seq \_ div \_ SMPTE \_ 24
-   MCI \_ Seq \_ div \_ SMPTE \_ 25
-   MCI \_ Seq \_ div \_ SMPTE \_ 30
-   MCI \_ Seq \_ div \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_contrôleur d' \_ État MCI Seq \_
</dt> <dd>

Le membre **dwReturn** est défini sur le type de synchronisation utilisé pour l’opération maître.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>décalage de l' \_ État MCI Seq \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le décalage SMPTE actuel d’une séquence.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>\_port d' \_ État MCI Seq \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’identificateur d’appareil MIDI pour le port actuel utilisé par la séquence.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_État esclave de l’État MCI Seq \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le type de synchronisation utilisé pour l’opération subordonnée.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>TEMPO d’État du MCI \_ Seq \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le tempo actuel d’une séquence MIDI en temps par minute pour les fichiers PPQN, ou les images par seconde pour les fichiers SMPTE.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique **VCR** . Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_enregistrement d' \_ État de magnétoscope \_ MCI \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le mode assembler est activé ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_ \_ moniteur audio d’état de magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante, indiquant le type de moniteur audio actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_numéro du \_ \_ moniteur audio \_ \_ de l’état du magnétoscope MCI
</dt> <dd>

Le membre **dwReturn** est défini sur le numéro du type de moniteur audio actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_ \_ enregistrement audio d’État magnétoscope \_ MCI \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’audio est enregistré lorsque la commande d’enregistrement suivante est donnée ; elle a la valeur **false** dans le cas contraire. Si vous spécifiez MCI \_ Track dans le paramètre *dwFlags* de cette commande, **dwTrack** contient le suivi auquel s’applique cette requête.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_ \_ source audio d’État MCI VCR \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante, indiquant le type de source audio en cours.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_numéro de \_ \_ source audio \_ \_ de l’état du magnétoscope MCI
</dt> <dd>

Le membre **dwReturn** est défini sur le numéro du type de source audio actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>horloge de l' \_ État MCI VCR \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la valeur d’horloge actuelle, dans le nombre total d’incréments d’horloge.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>ID d’horloge de l' \_ État de magnétoscope MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur un nombre qui décrit de façon unique l’horloge en cours d’utilisation.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>FORMAT du compteur de l' \_ État du magnétoscope MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante décrivant le format de compteur actuel. Pour plus d’informations, consultez l' \_ \_ \_ indicateur de format d’heure Set MCI de la commande [ \_ Set MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_résolution de \_ compteur d’état de magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante décrivant la résolution du compteur et est l’une des valeurs suivantes :

-   \_ \_ \_ Images de compteur de magnétoscope MCI : le \_ compteur a une résolution de frames.
-   \_Compteur de magnétoscopes MCI \_ \_ res \_ secondes : le compteur a une résolution de secondes.
-   \_Valeur du \_ compteur d’État du magnétoscope MCI \_ \_ : le membre **dwReturn** est défini sur le compteur en cours de lecture, dans le format au moment du compteur actuel.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_fréquence des \_ \_ trames d’état de magnétoscope MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur la fréquence d’images Native actuelle de l’appareil.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_index d' \_ état \_ magnétoscope MCI
</dt> <dd>

Le membre **dwReturn** est défini sur une constante, décrivant le contenu actuel de l’affichage à l’écran et est l’un des éléments suivants :

-   \_compteur d' \_ index \_ magnétoscope MCI
-   \_Date d' \_ index \_ magnétoscope MCI
-   \_heure d' \_ index \_ magnétoscope MCI
-   \_code temporel de l’index magnétoscope MCI \_ \_

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ \_ index d’état de magnétoscope MCI \_ activé
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’affichage à l’écran est activé ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_type de \_ média d’État magnétoscope \_ MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’un des éléments suivants :

-   \_Média magnétoscope \_ MCI \_ 8 mm
-   \_Hi8 de \_ média \_ magnétoscope MCI
-   MCI \_ magnétoscope \_ - \_ VHS
-   \_SVHS de \_ média \_ magnétoscope MCI
-   MCI \_ VCR \_ Media \_ bêta
-   \_EDBETA de \_ média \_ magnétoscope MCI
-   \_média magnétoscope \_ MCI \_ autre

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_numéro d' \_ État du magnétoscope MCI \_
</dt> <dd>

Le membre **dwNumber** est défini sur le numéro de tuner logique lorsque vous utilisez cet indicateur avec l' \_ indicateur de \_ canal tuner d’état de magnétoscope MCI \_ \_ .

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ État du magnétoscope \_ MCI \_ nombre \_ de \_ pistes audio
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre de pistes audio qui peuvent être sélectionnées de manière indépendante.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ État du magnétoscope \_ MCI \_ nombre \_ de \_ pistes vidéo
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre de pistes vidéo qui peuvent être sélectionnées de manière indépendante.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>délai de pause de l' \_ État de magnétoscope MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la durée maximale, en millisecondes, d’une commande pause. La valeur de retour de zéro indique qu’aucun délai d’attente n’a lieu.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>FORMAT de lecture de l' \_ État MCI VCR \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’un des éléments suivants :

-   \_format VCR \_ MCI \_ EP
-   \_format de magnétoscope MCI \_ \_ LP
-   \_format VCR \_ MCI \_ autre
-   MCI \_ magnétoscope \_ au format \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_ \_ \_ durée Postroll de l’état de magnétoscope MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur la longueur de la bande vidéo qui est lue après l’emplacement où il a été arrêté, dans le format d’heure actuel. Cela est nécessaire pour freiner le transport de bandes VCR à partir d’une commande Stop ou pause.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ État de l' \_ alimentation MCI magnétoscope \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’alimentation est activée ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_durée du \_ préroll d’État du magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la longueur de la bande vidéo qui doit être lue avant l’emplacement où il a été démarré, dans le format d’heure actuel. Cela est nécessaire pour stabiliser la sortie du magnétoscope.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_format d' \_ enregistrement d’État magnétoscope \_ MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’un des éléments suivants :

-   \_format VCR \_ MCI \_ EP
-   \_format de magnétoscope MCI \_ \_ LP
-   \_format VCR \_ MCI \_ autre
-   MCI \_ magnétoscope \_ au format \_ SP

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_Vitesse d' \_ État du magnétoscope MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur la vitesse actuelle. Pour plus d’informations, consultez l' \_ \_ indicateur de vitesse du jeu de magnétoscopes MCI \_ de la commande [ \_ Set MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>MODE de temps de l' \_ État des magnétoscopes MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’un des éléments suivants :

-   \_compteur de \_ temps MCI VCR \_
-   détection de l' \_ heure du magnétoscope MCI \_ \_
-   \_code temporel de l’heure MCI magnétoscope \_ \_

Pour plus d’informations, consultez l' \_ indicateur MCI magnétoscope \_ Set \_ Time \_ mode de la commande [MCI \_ Set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>TYPE de temps de l' \_ État du magnétoscope MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante décrivant le type d’heure actuel en cours d’utilisation (utilisé par [Play](play.md), [Record](record.md), [Seek](seek.md), etc.), et est l’un des éléments suivants :

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_compteur de \_ temps MCI VCR \_
</dt> <dd>

Compteur en cours d’utilisation.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>\_code temporel de l’heure MCI magnétoscope \_ \_
</dt> <dd>

Le code temporel est en cours d’utilisation.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_ \_ code temporel MCI État du magnétoscope \_ \_ présent
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le code temporel est présent à la position actuelle dans le contenu ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_enregistrement du \_ \_ code temporel \_ MCI de l’État magnétoscope
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le code temporel sera enregistré lorsque la commande d’enregistrement suivante est donnée ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>TYPE de code de l' \_ État magnétoscope MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante, décrivant le type de code temporel qui est directement pris en charge par l’appareil, et est l’un des éléments suivants :

-   \_ \_ Type de code temporel de magnétoscope MCI \_ \_ aucun : cet appareil n’utilise pas de code temporel.
-   \_Type de \_ code temporel MCI magnétoscope \_ \_ autre : cet appareil utilise un code temporel non spécifié.
-   \_Type de \_ code temporel MCI magnétoscope \_ \_ SMPTE : cet appareil utilise le code temporel SMPTE.
-   \_ \_ Suppression SMPTE du type de code temporel de magnétoscope MCI \_ \_ \_ : cet appareil utilise le code temporel de suppression SMPTE.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_canal du \_ tuner d’État MCI VCR \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le numéro de canal actuel. Si vous spécifiez \_ le numéro d’État du magnétoscope MCI \_ \_ dans le paramètre *dwFlags* de cette commande, **dwNumber** contient le numéro de tuner logique auquel cette commande s’applique.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_ \_ moniteur vidéo d’État magnétoscope \_ MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante, indiquant le type de moniteur vidéo actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_numéro de \_ \_ moniteur vidéo \_ d’État magnétoscope MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur le numéro du type de moniteur vidéo actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_ \_ enregistrement vidéo d’État magnétoscope \_ MCI \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si la vidéo est enregistrée lorsque la commande d’enregistrement suivante est donnée ; elle a la valeur **false** dans le cas contraire. Si vous spécifiez MCI \_ Track dans le paramètre *dwFlags* de cette commande, **dwTrack** contient le suivi auquel s’applique cette requête.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_ \_ source vidéo d’état de magnétoscope MCI \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur une constante indiquant le type de source vidéo actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_numéro de \_ \_ source vidéo \_ \_ de l’État MCI VCR
</dt> <dd>

Le membre **dwReturn** est défini sur le numéro du type de source vidéo actuellement sélectionné.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_État du magnétoscope MCI \_ \_ protégé en écriture \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le média est protégé en écriture ; elle a la valeur **false** dans le cas contraire.

</dd> </dl>

Pour les périphériques VCR, le paramètre *lpStatus* pointe vers une structure d' [**\_ \_ état \_ de magnétoscope MCI**](mci-vcr-status-parms.md) .

L’utilisation \_ de l' \_ indicateur de longueur d’État MCI pour déterminer la longueur du média retourne toujours 2 heures pour les périphériques VCR, sauf si la longueur a été explicitement modifiée à l’aide de la commande [ \_ Set MCI](mci-set.md) .

Les indicateurs supplémentaires suivants sont utilisés avec le type de périphérique de **superposition** . Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_HWND OVLY \_ état \_ HWND
</dt> <dd>

Le membre **dwReturn** est défini sur le handle de la fenêtre associée à l’appareil de superposition vidéo.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_extension d' \_ État MCI OVLY \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si l’étirement est activé ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **videodisc** . Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_support d’État MCI \_ \_ présent
</dt> <dd>

Le membre **dwReturn** a la valeur **true** si le média est inséré dans l’appareil ; elle a la valeur **false** dans le cas contraire.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_mode d’État MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur le mode actuel de l’appareil. Les appareils Videodisc peuvent retourner la \_ \_ constante de parking en mode VD MCI \_ , en plus des constantes que tout appareil peut retourner, comme indiqué dans le paramètre *dwFlags* .

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_taille du \_ disque d’état \_ \_ MCI MCI
</dt> <dd>

Le membre **dwReturn** est défini sur la taille du disque chargé, en pouces (8 ou 12).

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>État du MCI MCI \_ \_ \_
</dt> <dd>

Le membre **dwReturn** a la valeur **true** en cas de progression ; elle a la valeur **false** dans le cas contraire.

L’appareil MCI videodisc ne prend pas en charge cet indicateur.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_type de \_ média d’État MCI VD \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur le type de média du média inséré. Les types de média suivants peuvent être retournés :

\_ \_ CAV multimédia VD \_ MCI

\_ \_ CLV multimédia VD \_ MCI

\_média MCI \_ VD \_ autre

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ côté État MCI \_ VD
</dt> <dd>

Le membre **dwReturn** a la valeur 1 ou 2 pour indiquer le côté du disque chargé. Tous les appareils videodisc ne prennent pas en charge cet indicateur.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>Vitesse de l' \_ État MCI VD \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur la vitesse de lecture en images par seconde. MCIPIONR. Le pilote de périphérique DRV retourne une \_ fonction non prise en charge MCIERR \_ .

</dd> </dl>

Les indicateurs supplémentaires suivants sont utilisés avec le type d’appareil **WaveAudio** . Ces constantes sont utilisées dans le membre **dwItem** de la structure vers laquelle pointe le paramètre *lpStatus* lorsque \_ \_ l’élément d’État MCI est spécifié pour le paramètre *dwFlags* .

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG Wave \_ MCI
</dt> <dd>

Le membre **dwReturn** est défini sur la balise de format actuelle utilisée pour la diffusion, l’enregistrement et l’enregistrement.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrée MCI Wave \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’appareil d’entrée Wave utilisé pour l’enregistrement. Si aucun appareil n’est en cours d’utilisation et qu’aucun appareil n’a été défini explicitement, l’erreur renvoyée est MCIERR \_ Wave \_ INPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_sortie MCI Wave \_
</dt> <dd>

Le membre **dwReturn** est défini sur le périphérique de sortie Wave utilisé pour la diffusion. Si aucun appareil n’est en cours d’utilisation et qu’aucun appareil n’a été défini explicitement, l’erreur renvoyée est MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>État de l' \_ onde MCI \_ \_ AVGBYTESPERSEC
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre d’octets par seconde actuels utilisé pour la diffusion, l’enregistrement et l’enregistrement.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>État de l' \_ onde MCI \_ \_ BitsPerSample
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre actuel de bits par échantillon utilisé pour la diffusion, l’enregistrement et l’enregistrement des données au format PCM.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>État de l' \_ onde MCI \_ \_ BLOCKALIGN
</dt> <dd>

Le membre **dwReturn** est défini sur l’alignement de bloc actuel utilisé pour la diffusion, l’enregistrement et l’enregistrement.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canaux d' \_ État des Wave MCI \_
</dt> <dd>

Le membre **dwReturn** est défini sur le nombre de canaux actuel utilisé pour la diffusion, l’enregistrement et l’enregistrement.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>niveau d’état de l' \_ onde MCI \_ \_
</dt> <dd>

Le membre **dwReturn** est défini sur l’enregistrement actuel ou sur le niveau de lecture des données au format PCM. La valeur est retournée sous la forme d’une valeur de 8 ou 16 bits, en fonction de la taille de l’échantillon utilisée. Le niveau de canal droit ou mono est retourné dans le mot de poids faible. Le niveau de canal gauche est retourné dans le mot de poids fort.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>État de l' \_ onde MCI \_ \_ SAMPLESPERSEC
</dt> <dd>

Le membre **dwReturn** est défini sur les échantillons actuels par seconde utilisés pour la diffusion, l’enregistrement et l’enregistrement.

</dd> </dl>

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
</dt> <dt>

[\_raccourcis MCI](mci-cut.md)
</dt> <dt>

[suppression de MCI \_](mci-delete.md)
</dt> <dt>

[\_Collage MCI](mci-paste.md)
</dt> <dt>

[\_réserve MCI](mci-reserve.md)
</dt> <dt>

[jeu de MCI \_](mci-set.md)
</dt> <dt>

[répétition](play.md)
</dt> <dt>

[enregistrement](record.md)
</dt> <dt>

[Demandez](seek.md)
</dt> </dl>

 

