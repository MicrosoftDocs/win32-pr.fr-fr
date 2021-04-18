---
description: La méthode GetSampleGrabber récupère un pointeur vers l’interface ISampleGrabber, qui permet à une application de récupérer des échantillons individuels à partir d’un flux de média.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'IMediaDet :: GetSampleGrabber, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526077"
---
# <a name="imediadetgetsamplegrabber-method"></a>IMediaDet :: GetSampleGrabber, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetSampleGrabber` méthode récupère un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) , qui permet à une application de récupérer des échantillons individuels à partir d’un flux de média.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppVal* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Appelez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) avant d’appeler cette méthode. L’interface [**ISampleGrabber**](isamplegrabber.md) vous permet de récupérer des échantillons de médias individuels à partir du flux. Si vous avez simplement besoin d’une image bitmap d’une image vidéo, appelez la méthode [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) à la place. L’interface **ISampleGrabber** est plus souple, mais elle nécessite plus de travail que l’application.

Si cette méthode est réussie, l’interface [**ISampleGrabber**](isamplegrabber.md) qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

 

 




