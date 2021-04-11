---
title: commande capture
description: La commande capture copie le contenu de la mémoire tampon de frame et le stocke dans le fichier spécifié. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- commande de capture multimédia Windows
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105919"
---
# <a name="capture-command"></a>commande capture

La commande capture copie le contenu de la mémoire tampon de frame et le stocke dans le fichier spécifié. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

Un ou plusieurs des indicateurs suivants :



| Valeur          | Signification                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| comme *chemin d’accès*  | Spécifie le chemin d’accès et le nom de fichier de destination de l’image capturée. Cet indicateur est obligatoire.                                                                                                                                                                |
| au niveau du *rectangle* | Spécifie la zone rectangulaire dans la mémoire tampon de trame que l’appareil rogne et enregistre sur le disque. En cas d’omission, la zone rognée est définie par défaut sur le rectangle spécifié ou par défaut sur une commande [put](put.md) « source » précédente pour cette instance d’appareil. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Cette commande peut échouer si l’appareil est en train de visionner des vidéos animées ou d’exécuter d’autres opérations gourmandes en ressources. Si la mémoire tampon de trame est mise à jour en temps réel, la mise à jour s’interrompt momentanément afin qu’une image complète soit capturée. Si l’appareil interrompt la mise à jour, il peut y avoir un effet visuel ou audible. Si le format de fichier, l’algorithme de compression et les niveaux de qualité n’ont pas été définis, leurs valeurs par défaut sont utilisées.

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

[posé](put.md)
</dt> </dl>

 

