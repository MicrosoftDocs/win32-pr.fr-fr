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
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533633"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**contexte du certificat \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
