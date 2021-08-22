---
description: Libère un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété chainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'IChainContext :: FreeContext, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 10a6d0576cefd1c28e8f05fe455b89be90dcd36386b4312ef1921511616bce2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005487"
---
# <a name="ichaincontextfreecontext-method"></a>IChainContext :: FreeContext, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La méthode **FreeContext** libère un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="syntax"></a>Syntaxe


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pChainContext* \[ dans\]
</dt> <dd>

\_Contexte de la chaîne PCCERT \_ à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique la réussite de l’opération. Toute autre valeur indique que l’opération a échoué.

## <a name="remarks"></a>Remarques

Cette méthode ne libère pas le \_ contexte de chaîne PCCERT \_ contenu dans un objet [**chaîne**](chain.md) . Elle doit être utilisée uniquement pour libérer un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




