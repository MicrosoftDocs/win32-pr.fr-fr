---
title: Commande list
description: La commande list détermine le nombre et les types d’entrées vidéo et audio. Les appareils vidéo numériques et VCR reconnaissent cette commande.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- commande de liste Windows multimédia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8881c85d146ce869e41d234a72190901135d233f8e45d580d5f568c4ccc48da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139472"
---
# <a name="list-command"></a>Commande list

La commande list détermine le nombre et les types d’entrées vidéo et audio. Les appareils vidéo numériques et VCR reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("list %s %s %s"), 
  lpszDeviceID, 
  lpszList, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*
</dt> <dd>

Indicateur qui identifie le nombre et les types d’entrées vidéo et audio. Le tableau suivant répertorie les types d’appareils qui reconnaissent la commande de **liste** et les indicateurs utilisés par chaque type.



| Valeur        | Signification                                                                           | Signification                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | *index* *audio de* l’algorithme de qualité audio algorithmaudio streamcountnumber | tout de même, *algorithmstill Video Algorithm* Algorithm algorithmvideo Quality Algorithm *Algorithm Video sourcevideo* Stream |
| vidéo          | *index* du numéro de source countaudio source audio                                     | source vidéo countvideo *index* de nombre source                                                                                |



 

Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le paramètre **lpszList** et leurs significations.



| Valeur                               | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algorithme audio                     | Spécifie que la commande doit récupérer les noms des algorithmes audio.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algorithme* de l’algorithme de qualité audio | Spécifie que la commande doit récupérer les niveaux de qualité associés à l' *algorithme* spécifié. Si l' *algorithme* est « Current », le niveau de qualité de l’algorithme actuel est retourné.                                                                                                                                                                                                                                                                                                   |
| nombre de sources audio                  | Retourne le nombre total d’entrées audio.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *index* du numéro de la source audio         | Retourne le type d’entrée audio de l' *index* source.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| flux audio                        | Spécifie que la commande doit récupérer les noms des flux audio associés à l’espace de travail. Ces chaînes (telles que « English » ou « German ») sont incorporées dans le fichier et identifient le flux.                                                                                                                                                                                                                                                                                    |
| count                               | Retourne le nombre d’options du type spécifié.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *index* de nombre                      | Retourne une chaîne décrivant une option spécifique (telle qu’elle est identifiée par l' *index*) du type d’option spécifié. L' *index* doit être un entier compris entre 1 et la valeur retournée par « Count ».                                                                                                                                                                                                                                                                                                         |
| algorithme toujours                     | Spécifie que la commande doit récupérer des noms d’algorithmes toujours.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| algorithme de qualité continue ( *algorithme* ) | Spécifie que la commande doit récupérer les niveaux de qualité associés à l' *algorithme* continue spécifié. Si l' *algorithme* est « Current », le niveau de qualité de l’algorithme actuel est retourné.                                                                                                                                                                                                                                                                                             |
| algorithme vidéo                     | Spécifie que la commande doit récupérer les noms des algorithmes vidéo.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algorithme* de qualité vidéo | Spécifie que la commande doit récupérer les niveaux de qualité associés à l' *algorithme* vidéo spécifié. Si l' *algorithme* est « Current », le niveau de qualité de l’algorithme actuel est retourné.                                                                                                                                                                                                                                                                                             |
| source vidéo                        | Spécifie que la commande doit retourner des informations sur les sources vidéo. Lorsqu’il est utilisé avec l’indicateur « Count », il retourne le nombre de sources vidéo. Lorsqu’il est utilisé avec l’indicateur « nombre », il retourne le type d’une source vidéo. MCI définit les constantes suivantes pour le type : « NTSC », « RGB », « PAL », « SECAM », « Svideo » et « générique ». Plusieurs sources de chaque type peuvent être retournées. Le type de source « générique » est utilisé lorsque plusieurs signaux sont autorisés pour ce connecteur. |
| nombre de sources vidéo                  | Retourne le nombre total d’entrées vidéo.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *index* du numéro de source de la vidéo         | Retourne le type d’entrée vidéo de l' *index* source.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| flux vidéo                        | Spécifie que la commande doit récupérer les noms des flux vidéo associés à l’espace de travail. Ces chaînes (telles que « fin drôle » ou « fin triste ») sont incorporées dans le fichier et identifient le flux.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify » ou « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Pour les périphériques VCR, vous devez spécifier « source vidéo » ou « source audio » avec les indicateurs « nombre » ou « nombre ». Si « Count » est spécifié, le nombre total d’entrées de vidéo ou audio est retourné. Si « number » est spécifié, le pilote retourne un type correspondant à l’entrée. Le type peut être l’un des suivants : « Tuner », « line », « Svideo », « aux » ou « Generic ». En règle générale, vous devez d’abord interroger le magnétoscope pour obtenir le « nombre », puis utiliser le nombre comme plage pour l’indicateur « nombre ». Les nombres « sources » commencent à 1.

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
</dt> </dl>

 

