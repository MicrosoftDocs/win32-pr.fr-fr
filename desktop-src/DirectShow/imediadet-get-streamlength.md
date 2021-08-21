---
description: La \_ méthode obtenir StreamLength récupère la durée du flux actuel.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'IMediaDet :: get_StreamLength, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f29b11c5b9b054a759648343ea8b27c8f883d044cd65073b0bddc5ea8884a6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154286"
---
# <a name="imediadetget_streamlength-method"></a>IMediaDet :: \_ StreamLength, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_StreamLength` méthode récupère la durée du flux actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit la durée du flux, en secondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG. Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




