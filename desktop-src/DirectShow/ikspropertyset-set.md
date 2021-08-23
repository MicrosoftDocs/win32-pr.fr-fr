---
description: La méthode Set définit une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'IKsPropertySet :: Set, méthode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f3669acb7f2d3049b909a4dc2c24363bf478c9b44ad0a91528e1e8ea466399fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639189"
---
# <a name="ikspropertysetset-method"></a>IKsPropertySet :: Set, méthode

La `Set` méthode définit une propriété identifiée par un GUID de jeu de propriétés et un ID de propriété.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
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

*pInstanceData* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient les données d’instance pour la propriété.

</dd> <dt>

*cbInstanceData* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *pInstanceData* , en octets.

</dd> <dt>

*pPropData* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient la valeur de la propriété.

</dd> <dt>

*cbPropData* \[ dans\]
</dt> <dd>

Sise de la mémoire tampon *pPropData* , en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                              | Description                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                     | Réussite.<br/>                                                         |
| <dl> <dt>**jeu d’E \_ props \_ \_ non pris en charge**</dt> </dl> | Le jeu de propriétés n’est pas pris en charge.<br/>                               |
| <dl> <dt>**\_ID prop \_ \_ non pris en charge**</dt> </dl>  | L’ID de propriété n’est pas pris en charge pour le jeu de propriétés spécifié.<br/> |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Une autre interface portant ce nom existe dans le fichier d’en-tête dsound. h. Les deux interfaces ne sont pas compatibles. l’interface **IKsControl** , documentée dans le DirectShow DDK, est désormais l’interface recommandée pour passer des jeux de propriétés entre les pilotes WDM et les composants en mode utilisateur.

 

Vous devez inclure KS. h avant ksproxy. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothèque<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IKsPropertySet**](ikspropertyset.md)
</dt> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 




