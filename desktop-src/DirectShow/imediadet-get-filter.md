---
description: La \_ méthode de filtre d’extraction récupère un pointeur vers le filtre source actuellement utilisé par le détecteur de média.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'IMediaDet :: get_Filter, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c3d4622438dbb8c8dfc54183550c274fcd4555de8b75435b85bbbebfae9c2c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083759"
---
# <a name="imediadetget_filter-method"></a>IMediaDet :: obtient la \_ méthode de filtre

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Filter` méthode récupère un pointeur vers le filtre source actuellement utilisé par le détecteur de média.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppVal* \[ out, retval\]
</dt> <dd>

Reçoit un pointeur vers l’interface **IUnknown** du filtre. Si aucun filtre source n’est utilisé, la valeur est définie sur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Lorsque la méthode est retournée, si *\* ppVal* n’a pas la **valeur null**, l’interface **IUnknown** a un nombre de références en attente. Libérez l’interface une fois que vous avez fini de l’utiliser.

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

 

 




