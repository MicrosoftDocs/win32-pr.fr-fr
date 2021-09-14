---
description: La méthode QuerySupported détermine si un objet prend en charge un jeu de propriétés spécifié.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'IKsPropertySet :: QuerySupported, méthode (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240713"
---
# <a name="ikspropertysetquerysupported-method"></a>IKsPropertySet :: QuerySupported, méthode

La `QuerySupported` méthode détermine si un objet prend en charge un jeu de propriétés spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*guidPropSet* \[ dans\]
</dt> <dd>

GUID du jeu de propriétés.

</dd> <dt>

*dwPropID* \[ dans\]
</dt> <dd>

Identificateur de la propriété dans le jeu de propriétés.

</dd> <dt>

*pTypeSupport* \[ à\]
</dt> <dd>

Pointeur vers une valeur dans laquelle stocker des indicateurs indiquant la prise en charge fournie par le pilote. Les indicateurs pris en charge sont les suivants :



| Valeur                    | Description                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| \_prise en charge de KSPROPERTY \_ | Vous pouvez récupérer la propriété en appelant la méthode [**IKsPropertySet :: obtenir**](ikspropertyset-get.md) . |
| \_ensemble de support KSPROPERTY \_ | Vous pouvez modifier la propriété en appelant [**IKsPropertySet :: Set**](ikspropertyset-set.md).              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                              | Description                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Le jeu de propriétés et la combinaison d’ID de propriété spécifiés sont pris en charge.<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>                | Le jeu de propriétés n’est pas pris en charge.<br/>                                       |
| <dl> <dt>**\_ID prop \_ \_ non pris en charge**</dt> </dl>  | L’ID de propriété n’est pas pris en charge pour le jeu de propriétés spécifié.<br/>         |
| <dl> <dt>**jeu d’E \_ props \_ \_ non pris en charge**</dt> </dl> | Le jeu de propriétés n’est pas pris en charge.<br/>                                       |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h. Les deux interfaces ne sont pas compatibles. l’interface **IKsControl** , documentée dans le DirectShow DDK, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.

 

Vous devez inclure KS. h avant ksproxy. h.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                             |
| En-tête<br/>                   | <dl> <dt>KS. h ; </dt> <dt>Ksproxy. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 




