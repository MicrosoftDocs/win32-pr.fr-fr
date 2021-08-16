---
description: Récupère la propriété spécifiée d’un certificat.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: CertStoreProvGetCertProperty fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c7d338c94c4e9655c125b0f70e3f2e8dfa732316a970c74c26e4a7fbced22671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769924"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>CertStoreProvGetCertProperty fonction de rappel

La fonction de rappel **CertStoreProvGetCertProperty** récupère la propriété spécifiée d’un certificat.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hStoreProv* \[ dans\]
</dt> <dd>

Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

</dd> <dt>

*dwPropId* \[ dans\]
</dt> <dd>

Indique un identificateur de propriété.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Toutes les valeurs d’indicateur nécessaires.

</dd> <dt>

*pvData* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon destinée à contenir le pointeur vers une structure de [**\_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) qui doit être retournée par la fonction. Peut avoir la valeur **null** lors d’un premier appel à la fonction pour obtenir la valeur de *pcbData* avant d’allouer de la mémoire pour la mémoire tampon.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Pointeur vers une **valeur DWORD** indiquant la longueur de la mémoire tampon *pvData* .

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
</dt> </dl>

 

 
