---
title: commande setvideo
description: La commande setvideo définit les valeurs associées à la lecture et à la capture vidéo. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: a6851b9b-e09a-4251-bd1c-19b1e4b6f871
keywords:
- commande setvideo multimédia Windows
topic_type:
- apiref
api_name:
- setvideo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa4c3d1e3b90b9ab0c5bf5791dacd541c8a8bc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384840"
---
# <a name="setvideo-command"></a>commande setvideo

La commande setvideo définit les valeurs associées à la lecture et à la capture vidéo. Les appareils vidéo numériques et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("setvideo %s %s %s"), 
  lpszDeviceID, 
  lpszVideo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszVideo"></span><span id="lpszvideo"></span><span id="LPSZVIDEO"></span>*lpszVideo*
</dt> <dd>

Indicateur de lecture et de capture vidéo. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **setvideo** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                                                                                                                                                        | Signification                                                                                                                                                                                                                                                                                                |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | *algorithme* d’algorithme BitsPerPel pour *compter* la luminosité sur *Factor clocktimecolor à factoriser* *contraste pour factoriser* la gamma à la *valeur* halftoneinputkey couleur à *r :g:* *index de clé* b vers l' *index* offonoutput | *couleur* de couleur de la palette sur la *durée* par rapport à l' *index* sur le handle de la palette *newrgb* pour *gérer* la fréquence d’images des enregistrements du *descripteur* de qualité *jusqu'* au *taux* *d’enregistrement* du onrecord offsharpness de *facteur* source en *valeur* de numéro *source* |
| vidéo          | offonmonitor pour *taper* le *numéro nombre numéro* de *suivi de \_ la* piste offrecord                                                                                                               | enregistrer le numéro *de \_ piste de piste onrecord onsource dans* le *type* *numéro de* *suivi numéro de suivi offtrack numéro \_* de piste sur *\_*                                                                                                                                                                             |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszVideo** et leurs significations.



| Valeur                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algorithme* d’algorithme                          | Spécifie un algorithme de compression vidéo à utiliser par une commande [Reserve](reserve.md) ou [Record](record.md) ultérieure. Les algorithmes pris en charge par un appareil sont spécifiques à l’appareil. MCI définit les constantes « MPEG » et « H261 » pour l' *algorithme*. Si l’algorithme spécifié est en conflit avec le format de fichier actuel, le format de fichier est remplacé par le format par défaut de l’algorithme.<br/>                                                                                                                                     |
| BitsPerPel à *compter*                          | Définit le nombre de bits par pixel pour l’enregistrement des données avec la commande de [capture](capture.md) ou d' [enregistrement](record.md) .                                                                                                                                                                                                                                                                                                                                                                                                              |
| luminosité à *factoriser*                         | Définit le niveau de luminosité de la vidéo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| clocktime                                      | Indique que l’heure spécifiée dans l’indicateur « sur » est exprimée en millisecondes. L’heure est absolue et n’est pas à l’étape de la diffusion de l’espace de travail.                                                                                                                                                                                                                                                                                                                                                                                |
| couleur à *factoriser*                              | Définit le niveau de saturation de la couleur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| contraste vers le *facteur*                           | Définit le niveau de contraste de la vidéo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *valeur* gamma à                               | Spécifie l’exposant de correction gamma multiplié par 1000. Par exemple, pour spécifier un exposant de 2,2, utilisez 2200 comme *valeur*. Une valeur gamma de 1,0 (1000) indique qu’aucune correction gamma n’est appliquée. La correction gamma ajuste le mappage entre l’intensité encodée dans la source de présentation et la luminosité affichée.                                                                                                                                                                                                 |
| -                                       | Provoque l’utilisation de la palette de demi-teintes à la place de la palette par défaut. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.                                                                                                                                                                                                                                                                                                                                                                                         |
| entrée                                          | Modifie les indicateurs « luminosité », « couleur », « contraste », « gamma », « nette » ou « teinte » afin qu’il affecte le signal d’entrée et modifie ce qui est enregistré. Si possible, il s’agit de la valeur par défaut lors de l’analyse de l’entrée.                                                                                                                                                                                                                                                                                                             |
| couleur de la clé pour *r :g: b*                           | Définit la couleur de la clé. La variable *r :g: b* est une valeur RVB. Deux-points ( :) Séparez les valeurs individuelles de rouge, de vert et de bleu.                                                                                                                                                                                                                                                                                                                                                                                                       |
| index de clé à *indexer*                           | Définit l’index de clé. La variable d' *index* est un index de palette physique.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| analyser pour *taper* le *numéro numéro*              | Contrôle l’entrée source qui sera transmise à la sortie du magnétoscope, sans modifier la sélection d’entrée de la source d’enregistrement. Le type peut être « Output » ou l’une des sources d’entrée valides. Si « Number » n’est pas spécifié, la première entrée de ce type est choisie.                                                                                                                                                                                                                                                                        |
| offon                                          | Active ou désactive l’affichage de la vidéo. La désactivation de la vidéo définit les [pixels du rectangle de « destination](put.md) » (ou par défaut, la zone cliente de la fenêtre active) sur une couleur unie. Elle n’a aucun effet sur la mémoire tampon de trame. La source vidéo, qu’il s’agisse d’un espace de travail ou d’une entrée externe, peut continuer à stocker de nouvelles images dans la mémoire tampon de trame. Ils ne s’affichent pas tant que la vidéo n’est pas activée. Vous pouvez utiliser la commande « état » de la [fenêtre](window.md) pour masquer la fenêtre. La valeur par défaut est **setvideo** "on".<br/> |
| sortie                                         | Modifie les indicateurs « Brightness », « Color », « Contrast », « gamma », « Sharp » ou « tint » afin qu’il modifie uniquement le signal affiché et non ce qui est enregistré. Si possible, il s’agit de la valeur par défaut lors de l’analyse d’un fichier.                                                                                                                                                                                                                                                                                                           |
| au-delà de la *durée*                                | Spécifie la durée nécessaire pour effectuer une modification qui utilise une variable *facteur* . Les unités de *durée* sont au format d’heure actuel. Les modifications se produisent à l’étape avec la diffusion de l’espace de travail. Lorsque la lecture est suspendue, la modification est également suspendue jusqu’à ce que la lecture se poursuive. Si « sur » n’est pas utilisé ou n’est pas pris en charge, la modification se produit immédiatement.                                                                                                                                                                    |
| *couleur* de couleur de la palette sur l' *index* à *newrgb* | Définit une nouvelle couleur de la palette. L’index de couleur et de palette à modifier est spécifié par les paramètres de *couleur* et d' *index* ; la nouvelle couleur est spécifiée par *newrgb*. Cet indicateur est reconnu uniquement par le pilote vidéo de MCIAVI.                                                                                                                                                                                                                                                                                               |
| handle de palette à *gérer*                     | Spécifie le descripteur d’une palette que l’appareil doit utiliser pour le rendu. Cet élément est pris en charge uniquement par les appareils qui utilisent des palettes. Si *handle* est égal à zéro, la palette par défaut est utilisée. Les périphériques vidéo numériques ne doivent pas libérer la palette transmise avec cette commande. Les applications doivent le libérer après avoir fermé l’appareil.<br/>                                                                                                                                                                                                 |
| *descripteur* de qualité                           | Spécifie les caractéristiques de la compression vidéo effectuée lorsque la vidéo est enregistrée dans un fichier. Tous les appareils prennent en charge les trois descripteurs : « Low », « medium » et « High ». La valeur par défaut est spécifique à l’appareil. L’importance de ces noms dépend de l’algorithme et de l’appareil. Les appareils peuvent définir des noms de descripteurs supplémentaires. La commande [Quality](quality.md) peut être utilisée pour définir des noms de descripteurs supplémentaires. Si l’indicateur « algorithme » n’est pas utilisé, le *descripteur* s’applique à l’algorithme actuel.<br/>   |
| taux de trames d’enregistrement à *tarif*                    | Définit l’enregistrement pour la vidéo animée. Le *taux* d’enregistrement est spécifié en unités d’images par seconde multiplié par 1000. Par exemple, la fréquence d’images NTSC de 29,97 images par seconde est représentée sous la forme 29970.                                                                                                                                                                                                                                                                                                                   |
| enregistrement onrecord désactivé                            | Active ou désactive l’enregistrement des données vidéo. L’enregistrement des données vidéo est la valeur par défaut.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| enregistrer le *\_ numéro de piste* de piste désactivé               | Efface la sélection de la source vidéo afin qu’aucune vidéo ne soit enregistrée avec la commande d' [enregistrement](record.md) suivante. « Track » permet une sélection de suivi indépendante. Si « Track » n’est pas spécifié, la valeur par défaut 1 est utilisée. Il peut être nécessaire de commencer par émettre une commande [Set](set.md) « assembler l’enregistrement off » pour que l’enregistrement vidéo puisse être désactivé.                                                                                                                                                                     |
| enregistrer le *\_ numéro de piste* du suivi sur                | Sélectionne la source vidéo à enregistrer avec la commande **enregistrement** suivante. « Track » permet une sélection de suivi indépendante. Track 2 correspond à la piste PCM dans Hi8. Si « Track » n’est pas spécifié, une valeur par défaut de 1 est utilisée.                                                                                                                                                                                                                                                                                                      |
| netteté pour *factoriser*                          | Définit le niveau de netteté de la vidéo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *valeur* du numéro de source à *source*              | Définit la source de l’entrée vidéo. Cela correspond généralement aux connecteurs externes. Les constantes définies pour la *source* sont « RGB », « PAL », « NTSC », « Svideo » et « SECAM ». S’il existe plusieurs entrées du type spécifié, la *valeur* facultative « number » indique l’entrée souhaitée. Par exemple, **setvideo** "source to NTSC number 2" spécifie la deuxième entrée NTSC. Si la *source* « to » est omise, la source absolue est utilisée comme défini par la commande « Video source » de la [liste](list.md) .<br/>            |
| Numéro de la source  au *type* numéro               | Sélectionne la source vidéo à enregistrer sur la bande. Le *type* doit être « tuner », « line », « Svideo », « aux », « Generic », « MUTE » ou « RGB ».                                                                                                                                                                                                                                                                                                                                                                                              |
| *algorithme* de l’algorithme continue                    | Spécifie l’algorithme de compression d’image continue utilisé par la commande de [capture](capture.md) . Chaque appareil doit prendre en charge l' *algorithme* « None », ce qui signifie qu’aucune compression n’est nécessaire. Il s’agit de la valeur par défaut. Dans ce cas, les périphériques vidéo numériques enregistrent des images fixes en tant que bitmaps indépendantes des appareils RVB. Les appareils peuvent également prendre en charge une liste d’algorithmes supplémentaires spécifiques à l’appareil.                                                                                                                                                           |
| *descripteur* de qualité toujours                     | Spécifie les caractéristiques de la compression d’image continue effectuée lors de la capture d’une image continue. Tous les appareils prennent en charge les descripteurs « Low », « medium » et « High ». La valeur par défaut est spécifique à l’appareil. Si l’indicateur « algorithme » n’est pas utilisé, le *descripteur* s’applique à l’algorithme actuel.<br/> La commande [Quality](quality.md) peut être utilisée pour définir d’autres noms de descripteurs.<br/>                                                                                                                            |
| diffuser en *nombre*                             | Spécifie le flux vidéo lu à partir de l’espace de travail. Si le flux n’est pas spécifié et qu’un flux par défaut n’est pas défini par le format de fichier, le flux vidéo d’abord entrelacé physique est joué.                                                                                                                                                                                                                                                                                                                 |
| teinte à *factoriser*                               | Définit la teinte de l’image. En règle générale, cet ajustement est modélisé après le contrôle de la teinte de nombreux jeux de télévision couleur, avec 250 signifiant vert, 750 signifie rouge et 0 (ou                                                                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Pour les périphériques VCR, l’utilisation de setvideo avec un indicateur qui désactive une piste individuelle (« suivre le *\_ numéro de suivi* ») peut entraîner la réception par votre application d’un message d’état indiquant que la commande n’a pas pu être exécutée. Certains magnétoscopes peuvent désactiver uniquement les combinaisons de pistes, pas les pistes individuelles. par exemple, la première piste audio et une piste vidéo d’une cassette vidéo. Dans ce cas, utilisez simplement [SetAudio](setaudio.md) et setvideo pour continuer à désactiver les autres pistes qui composent la combinaison. Le pilote désactive les pistes lorsqu’il reçoit la commande pour désactiver la dernière piste dans la combinaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[attire](capture.md)
</dt> <dt>

[list](list.md)
</dt> <dt>

[posé](put.md)
</dt> <dt>

[enregistrement](record.md)
</dt> <dt>

[reserve](reserve.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[fenetre](window.md)
</dt> </dl>

 

