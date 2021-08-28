---
description: La méthode GetPropertySetter récupère l’accesseur Set de la propriété de l’objet. Lorsque l’objet est rendu, les informations de propriété contenues dans l’accesseur Set de propriété sont appliquées à l’objet.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'IAMTimelineObj :: GetPropertySetter, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd86d1c0b8334c1587745278ee499e38113887bb074770f49364429f71fa53da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831079"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>IAMTimelineObj :: GetPropertySetter, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetPropertySetter` méthode récupère l’accesseur Set de la propriété de l’objet. Lorsque l’objet est rendu, les informations de propriété contenues dans l’accesseur Set de propriété sont appliquées à l’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IPropertySetter**](ipropertysetter.md) de l’accesseur Set de la propriété. Si l’objet n’a pas de méthode setter de propriété, la valeur est **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si la valeur retournée dans *pval* n’est pas **null**, l’interface **IPropertySetter** a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




