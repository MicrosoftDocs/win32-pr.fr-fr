---
description: Ces indicateurs spécifient le mode de rendu d’une source vidéo si sa taille ne correspond pas aux dimensions de sortie.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Indicateurs de redimensionnement (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533395"
---
# <a name="resize-flags"></a>Indicateurs de redimensionnement

\[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

Ces indicateurs spécifient le mode de rendu d’une source vidéo si sa taille ne correspond pas aux dimensions de sortie.



| Constante/valeur                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt> </dl>                                                                          | L’image est étirée pour s’ajuster à la taille du cadre cible dans les deux dimensions, sans conserver les proportions.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_ ROGNAGE**</dt> <dt>1</dt> </dl>                                                                                   | L’image n’est pas redimensionnée. Si l’image est plus petite que le frame cible, la zone environnante est noire. Si l’image est plus grande que le frame cible, l’image est rognée.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | L’image est redimensionnée pour s’ajuster au frame cible sur une dimension, tout en conservant les proportions. Si le rapport entre la largeur et la hauteur dans l’image ne correspond pas au ratio dans le frame cible, elle crée une zone de bandes.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt> </dl> | L’image est redimensionnée pour remplir l’intégralité du frame cible tout en préservant les proportions. Au lieu de créer une bandes, ce mode rogne l’image, sur les côtés ou en haut et en bas.<br/>                 |



## <a name="remarks"></a>Notes

Les images suivantes montrent les effets de ces indicateurs.

![indicateurs de redimensionnement](images/stretch14.png)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




