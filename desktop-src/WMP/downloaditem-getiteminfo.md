---
title: Méthode DownloadItem. getItemInfo
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode getItemInfo récupère la valeur d’un attribut pour l’élément de téléchargement.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, classe DownloadItem
- Classe DownloadItem lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530299"
---
# <a name="downloaditemgetiteminfo-method"></a>Méthode DownloadItem. getItemInfo

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **getItemInfo** récupère la valeur d’un attribut pour l’élément de téléchargement.

## <a name="syntax"></a>Syntaxe


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ItemName* \[ dans\]
</dt> <dd>

**Chaîne** contenant le nom de l’attribut. Les valeurs prises en charge sont AlbumArtist, album, Duration, WM/Provider, title, UserRating et WM/TrackNumber.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne une **chaîne** contenant la valeur de l’attribut spécifié par *ItemName*.

## <a name="remarks"></a>Notes

Cette méthode récupère les attributs spécifiés à l’aide de la chaîne de description BITS. Consultez la [Convention de travail bits du lecteur Windows Media](windows-media-player-bits-job-convention.md).

Cette méthode est prise en charge pour le téléchargement en arrière-plan. Votre code ne doit pas appeler cette méthode lors de l’utilisation d’un téléchargement en temps réel.

Cette méthode peut récupérer des informations sur les tâches BITS ajoutées au cours de la session du lecteur Windows Media en cours uniquement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DownloadItem. type**](downloaditem-type.md)
</dt> <dt>

[**Objet DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





