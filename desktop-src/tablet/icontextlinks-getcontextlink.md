---
description: Récupère le IContextLink à l’index spécifié.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'IContextLinks :: GetContextLink, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523281"
---
# <a name="icontextlinksgetcontextlink-method"></a>IContextLinks :: GetContextLink, méthode

Récupère le [**IContextLink**](icontextlink.md) à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulIndex* \[ dans\]
</dt> <dd>

Index de base zéro de l’objet [**IContextLink**](icontextlink.md) à récupérer.

</dd> <dt>

*ppContextLink* \[ à\]
</dt> <dd>

Pointeur vers l’objet [**IContextLink**](icontextlink.md) à l’index spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppContextLink* lorsque vous n’avez plus besoin d’utiliser le lien de contexte.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

