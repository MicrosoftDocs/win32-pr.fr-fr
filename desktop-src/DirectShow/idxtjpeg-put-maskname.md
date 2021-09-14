---
description: La \_ méthode put MaskName spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: IDxtJpeg ::p ut_MaskName, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230352"
---
# <a name="idxtjpegput_maskname-method"></a>IDxtJpeg ::p ut \_ MaskName, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_MaskName` méthode spécifie le nom d’un fichier JPEG à utiliser comme masque de réinitialisation. Ce masque sera utilisé à la place de l’un des masques de réinitialisation intégrés. Le fichier doit contenir un dégradé monochrome, 8 bits par pixel. Le dégradé est utilisé comme masque pour définir la progression de la réinitialisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Spécifie le nom du fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Pour revenir à un masque intégré, définissez la propriété **MaskNum** .

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IDxtJpeg**](idxtjpeg.md)
</dt> <dt>

[**IDxtJpeg ::p ut \_ MaskNum**](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




