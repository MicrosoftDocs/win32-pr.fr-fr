---
description: Crée un objet IContextNodes.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'IInkAnalyzer :: CreateContextNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523260"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a>IInkAnalyzer :: CreateContextNodes, méthode

Crée un objet [**IContextNodes**](icontextnodes.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppContextNodes* \[ à\]
</dt> <dd>

Pointeur vers l’objet [**IContextNodes**](icontextnodes.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

> [!Caution]  
> Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppContextNodes* lorsque vous n’avez plus besoin d’utiliser l’objet.

 

Utilisez cette méthode pour créer une collection [**IContextNodes**](icontextnodes.md) vide associée au [**IInkAnalyzer**](iinkanalyzer.md). La nouvelle collection **IContextNodes** ne fait pas partie de l’arborescence de contexte de l’objet **IInkAnalyzer** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

