---
description: La \_ méthode obtenir alpha récupère la valeur alpha de la totalité de l’image.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'IDxtAlphaSetter :: get_Alpha, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 054e2a1745f96dc4d6ea846bed0448948fae8407dd6ab44d2796742e405f2e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051969"
---
# <a name="idxtalphasetterget_alpha-method"></a>IDxtAlphaSetter :: obtient la \_ méthode alpha

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_Alpha` méthode récupère la valeur alpha de la totalité de l’image.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Reçoit la valeur alpha. Cette valeur alpha sera appliquée à l’intégralité de l’image cible. Une valeur négative indique qu’aucune valeur alpha n’est définie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                               | Description                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null**<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Succès<br/>                   |



 

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

[**Interface IDxtAlphaSetter**](idxtalphasetter.md)
</dt> </dl>

 

 




