---
description: Récupère la propriété spécifiée d’une liste de révocation de certificats.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: CertStoreProvGetCRLProperty fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877049"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>CertStoreProvGetCRLProperty fonction de rappel

La fonction de rappel **CertStoreProvGetCRLProperty** récupère la propriété spécifiée d’une [*liste de révocation de certificats*](../secgloss/c-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
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

*pCrlContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte de liste de révocation de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .

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

Pointeur vers une mémoire tampon qui contient le pointeur vers une structure de [**\_ contexte de liste de révocation de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) qui doit être retournée par la fonction. Peut avoir la valeur **null** lors d’un premier appel à la fonction pour obtenir la valeur de *pcbData* avant d’allouer de la mémoire pour la mémoire tampon.

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

[**\_contexte CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
