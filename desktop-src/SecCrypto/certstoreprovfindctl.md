---
description: Énumère ou recherche la liste CTL First ou Next dans un magasin externe qui correspond aux critères spécifiés.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: CertStoreProvFindCTL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530669"
---
# <a name="certstoreprovfindctl-callback-function"></a>CertStoreProvFindCTL fonction de rappel

La fonction de rappel **CertStoreProvFindCTL** énumère ou recherche la [*liste CTL*](../secgloss/c-gly.md) First ou Next dans un [*magasin externe*](../secgloss/e-gly.md) qui correspond aux critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
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

Pointeur vers un [**magasin de \_ certificats \_ Prov \_ trouve \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la structure des informations contenant tous les paramètres transmis à [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore). CHANGETABLE(CHANGES ...).

</dd> <dt>

*pPrevCtlContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la dernière liste de certificats de confiance trouvée. Lors du premier appel à la fonction, ce paramètre doit avoir la valeur **null**. Lors des appels suivants, il doit être défini sur le pointeur retourné dans le paramètre *ppProvCTLContext* du dernier appel. Un pointeur non **null** passé dans ce paramètre est libéré par la fonction de rappel.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Toutes les valeurs d’indicateur nécessaires.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Pointeur vers un pointeur vers la mémoire tampon pour retourner les informations du fournisseur de magasin. Le rappel peut éventuellement retourner un pointeur vers des informations de recherche interne dans ce paramètre. Après le premier appel, ce paramètre est défini sur le pointeur retourné par l’appel précédent à la fonction.

</dd> <dt>

*ppProvCtlContext* \[ à\]
</dt> <dd>

En cas de recherche réussie, un pointeur vers la liste CTL trouvée est retourné dans ce paramètre.

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

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**\_contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
