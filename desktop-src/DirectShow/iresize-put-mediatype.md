---
description: La \_ méthode put MediaType définit le type de média de sortie sur le filtre de redimensionnement.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: IResize ::p ut_MediaType, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6c26878af6f091efd3c3f321cb073ce51a8e6236d4bafa326ab99f85f39e1a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818200"
---
# <a name="iresizeput_mediatype-method"></a>IResize ::p ut \_ MediaType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_MediaType` méthode définit le type de média de sortie sur le filtre de redimensionnement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PMT* \[ dans\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui contient le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

DES appelle cette méthode avant de connecter la broche de sortie du filtre. Utilisez le type de média comme type de média de la broche de sortie. Retournez ce type de média dans la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) et vérifiez agsint ce type dans la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) . DES n’appelle jamais cette méthode une fois que la broche de sortie est connectée.

Actuellement, le définit toujours le type de média de sortie sur un format RVB non compressé avec un bloc de format **VIDEOINFOHEADER** (le type de format est égal au format \_ videoinfo). Le sous-type peut être MEDIASUBTYPE \_ ARGB32, qui indique la couleur rvb 32 bits avec un canal alpha.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 ou version ultérieure<br/>                                                         |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IResize**](iresize.md)
</dt> </dl>

 

 




