---
title: commande Open (Corecrt \_ IO. h)
description: La commande Open Initialise un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- ouvrir une commande Windows multimédia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363696"
---
# <a name="open-command"></a>ouvrir une commande

La commande Open Initialise un appareil. Tous les périphériques MCI reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*
</dt> <dd>

Identificateur d’un périphérique MCI ou d’un pilote de périphérique. Il peut s’agir d’un nom d’appareil (comme indiqué dans le registre ou le fichier SYSTEM.INI) ou du nom de fichier du pilote de périphérique. Si vous spécifiez le nom de fichier du pilote de périphérique, vous pouvez éventuellement inclure le. DRV, mais vous ne devez pas inclure le chemin d’accès au fichier.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Indicateur qui identifie l’élément à initialiser. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **Open** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                        | Signification                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias d' *appareil \_ alias* partageable                                  | type *de \_ périphérique* de type                                                             |
| digitalvideo | alias de l' *appareil \_ aliaselementname* nostatic parent *HWND* partageable | style de style d’un style enfant chevauchement style de style Popup type *de type \_* *périphérique \_* |
| superposition      | alias de l' *appareil \_* alias parent du style partageable *HWND*         | style de style Popup style avec chevauchement style type *de type \_* *périphérique \_*             |
| sequencer    | alias d' *appareil \_ alias* partageable                                 | type *de \_ périphérique* de type                                                             |
| vidéo          | alias d' *appareil \_ alias* partageable                                  | type *de \_ périphérique* de type                                                             |
| videodisk    | alias d' *appareil \_ alias* partageable                                  | type *de \_ périphérique* de type                                                             |
| WaveAudio    | alias de la *\_ taille* de la mémoire tampon des *\_ alias d’appareil*                     | *\_ type de périphérique* partageable                                                    |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszOpenFlags** et leurs significations.



| Valeur                 | Signification                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alias de l' *appareil \_* alias | Spécifie un autre nom pour l’appareil donné. S’il est spécifié, il doit être utilisé *comme \_ ID d’appareil* dans les commandes suivantes.                                                                                                                                                                                                                                          |
| *ElementName*         | Spécifie le nom de l’élément d’appareil (fichier) chargé lorsque l’appareil s’ouvre.                                                                                                                                                                                                                                                                                        |
| *\_ taille* de la mémoire tampon de mémoire tampon | Définit la taille, en secondes, de la mémoire tampon utilisée par le périphérique Wave-audio. La taille par défaut de la mémoire tampon est définie lorsque le périphérique Wave-audio est installé ou configuré. En règle générale, la taille de la mémoire tampon est définie à 4 secondes. Avec l’appareil MCIWAVE, la taille minimale est de 2 secondes et la taille maximale est de 9 secondes.                                                |
| *HWND* parent         | Spécifie le handle de fenêtre de la fenêtre parente.                                                                                                                                                                                                                                                                                                                    |
| partageable              | Initialise l’appareil ou le fichier comme partageable. Les tentatives suivantes d’ouverture du périphérique ou du fichier échouent, sauf si vous spécifiez « partageable » dans les commandes d’origine et les commandes **ouvertes** suivantes. MCI retourne une erreur d’appareil non valide si l’appareil est déjà ouvert et ne peut pas être partagé.<br/> Les appareils MCISEQ Sequencer et MCIWAVE ne prennent pas en charge les fichiers partagés.<br/> |
| enfant de style           | Ouvre une fenêtre avec un style de fenêtre enfant.                                                                                                                                                                                                                                                                                                                            |
| chevauchement de style      | Ouvre une fenêtre avec un style de fenêtre avec chevauchement.                                                                                                                                                                                                                                                                                                                      |
| menu contextuel style           | Ouvre une fenêtre avec un style de fenêtre contextuelle.                                                                                                                                                                                                                                                                                                                           |
| *\_ type de style* de style   | Indique un style de fenêtre.                                                                                                                                                                                                                                                                                                                                            |
| type *de \_ périphérique* de type   | Spécifie le type d’appareil d’un fichier.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

MCI réserve « cdaudio » pour le type de périphérique CD audio, « videodisc » pour le type d’appareil videodisc, « Sequencer » pour le type d’appareil MIDI Sequencer, « AVIVideo » pour le type de périphérique vidéo numérique et « WaveAudio » pour le type de périphérique Waveform-Audio.

En guise d’alternative à l’indicateur « type », MCI peut sélectionner l’appareil en fonction de l’extension utilisée par le fichier, tel qu’il est enregistré dans le registre ou dans la \[ \] section d’extension MCI du fichier SYSTEM.INI.

MCI peut ouvrir des fichiers AVI à l’aide d’un pointeur d’interface de fichier ou d’un pointeur d’interface de flux. Pour ouvrir un fichier à l’aide de l’un des deux types de pointeur d’interface, spécifiez un arobase (@) suivi du pointeur d’interface à la place du nom du fichier ou du périphérique pour le paramètre *lpszDevice* . Pour plus d’informations sur les interfaces de fichier et de flux, consultez « [fonctions et macros avifile](avifile-functions-and-macros.md)».

La commande suivante ouvre l’appareil « mySound ».

``` syntax
open new type waveaudio alias mysound buffer 6
```

Avec le nom de périphérique « nouveau », le pilote de forme d’onde prépare une nouvelle ressource de forme d’onde. La commande attribue l’alias d’appareil « mySound » et spécifie une mémoire tampon de 6 secondes.

Vous pouvez éliminer l’indicateur « type » si vous combinez le nom de l’appareil avec le nom de fichier. MCI reconnaît cette combinaison lorsque vous utilisez la syntaxe suivante :

*\_ nom* de l’appareil ! *nom de l’élément \_*

Le point d’exclamation sépare le nom du périphérique du nom de fichier. Le point d’exclamation ne doit pas être délimité par des espaces blancs.

L’exemple suivant ouvre le droit. Fichier WAV utilisant l’appareil « WaveAudio ».

``` syntax
open waveaudio!right.wav
```

Le pilote MCIWAVE requiert un périphérique audio Wave asynchrone.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Corecrt \_ IO. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> </dl>

 

