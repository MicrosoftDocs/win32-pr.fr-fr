---
description: La \_ méthode put ScaleX spécifie la quantité d’étirement horizontal de la réinitialisation.
ms.assetid: d57af5dc-41e0-45a7-8f11-55ef3bc62549
title: IDxtJpeg ::p ut_ScaleX, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fff0583ce3163ebf5626cfdbb82edf5c927bdc9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230309"
---
# <a name="idxtjpegput_scalex-method"></a>IDxtJpeg ::p ut \_ ScaleX, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_ScaleX` méthode spécifie la quantité d’étirement horizontal de la réinitialisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ScaleX(
  [in] double newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Valeur de l’étirement horizontal de la réinitialisation, sous la forme d’un pourcentage de la définition de la réinitialisation d’origine. Par exemple, la valeur 1,0 signifie aucun étirement, et 2,0 signifie l’étirement de 200%.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

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
</dt> </dl>

 

 




