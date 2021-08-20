---
description: La méthode obtenir la \_ similarité récupère la plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'IDxtKey :: get_Similarity, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dda31145fe28f0b428189eafd3105ae56120fbc19e0c611ad0df8d9f511130a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399139"
---
# <a name="idxtkeyget_similarity-method"></a>IDxtKey :: obtient \_ la méthode de similarité

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Similarity` méthode récupère la plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Reçoit la valeur de similarité.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

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

[**Interface IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey :: obtient \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




