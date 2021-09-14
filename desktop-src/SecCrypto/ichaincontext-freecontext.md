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
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237569"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique la réussite de l’opération. Toute autre valeur indique que l’opération a échoué.

## <a name="remarks"></a>Notes

Cette méthode ne libère pas le \_ contexte de chaîne PCCERT \_ contenu dans un objet [**chaîne**](chain.md) . Elle doit être utilisée uniquement pour libérer un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




