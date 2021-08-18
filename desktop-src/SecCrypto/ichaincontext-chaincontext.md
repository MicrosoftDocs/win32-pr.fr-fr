---
description: Définit ou récupère le \_ \_ contexte de chaîne PCCERT d’un certificat.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'IChainContext :: ChainContext, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d5e7bc92aa798766538af19cae440542705a859040aed7fc8d9510e3724051f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005497"
---
# <a name="ichaincontextchaincontext-property"></a>IChainContext :: ChainContext, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La propriété **chainContext** définit ou récupère le \_ \_ contexte de chaîne PCCERT d’un certificat.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Valeur de la propriété

\_Contexte de la chaîne PCCERT \_ du certificat.

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes d’accès aux propriétés **placent \_ chainContext** et **obtiennent \_ chainContext** , elles retournent la réponse \_ OK.

Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Remarques

Vous devez appeler la méthode [**FreeContext**](ichaincontext-freecontext.md) ou la fonction [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) pour libérer le contexte.

Si vous définissez la propriété **chainContext** , l’état de la totalité de l’objet [**chaîne**](chain.md) est réinitialisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




