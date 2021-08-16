---
description: La \_ méthode put RGB spécifie la couleur RVB sur laquelle la touche est enfoncée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: IDxtKey ::p ut_RGB, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f53cb5d856377b611c5ea90d3b9c1f7fa522d892e6c79aa50d350883497398a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819392"
---
# <a name="idxtkeyput_rgb-method"></a>IDxtKey : méthode :p ut \_ RGB

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_RGB` méthode spécifie la couleur RVB sur laquelle la touche est enfoncée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Spécifie la couleur sous la forme d’un nombre hexadécimal au format 0xRRGGBB, où RR est la valeur rouge, GG est la valeur verte et BB est la valeur bleue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

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

[**Interface IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey ::p \_ type ut**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




