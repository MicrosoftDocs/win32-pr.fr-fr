---
description: La méthode SaveToBlob enregistre les données de propriété dans un format de persistance.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'IPropertySetter :: SaveToBlob, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540537"
---
# <a name="ipropertysettersavetoblob-method"></a>IPropertySetter :: SaveToBlob, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SaveToBlob` méthode enregistre les données de propriété dans un format de persistance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcSize* \[ à\]
</dt> <dd>

Reçoit la taille des données, en octets.

</dd> <dt>

*ppb* \[ à\]
</dt> <dd>

Reçoit un pointeur vers un tableau d’octets qui reçoit les données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La méthode alloue de la mémoire pour le tableau d’octets. L’appelant doit le libérer, à l’aide de la fonction **CoTaskMemFree** .

La longueur de tous les noms et valeurs de propriétés est tronquée à 40 caractères. C’est la raison pour laquelle XML est le format de persistance par défaut. Voir [**interface IXml2Dex**](ixml2dex.md).

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




