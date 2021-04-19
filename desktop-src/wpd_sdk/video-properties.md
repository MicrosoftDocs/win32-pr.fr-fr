---
description: Appareils mobiles Windows prend en charge les propriétés vidéo suivantes.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Propriétés de la vidéo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525198"
---
# <a name="video-properties"></a>Propriétés de la vidéo

Appareils mobiles Windows prend en charge les propriétés vidéo suivantes.



| Propriété                                         | VarType        | Description                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_auteur de vidéo wpd \_**                           | **\_LPWStr VT** | Auteur du fichier vidéo.                                                                                                                                                                                                                           |
| **\_vitesse de \_ transmission vidéo wpd**                          | **VT \_ UI4**    | Vitesse de transmission du fichier vidéo.                                                                                                                                                                                                                         |
| **taille de la \_ \_ mémoire tampon vidéo wpd \_**                     | **VT \_ UI4**    | Valeur qui spécifie la taille de mémoire tampon vidéo requise pour restituer ce fichier.                                                                                                                                                                              |
| **\_crédits vidéo \_ wpd**                          | **\_LPWStr VT** | Les crédits qui répertorient le cast et l’équipage de la vidéo.                                                                                                                                                                                                    |
| **\_ \_ code FourCC vidéo \_ wpd**                     | **\_DWORD VT**  | Code FourCC inscrit qui indique le codec utilisé pour le fichier vidéo. Pour obtenir la liste des formats FourCC, consultez l’article sur les [codes FourCC et les formats Wave inscrits](https://msdn2.microsoft.com/library/ms867195.aspx) sur le site Web MSDN. |
| **\_fréquence d’images vidéo wpd \_**                        | **VT \_ UI4**    | Fréquence d’images du fichier vidéo, en images/seconde x 1 000. Par exemple, une fréquence d’images de 29,97 est représentée sous la forme 29970.                                                                                                                                 |
| **\_genre vidéo \_ wpd**                            | **\_LPWStr VT** | Genre de ce fichier vidéo. Il n’existe aucune définition de genre standard.                                                                                                                                                                                  |
| **DISTANCE de l’image de la \_ clé vidéo wpd \_ \_ \_**             | **VT \_ UI4**    | Intervalle, en millisecondes, entre les images clés.                                                                                                                                                                                                       |
| **\_paramètre de \_ qualité \_ vidéo wpd**                 | **VT \_ UI4**    | Paramètre de qualité du fichier vidéo. Cela dépend du codec.                                                                                                                                                                                        |
| **\_numéro de \_ \_ canal RECORDEDTV vidéo wpd \_**      | **VT \_ UI4**    | Numéro du canal de télévision à partir duquel la vidéo a été enregistrée.                                                                                                                                                                                              |
| **\_Description du \_ \_ programme RECORDEDTV vidéo wpd \_** | **\_LPWStr VT** | Description du programme de télévision enregistré.                                                                                                                                                                                                       |
| **\_RECORDEDTV vidéo \_ wpd \_ répéter**               | **VT \_ bool**   | Valeur booléenne qui spécifie si le programme de télévision était une répétition affichée.                                                                                                                                                                     |
| **\_nom de \_ la \_ station RECORDEDTV vidéo \_ wpd**        | **\_LPWStr VT** | Station de télévision à partir de laquelle la vidéo a été enregistrée.                                                                                                                                                                                                |
| **\_type d' \_ analyse \_ vidéo wpd**                       | **VT \_ UI4**    | Énumérateur [**de \_ \_ \_ types d’analyses vidéo wpd**](wpd-video-scan-types.md) qui spécifie l’entrelacement du fichier vidéo.                                                                                                                                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




