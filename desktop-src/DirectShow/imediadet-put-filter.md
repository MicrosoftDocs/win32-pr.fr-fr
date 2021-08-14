---
description: La \_ méthode de filtre put spécifie un filtre source pour le détecteur de média à utiliser.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: IMediaDet ::p ut_Filter, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a118baae251bd4456dfe0097afa091e0084e41ad96d96c9847006b8ce9c58d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398116"
---
# <a name="imediadetput_filter-method"></a>IMediaDet ::p \_ méthode de filtre ut

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_Filter` méthode spécifie un filtre source pour le détecteur de média à utiliser.

> [!IMPORTANT]
> N’ajoutez pas le filtre source à votre propre graphique de filtre ou utilisez un filtre qui figure déjà dans un graphique de filtre. L’objet détecteur de média crée automatiquement un graphique de filtres interne, et le fait de placer le filtre dans un autre graphique peut entraîner des résultats inattendus.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Pointeur vers l’interface **IUnknown** du filtre source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                   | Description                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *newVal* ne pointe pas vers un filtre.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/>           |



 

## <a name="remarks"></a>Remarques

Pour la plupart des applications, il est plus simple d’appeler la méthode [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) avec le nom d’un fichier source.

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

 

 




