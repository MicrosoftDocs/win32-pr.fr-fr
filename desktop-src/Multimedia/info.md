---
title: info (commande)
description: La commande info récupère une description du matériel à partir d’un appareil. Tous les périphériques MCI reconnaissent cette commande.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- commande info Windows multimédia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15675923f37a80ce694a400f18113f5178a54a3f75664008644919c6d9fc128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690469"
---
# <a name="info-command"></a>info (commande)

La commande info récupère une description du matériel à partir d’un appareil. Tous les périphériques MCI reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

Indicateur qui identifie le type d’informations requis. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande **info** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                             | Signification                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | info identityinfo UPC                                               | product                                             |
| digitalvideo | qualité audio algorithmaudio qualityfileproductstill algorithmstill | usageversionvideo algorithmvideo qualitywindow texte |
| superposition      | fileproduct                                                         | texte de la fenêtre                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| vidéo          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| WaveAudio    | fileinput                                                           | outputproduct                                       |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszInfoType** et leurs significations.



| Valeur           | Signification                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algorithme audio | Retourne le nom de l’algorithme de compression audio actuel.                                                                                                                                       |
| qualité audio   | Retourne le nom du descripteur de qualité audio actuel. Cela peut retourner « Unknown » si l’application a défini des paramètres sur des valeurs spécifiques qui ne correspondent pas aux qualités définies.       |
| copyright       | Récupère l’avis de copyright du fichier MIDI à partir de l’événement de métadonnées de copyright.                                                                                                                            |
| fichier            | Récupère le nom du fichier utilisé par l’appareil composé. Si l’appareil est ouvert sans fichier et que la commande [Load](load.md) n’a pas été utilisée, une chaîne NULL est retournée.                  |
| identité des informations   | Produit un identificateur unique pour le CD audio actuellement chargé dans le lecteur interrogé.                                                                                                        |
| info UPC        | Produit le code UPC (Universal Product Code) encodé sur un CD audio. Le UPC est une chaîne de chiffres. Elle n’est peut-être pas disponible pour tous les CD.                                                    |
| entrée           | Récupère la description de l’appareil d’entrée actuel. Retourne "none" si aucun périphérique d’entrée n’est défini.                                                                                               |
| name            | Récupère le nom de la séquence à partir de l’événement Meta nom de la séquence/suivi.                                                                                                                               |
| sortie          | Récupère la description du périphérique de sortie actuel. Retourne "none" si aucun périphérique de sortie n’est défini.                                                                                             |
| product         | Récupère une description de l’appareil. Ces informations incluent souvent le nom et le modèle du produit. La longueur de la chaîne ne doit pas dépasser 31 caractères.                                               |
| algorithme toujours | Retourne le nom de l’algorithme de compression d’image continue actuel.                                                                                                                                 |
| qualité toujours   | Retourne le nom du descripteur de qualité d’image continue actuel. Cela peut retourner « Unknown » si l’application a défini des paramètres sur des valeurs spécifiques qui ne correspondent pas aux qualités définies. |
| usage           | Retourne une chaîne qui décrit les restrictions d’utilisation qui peuvent être imposées par le propriétaire des données audio ou visuelles dans l’espace de travail.                                                                    |
| version         | Retourne le niveau de version du pilote de périphérique et du matériel.                                                                                                                                       |
| algorithme vidéo | Retourne le nom de l’algorithme de compression vidéo actuel.                                                                                                                                       |
| qualité vidéo   | Retourne le nom du descripteur de qualité vidéo actuel. Cela peut retourner « Unknown » si l’application a défini des paramètres sur des valeurs spécifiques qui ne correspondent pas aux qualités définies.       |
| texte de la fenêtre     | Récupère la légende de la fenêtre utilisée par l’appareil.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="examples"></a>Exemples

La commande suivante récupère une description du matériel associé à l’appareil « mySound ».

``` syntax
info mysound product
```

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

[load](load.md)
</dt> </dl>

 

