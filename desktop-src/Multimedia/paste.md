---
title: commande Coller
description: La commande Coller copie le contenu du presse-papiers dans l’espace de travail. Les périphériques vidéo numériques reconnaissent cette commande.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- commande coller Windows multimédia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363927"
---
# <a name="paste-command"></a>commande Coller

La commande Coller copie le contenu du presse-papiers dans l’espace de travail. Les périphériques vidéo numériques reconnaissent cette commande.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Un ou plusieurs des indicateurs suivants.



| Valeur                 | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| au niveau du *rectangle*        | Spécifie l’emplacement dans le frame où les données sont collées. L’angle supérieur gauche du *rectangle* correspond au coin supérieur gauche des données ajoutées. Si le rectangle a une taille différente de zéro dans X ou Y, le contenu du presse-papiers est mis à l’échelle dans ces dimensions lorsqu’elles sont collées dans le cadre. En cas d’omission, le *rectangle* a comme valeur par défaut l’ensemble du frame. Si cet indicateur est spécifié en mode « Insert » (valeur par défaut), toute région située à l’extérieur du rectangle est peinte avec une couleur unie.                       |
| *flux* de flux audio | Spécifie le flux audio dans l’espace de travail affecté par la commande. S’il n’existe qu’un seul flux audio dans le presse-papiers, les données audio sont collées dans le *flux* désigné. Si plusieurs flux audio existent dans le presse-papiers, le *flux* indique le numéro de départ des séquences de flux. Si vous utilisez cet indicateur et que vous souhaitez également coller la vidéo, vous devez également utiliser l’indicateur « flux vidéo ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés et conservent leurs numéros de flux d’origine.) |
| insert                | Spécifie que les données sont insérées dans l’espace de travail. Toutes les données qui suivent le point d’insertion sont déplacées vers l’avant dans l’espace de travail pour faire de la place. Il s’agit de la valeur par défaut.                                                                                                                                                                                                                                                                                                                                                    |
| overwrite             | Spécifie que les données sont copiées dans l’espace de travail en écrivant sur les données existantes après le point d’insertion. Les indicateurs « Insert » et « overwrite » déterminent si les images sont détruites ou déplacées pendant l’opération de collage, et non la manière dont les données sont collées dans chaque image.                                                                                                                                                                                                                                              |
| pour *positionner*         | Spécifie la position dans l’espace de travail à laquelle les données sont collées. En cas d’omission, sa valeur par défaut est la position actuelle.                                                                                                                                                                                                                                                                                                                                                                                                    |
| *flux* de flux vidéo | Spécifie le flux vidéo dans l’espace de travail affecté par la commande. S’il n’existe qu’un seul flux vidéo dans le presse-papiers, les données vidéo sont collées dans le *flux* désigné. Si plusieurs flux vidéo existent dans le presse-papiers, le *flux* indique le numéro de départ des séquences de flux. Si vous utilisez cet indicateur et que vous souhaitez également coller l’audio, vous devez également utiliser l’indicateur « flux audio ». (Si aucun indicateur n’est spécifié, tous les flux audio et vidéo sont collés et conservent leurs numéros de flux d’origine.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », « test » ou une combinaison de ceux-ci. Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Aucun signal n’est présent dans les données copiées à partir du presse-papiers. La modification devient permanente uniquement lorsque les données sont enregistrées de manière explicite ; Toutefois, la lecture agit comme si les données avaient été ajoutées.

## <a name="requirements"></a>Spécifications



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

 

