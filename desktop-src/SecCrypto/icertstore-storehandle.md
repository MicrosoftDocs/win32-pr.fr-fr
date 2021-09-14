---
description: Définit ou récupère le handle HCERTSTORE d’un magasin de certificats.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'ICertStore :: StoreHandle, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237599"
---
# <a name="icertstorestorehandle-property"></a>ICertStore :: StoreHandle, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La propriété **StoreHandle** définit ou récupère le handle HCERTSTORE d’un magasin de certificats.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Valeur de la propriété

Handle HCERTSTORE du magasin de certificats.

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes d’accès aux propriétés **placent \_ StoreHandle** et **obtiennent \_ StoreHandle** , elles retournent la réponse \_ OK.

Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Notes

Vous devez appeler la méthode [**CloseHandle**](icertstore-closehandle.md) ou la fonction [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) pour libérer le contexte.

Si vous définissez la propriété **StoreHandle** , l’état de la totalité de l’objet de [**magasin**](store.md) est réinitialisé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




