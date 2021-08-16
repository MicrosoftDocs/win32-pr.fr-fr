---
description: Récupère une propriété spécifiée d’une liste de certificats de confiance (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: CertStoreProvGetCTLProperty fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1677c2cccbdf0b422696437736380bd0bb57542220a898332d72ec7a0562fd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769758"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>CertStoreProvGetCTLProperty fonction de rappel

La fonction de rappel **CertStoreProvGetCTLProperty** récupère une propriété spécifiée d’une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL).

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

*pCtlContext* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

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

Pointeur vers une mémoire tampon destinée à contenir le pointeur vers une structure de [**\_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) devant être retournée par la fonction. Pour obtenir la valeur de *pcbData* avant d’allouer de la mémoire pour la mémoire tampon, ce paramètre peut avoir la valeur **null** lors d’un premier appel à la fonction.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui indique la longueur de la mémoire tampon *pvData* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la fonction retourne une valeur différente de zéro.

Si la fonction échoue, elle retourne zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
