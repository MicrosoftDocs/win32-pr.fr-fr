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
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542367"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>IMediaDet :: EnterBitmapGrabMode, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

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
| <dl> <dt>**\_OK**</dt> </dl>                    | Opération réussie.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Argument non valide.<br/>                             |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Le fichier source n’a pas de flux vidéo.<br/> |
| <dl> <dt>**VFW \_ E \_ temps \_ expiré**</dt> </dl>    | Délai d’attente de la commande Seek dépassé.<br/>                       |



 

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Cette méthode insère l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) dans le graphique de filtre. Vous pouvez ensuite appeler [**IMediaDet :: GetSampleGrabber**](imediadet-getsamplegrabber.md) pour obtenir un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) . Une fois que le détecteur de média passe en mode de manipulation bitmap, les différentes méthodes d’information dans **IMediaDet** ne fonctionnent pas.

Les méthodes [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md) placent également le détecteur de média en mode de manipulation bitmap.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

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

 

 




