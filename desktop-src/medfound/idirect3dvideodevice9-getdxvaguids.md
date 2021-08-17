---
description: Obtient une liste des profils d’accélération vidéo DirectX (DXVA) pris en charge par le pilote d’affichage.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9 :: GetDXVAGuids, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 6a355c27177a546a2e91e769f72d9f4b9e216b005f711d42b5b7af39b4b78361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269239"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>IDirect3DVideoDevice9 :: GetDXVAGuids, méthode

Obtient une liste des profils d’accélération vidéo DirectX (DXVA) pris en charge par le pilote d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNumGuids* 
</dt> <dd>

En entrée, spécifie le nombre d’éléments dans le tableau *pGuids* . Si *pGuids* a la valeur **null**, la valeur de `*pNumGuids` doit être égale à zéro.

En sortie, si *pGuids* a la **valeur null**, *pNumGuids* reçoit le nombre de profils DXVA en mode restreint. Sinon, *pNumGuids* reçoit le nombre réel de GUID copiés dans le tableau *pGuids* .

</dd> <dt>

*pGuids* 
</dt> <dd>

Adresse d’un tableau de GUID ou **null**. Si la valeur n’est pas **null**, le tableau reçoit une liste de GUID qui spécifient des profils DXVA en mode restreint. Ces GUID sont définis dans DXVA. h et sont documentés dans la [spécification dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Appelez cette méthode deux fois. Lors du premier appel, affectez à *pGuids* la **valeur null**. Le paramètre *pNumGuids* reçoit le nombre de GUID du profil DXVA. Allouez un tableau de GUID avec la taille requise et rappelez la méthode. Cette fois-ci, définissez *pGuids* sur l’adresse du tableau. La méthode remplit le tableau avec la liste des GUID de profil DXVA.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
