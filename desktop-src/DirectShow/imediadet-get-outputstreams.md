---
description: La \_ méthode obtenir OutputStreams récupère le nombre de flux audio et vidéo contenus dans la source du média. Tous les autres types de flux, tels que les flux de données, sont ignorés.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'IMediaDet :: get_OutputStreams, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19081afd1c005c61d39fc91cda8c28a93fface2a03b672411ef6449f75fa66fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083749"
---
# <a name="imediadetget_outputstreams-method"></a>IMediaDet :: \_ OutputStreams, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_OutputStreams` méthode récupère le nombre de flux audio et vidéo contenus dans la source du média. Tous les autres types de flux, tels que les flux de données, sont ignorés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit le nombre de flux de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) pour définir le nom de fichier. Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG. Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

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

 

 




