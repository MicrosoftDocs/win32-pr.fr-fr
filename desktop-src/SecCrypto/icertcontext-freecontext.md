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
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120949"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique la réussite de l’opération. Toute autre valeur indique que l’opération a échoué.

## <a name="remarks"></a>Notes

Cette méthode ne libère pas le \_ contexte PCCERT contenu dans un objet de [**certificat**](certificate.md) . Elle doit être utilisée uniquement pour libérer un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




