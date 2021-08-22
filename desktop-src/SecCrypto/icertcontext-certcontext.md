---
description: Définit ou récupère le contexte PCCERT \_ d’un certificat.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'ICertContext :: CertContext, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5c517384bdffd8723c1e9e0d96683cc4bd4918361acdf19df77286bfbac962b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006367"
---
# <a name="icertcontextcertcontext-property"></a>ICertContext :: CertContext, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La propriété **CertContext** définit ou récupère le contexte PCCERT \_ d’un certificat.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Valeur de la propriété

Contexte PCCERT \_ du certificat.

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes d’accès aux propriétés **placent \_ CertContext** et **obtiennent \_ CertContext** , elles retournent la réponse \_ OK.

Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Remarques

Vous devez appeler la méthode [**FreeContext**](icertcontext-freecontext.md) ou la fonction [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) pour libérer le contexte.

Si vous définissez la propriété **CertContext** , l’état de l’intégralité de l’objet de [**certificat**](certificate.md) est réinitialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




