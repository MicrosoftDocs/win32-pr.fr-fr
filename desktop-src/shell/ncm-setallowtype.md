---
description: Définit les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.
title: Message NCM_SETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d3fc6b8ceb848d4738ff2d77b4441a29354bf09248e0de88008072dbf867e8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719923"
---
# <a name="ncm_setallowtype-message"></a>\_Message NCM SETALLOWTYPE

Définit les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*addrMask* \[ dans\]
</dt> <dd>Spécifie les types d’adresses réseau sous la forme d’une ou de plusieurs constantes de <a href="net-string.md">**\_ chaîne net**</a> .</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

L’ensemble de masques est le critère utilisé pour valider une adresse réseau dans le message [**NCM \_ GETADDRESS**](ncm-getaddress.md) .

Utilisez ce message pour un contrôle d’adresse réseau uniquement. Pour instancier, utilisez la classe **msctls \_ NetAddress** définie dans shellapi. h. Appelez [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) au moment de l’exécution avant d’envoyer ce message. Cette commande initialise la bibliothèque de contrôles communs qui contient le contrôle d’adresse réseau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**SetAllowType NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




