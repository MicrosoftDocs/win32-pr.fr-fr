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
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528262"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
