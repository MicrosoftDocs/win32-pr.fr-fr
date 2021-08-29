---
description: La méthode GetProps récupère les propriétés définies sur cet objet, avec leurs valeurs correspondantes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'IPropertySetter :: GetProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 10a2f1cd8be327a288d37ddee8acf3a7f02433897c938bebaf7ad2aa3af24105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131029"
---
# <a name="ipropertysettergetprops-method"></a>IPropertySetter :: GetProps, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetProps` méthode récupère les propriétés définies sur cet objet, avec leurs valeurs correspondantes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcParams* \[ à\]
</dt> <dd>

Reçoit le nombre de structures retournées dans *paParam*.

</dd> <dt>

*paParam* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers un tableau de structures de [**\_ paramètres Dexter**](dexter-param.md) .

</dd> <dt>

*paValue* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers un tableau de structures de [**\_ valeur Dexterity**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Pour chaque propriété retournée dans *paParam*, le membre **nvaleurs** indique le nombre de structures de [**\_ valeur dexterisation**](dexter-value.md) associées à la propriété. Les paires sont retournées dans l’ordre chronologique croissant de chaque propriété.

Lorsque vous avez terminé d’utiliser les structures retournées, appelez [**IPropertySetter :: FreeProps**](ipropertysetter-freeprops.md) pour libérer les ressources allouées par cette méthode.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment itérer au sein de toutes les valeurs sur une instance de l’accesseur Set de propriété :


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



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

 

 




