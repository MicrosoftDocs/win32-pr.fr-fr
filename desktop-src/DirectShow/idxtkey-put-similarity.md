---
description: La \_ méthode put similarité spécifie la plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: IDxtKey ::p ut_Similarity, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5dbd14b2791441f5c09a7242d6f8c1e343413f8c3cd94fc0519ac6487857b7d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399129"
---
# <a name="idxtkeyput_similarity-method"></a>IDxtKey ::p \_ méthode de similarité de la ut

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_Similarity` méthode spécifie la plage de données de couleur qui devient transparente. À des valeurs plus élevées, une plus grande plage de couleurs similaires est transparente. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB ou DXTKEY \_ NONRED.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Spécifie la valeur de similarité. La plage valide est comprise entre 0 et 100.

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

[**IDxtKey ::p \_ type ut**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




