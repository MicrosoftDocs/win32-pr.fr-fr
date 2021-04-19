---
description: La \_ méthode obtenir MaskName récupère le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'IDxtJpeg :: get_MaskName, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535900"
---
# <a name="idxtjpegget_maskname-method"></a>IDxtJpeg :: \_ MaskName, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `get_MaskName` méthode récupère le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit le nom de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si la transition de réinitialisation utilise l’une des réinitialisations SMPTE intégrées qu’elle prend en charge, la valeur de cette propriété est une chaîne vide.

L’appelant doit libérer la chaîne retournée à l’aide de la fonction **SysFreeString** .

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

[**Interface IDxtJpeg**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg :: obtient \_ MaskNum**](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




