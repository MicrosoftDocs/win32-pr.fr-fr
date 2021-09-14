---
description: Définit ou récupère l’emplacement du magasin CAPICOM \_ \_ d’un magasin de certificats.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'ICertStore :: StoreLocation, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237593"
---
# <a name="icertstorestorelocation-property"></a>ICertStore :: StoreLocation, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La propriété **StoreLocation** définit ou récupère l' [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) d’un magasin de certificats.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>Valeur de la propriété

Emplacement du magasin de certificats

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes d’accès aux propriétés **placent \_ StoreLocation** et **obtiennent \_ StoreLocation** , elles retournent la réponse \_ OK.

Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




