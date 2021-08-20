---
title: Méthode DownloadItem. getItemInfo
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode getItemInfo récupère la valeur d’un attribut pour l’élément de téléchargement.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- Lecteur Windows Media de la méthode getItemInfo
- méthode getItemInfo Lecteur Windows Media, classe DownloadItem
- Lecteur Windows Media de la classe DownloadItem, méthode getItemInfo
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
ms.openlocfilehash: e51414f70d518c37c560ee6f4db66994ed0cc0cadd95fc44e9f0d569601617ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935838"
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

## <a name="remarks"></a>Remarques

Cette méthode récupère les attributs spécifiés à l’aide de la chaîne de description BITS. consultez [Lecteur Windows Media Convention de travail BITS](windows-media-player-bits-job-convention.md).

Cette méthode est prise en charge pour le téléchargement en arrière-plan. Votre code ne doit pas appeler cette méthode lors de l’utilisation d’un téléchargement en temps réel.

cette méthode peut récupérer des informations pour les tâches BITS ajoutées au cours de la session de Lecteur Windows Media actuelle uniquement.

## <a name="requirements"></a>Conditions requises



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

 

 





