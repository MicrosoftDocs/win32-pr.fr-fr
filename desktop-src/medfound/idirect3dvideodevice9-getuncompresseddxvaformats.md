---
description: Obtient une liste de formats de pixel non compressés qui peuvent être rendus à l’aide d’un profil d’accélération vidéo DirectX (DXVA) spécifié.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9 :: GetUncompressedDXVAFormats, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319006"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>IDirect3DVideoDevice9 :: GetUncompressedDXVAFormats, méthode

Obtient une liste de formats de pixel non compressés qui peuvent être rendus à l’aide d’un profil d’accélération vidéo DirectX (DXVA) spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGuid* 
</dt> <dd>

Pointeur vers un GUID qui spécifie le profil DXVA. Pour obtenir la liste des profils pris en charge, appelez [**IDirect3DVideoDevice9 :: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

En entrée, spécifie le nombre d’éléments dans le tableau *pFormats* . Si *pFormats* a la valeur **null**, la valeur de `*pNumFormats` doit être égale à zéro.

En sortie, si *pFormats* a la **valeur null**, *pNumFormats* reçoit le nombre de formats de pixel pris en charge. Sinon, *pNumFormats* reçoit le nombre réel de formats de pixel copiés dans le tableau *pFormats* .

</dd> <dt>

*pFormats* 
</dt> <dd>

Adresse d’un tableau de valeurs **D3DFORMAT** , ou **null**. Si la valeur n’est pas **null**, le tableau reçoit une liste de formats de pixel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Appelez cette méthode deux fois. Lors du premier appel, affectez à *pFormats* la **valeur null**. Le paramètre *pNumFormats* reçoit le nombre de formats. Allouez un tableau **D3DFORMAT** avec la taille requise, puis rappelez la méthode. Cette fois-ci, définissez *pFormats* sur l’adresse du tableau. La méthode remplit le tableau avec la liste des formats de pixel.

Le pilote doit retourner les formats dans l’ordre de préférence décroissant, avec le format le plus préféré listé en premier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




