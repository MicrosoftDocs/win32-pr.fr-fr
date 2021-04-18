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
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540519"
---
# <a name="icertcontextcertcontext-property"></a>ICertContext :: CertContext, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

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

## <a name="remarks"></a>Notes

Vous devez appeler la méthode [**FreeContext**](icertcontext-freecontext.md) ou la fonction [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) pour libérer le contexte.

Si vous définissez la propriété **CertContext** , l’état de l’intégralité de l’objet de [**certificat**](certificate.md) est réinitialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




