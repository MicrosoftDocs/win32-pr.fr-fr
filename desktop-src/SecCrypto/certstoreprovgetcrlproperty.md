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
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542931"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_contexte CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
