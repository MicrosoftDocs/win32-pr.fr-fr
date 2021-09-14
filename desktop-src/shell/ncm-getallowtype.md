---
description: Récupère les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.
title: Message NCM_GETALLOWTYPE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296106"
---
# <a name="ncm_getallowtype-message"></a>\_Message NCM GETALLOWTYPE

Récupère les types d’adresses réseau que le contrôle d’adresse réseau spécifié accepte.


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne les types d’adresses réseau autorisés comme une ou plusieurs des constantes de [**\_ chaîne net**](net-string.md) .

## <a name="remarks"></a>Notes

Le masque retourné est le critère utilisé pour valider une adresse réseau dans le message [**NCM \_ GETADDRESS**](ncm-getaddress.md) .

Utilisez ce message pour un contrôle d’adresse réseau uniquement. Pour instancier, utilisez la classe **msctls \_ NetAddress** définie dans shellapi. h. Appelez [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) au moment de l’exécution avant d’envoyer ce message. Cette commande initialise la bibliothèque de contrôles communs qui contient le contrôle d’adresse réseau.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md)
</dt> <dt>

[**GetAllowType NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




