---
description: Obtient des informations sur les mémoires tampons compressées nécessaires au décodage accéléré par le matériel.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9 :: GetDXVACompressedBufferInfo, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530837"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>IDirect3DVideoDevice9 :: GetDXVACompressedBufferInfo, méthode

Obtient des informations sur les mémoires tampons compressées nécessaires au décodage accéléré par le matériel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGuid* 
</dt> <dd>

Pointeur vers un GUID qui spécifie le profil DXVA. Pour obtenir la liste des profils pris en charge, appelez [**IDirect3DVideoDevice9 :: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Pointeur vers une structure [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) qui spécifie la taille et le format de pixel des données non compressées.

</dd> <dt>

*pNumBuffers* 
</dt> <dd>

En entrée, spécifie le nombre d’éléments dans le tableau *pBufferInfo* . Si *pBufferInfo* a la valeur **null**, la valeur de `*pNumBuffers` doit être égale à zéro.

En sortie, si *pBufferInfo* a la **valeur null**, *pNumBuffers* reçoit la taille du tableau à allouer. Sinon, *pNumBuffers* reçoit le nombre réel d’éléments qui sont copiés dans le tableau *pBufferInfo* .

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Adresse d’un tableau de structures [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) ou **null**. Si la valeur n’est pas **null**, la méthode copie une liste de structures **DXVACompBufferInfo** dans ce tableau. Chaque structure correspond à un type de tampon de données compressé utilisé par l’accélérateur vidéo.

Affectez à tous les éléments du tableau la valeur zéro avant d’appeler cette méthode.

Chaque index de tableau correspond à l’un des types de surface DXVA définis dans DXVA. h. L’accélérateur vidéo renvoie une liste des entrées de tableau de **\_ \_ \_ \_ mémoires tampons de type nombre** jusqu’à DXVA. Pour plus d’informations, reportez-vous à la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration), section 3,4, « liste des descriptions de tampon ». Si un type de mémoire tampon spécifique n’est pas utilisé par le profil DXVA, l’entrée à cet index contient des zéros pour toutes les valeurs.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
