---
description: 'La méthode FreeProps libère les ressources allouées par la méthode IPropertySetter :: GetProps. Appelez cette méthode après avoir appelé GetProps, en lui transmettant les structures retournées par GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'IPropertySetter :: FreeProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530947"
---
# <a name="ipropertysetterfreeprops-method"></a>IPropertySetter :: FreeProps, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `FreeProps` méthode libère les ressources allouées par la méthode [**IPropertySetter :: GetProps**](ipropertysetter-getprops.md) . Appelez cette méthode après avoir appelé **GetProps**, en lui transmettant les structures retournées par **GetProps**.

## <a name="syntax"></a>Syntaxe


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cParams* \[ dans\]
</dt> <dd>

Nombre d’éléments dans le tableau *paParam* .

</dd> <dt>

*paParam* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures de [**\_ paramètres Dexter**](dexter-param.md) .

</dd> <dt>

*paValue* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures de [**\_ valeur Dexterity**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

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

 

 




