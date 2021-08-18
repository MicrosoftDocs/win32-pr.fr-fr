---
description: Libère un \_ contexte PCCERT acquis par le biais de la propriété CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'ICertContext :: FreeContext, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06809d8950d62f1136b8efc25c8e5b4499e020dce956d65f9e0d4a0e349567de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006187"
---
# <a name="icertcontextfreecontext-method"></a>ICertContext :: FreeContext, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La méthode **FreeContext** libère un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .

## <a name="syntax"></a>Syntaxe


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCertContext* \[ dans\]
</dt> <dd>

Contexte PCCERT \_ à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique la réussite de l’opération. Toute autre valeur indique que l’opération a échoué.

## <a name="remarks"></a>Remarques

Cette méthode ne libère pas le \_ contexte PCCERT contenu dans un objet de [**certificat**](certificate.md) . Elle doit être utilisée uniquement pour libérer un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




