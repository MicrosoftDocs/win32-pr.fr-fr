---
description: La méthode EnterBitmapGrabMode bascule le détecteur de média en mode de manipulation bitmap et recherche le graphique de filtre à une heure spécifiée.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'IMediaDet :: EnterBitmapGrabMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d47989b95663a9a99f4363fb505aec996ea23acdd813cf301f7ee252c874dc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952618"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>IMediaDet :: EnterBitmapGrabMode, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `EnterBitmapGrabMode` méthode bascule le détecteur de média en mode de manipulation bitmap et recherche le graphique de filtre à une heure spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StreamTime* 
</dt> <dd>

Durée, en secondes, à laquelle le graphique recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                             | Description                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argument non valide.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Le fichier source n’a pas de flux vidéo.<br/> |
| <dl> <dt>**VFW \_ E \_ temps \_ expiré**</dt> </dl>    | Délai d’attente de la commande Seek dépassé.<br/>                       |



 

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Cette méthode insère l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) dans le graphique de filtre. Vous pouvez ensuite appeler [**IMediaDet :: GetSampleGrabber**](imediadet-getsamplegrabber.md) pour obtenir un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) . Une fois que le détecteur de média passe en mode de manipulation bitmap, les différentes méthodes d’information dans **IMediaDet** ne fonctionnent pas.

Les méthodes [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md) placent également le détecteur de média en mode de manipulation bitmap.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




