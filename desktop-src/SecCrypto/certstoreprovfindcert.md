---
description: Énumère ou recherche le premier certificat ou certificat suivant dans un magasin externe qui correspond aux critères spécifiés.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: CertStoreProvFindCert fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770018"
---
# <a name="certstoreprovfindcert-callback-function"></a>CertStoreProvFindCert fonction de rappel

La fonction de rappel **CertStoreProvFindCert** énumère ou recherche le premier certificat ou le certificat suivant dans un [*magasin externe*](../secgloss/e-gly.md) qui correspond aux critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hStoreProv* \[ dans\]
</dt> <dd>

Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ dans\]
</dt> <dd>

Pointeur vers un [**magasin de \_ certificats \_ Prov \_ trouve \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) une structure contenant tous les paramètres transmis à la fonction [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .

</dd> <dt>

*pPrevCertContext* \[ dans\]
</dt> <dd>

Pointeur vers un [**\_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificat du certificat trouvé. Lors du premier appel à la fonction, ce paramètre doit avoir la valeur **null**. Lors des appels suivants, il doit être défini sur le pointeur retourné dans le paramètre *ppProvCertContext* du dernier appel. Un pointeur non **null** passé dans ce paramètre est libéré par la fonction de rappel.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Toutes les valeurs d’indicateur nécessaires.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Pointeur vers un pointeur vers une mémoire tampon pour retourner les informations du fournisseur de magasin. Le rappel peut éventuellement retourner un pointeur vers des informations de recherche interne dans ce paramètre. Après le premier appel, ce paramètre est défini sur le pointeur retourné par l’appel précédent à la fonction.

</dd> <dt>

*ppProvCertContext* \[ à\]
</dt> <dd>

En cas de recherche réussie, un pointeur vers le certificat trouvé est retourné dans ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**contexte du certificat \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**\_informations de \_ \_ recherche Prov \_ . du magasin de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
