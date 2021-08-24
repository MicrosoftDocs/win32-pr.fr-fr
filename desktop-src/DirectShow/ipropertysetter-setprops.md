---
description: La méthode SetProps définit les propriétés de l’objet cible à l’état approprié pour l’heure spécifiée.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'IPropertySetter :: SetProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3b5a1832897b52d21c57e26595b7d66c4fc9a53f2bcbee0090c53d00f8fe832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767209"
---
# <a name="ipropertysettersetprops-method"></a>IPropertySetter :: SetProps, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetProps` méthode définit les propriétés de l’objet cible à l’état approprié pour l’heure spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTarget* \[ dans\]
</dt> <dd>

Pointeur vers l’objet cible pour lequel définir les propriétés.

</dd> <dt>

*rtNow* \[ dans\]
</dt> <dd>

Heure à laquelle définir les propriétés, en unités de 100 nanosecondes, ou-1 pour définir des propriétés statiques (celles qui ne varient pas au fil du temps).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée par DES pour définir les propriétés sur une transition ou un effet. Une application n’appelle normalement pas cette méthode.

L’objet spécifié par *pTarget* doit implémenter l’interface **IDispatch** .

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




