---
description: Énumère ou recherche la première liste de révocation de certificats ou la prochaine dans un magasin externe qui correspond aux critères spécifiés.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: CertStoreProvFindCRL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529710"
---
# <a name="certstoreprovfindcrl-callback-function"></a>CertStoreProvFindCRL fonction de rappel

La fonction de rappel **CertStoreProvFindCRL** énumère ou recherche la première ou la nouvelle [*liste de révocation de certificats*](../secgloss/c-gly.md) dans un [*magasin*](../secgloss/e-gly.md) externe qui correspond aux critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
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

Pointeur vers un [**magasin de \_ certificats \_ Prov \_ trouve \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) une structure contenant tous les paramètres transmis à la fonction [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .

</dd> <dt>

*pPrevCrlContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte de liste de révocation**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) de certificats de la dernière liste de révocation de certificats trouvée. Lors du premier appel à la fonction, ce paramètre doit avoir la valeur **null**. Lors des appels suivants, il doit être défini sur le pointeur retourné dans le paramètre *ppProvCRLContext* du dernier appel. Un pointeur non **null** passé dans ce paramètre est libéré par la fonction de rappel.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Toutes les valeurs d’indicateur nécessaires.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Pointeur vers un pointeur vers une mémoire tampon pour retourner les informations du fournisseur de magasin. Le rappel peut éventuellement retourner un pointeur vers des informations de recherche interne dans ce paramètre. Après le premier appel, ce paramètre est défini sur le pointeur retourné par l’appel précédent à la fonction.

</dd> <dt>

*ppProvCrlContext* \[ à\]
</dt> <dd>

En cas de recherche réussie, un pointeur vers la liste de révocation de certificats trouvée est retourné dans ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations de \_ \_ recherche Prov \_ . du magasin de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**\_contexte CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
