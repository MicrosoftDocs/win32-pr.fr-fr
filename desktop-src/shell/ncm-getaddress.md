---
description: Indique si une adresse réseau est conforme à un type et un format spécifiés.
title: Message NCM_GETADDRESS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296107"
---
# <a name="ncm_getaddress-message"></a>\_Message NCM GETADDRESS

Indique si une adresse réseau est conforme à un type et un format spécifiés.


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*PV* \[ in, out\]
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> pour recevoir des informations d’adresse réseau sous forme analysée, si le format et le type d’adresse dans le contrôle spécifié par *HWND* sont validés. L’application appelante est chargée d’allouer la mémoire pour cette structure.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs suivantes de type **HRESULT**.



| Code de retour                                                                                                | Description                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | L’application appelante n’a pas pu allouer une structure d' [**\_ adresse NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .<br/> |
| <dl> <dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt> </dl> | La mémoire tampon de sortie est trop petite pour contenir l’adresse réseau analysée.<br/>                           |
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>   | La chaîne d’adresse réseau n’est pas de type spécifié.<br/>                                  |
| <dl> <dt>**ERREUR de \_ réussite**</dt> </dl>              | L'opération a réussi.<br/>                                                             |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Il n’y a aucune adresse dans le contrôle d’adresse réseau à valider.<br/>                           |



 

## <a name="remarks"></a>Notes

Utilisez le message **NCM \_ GETADDRESS** pour valider une adresse réseau dans un contrôle d’adresse réseau par rapport à un masque de type d’adresse réseau prédéfini. Pour instancier, utilisez la classe **msctls \_ NetAddress** définie dans shellapi. h. Appelez [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) au moment de l’exécution avant d’envoyer ce message. Cette commande initialise la bibliothèque de contrôles communs qui contient le contrôle d’adresse réseau.

Ce message obtient la chaîne d’adresse réseau à partir d’un contrôle d’adresse réseau, analyse la chaîne et vérifie si la chaîne correspond à un masque de type d’adresse réseau. Si la chaîne correspond au masque, le message retourne \_ la valeur OK et retourne la chaîne sous forme analysée à l’application appelante (y compris le numéro de port, la longueur de préfixe et d’autres informations d’adresse), à l’aide de la structure d' [**\_ adresse NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) pointée par *va*. Ce message renvoie E \_ INVALIDARG si l’application appelante ne parvient pas à allouer la structure désignée par *va*.

Les représentations de l’adresse IP (Internet Protocol) versions 4 et 6 (v4/V6) pour les services et les réseaux, ainsi que les adresses Internet et les services nommés utilisant le format DNS (Domain Name System) sont analysés. Si la chaîne d’adresse réseau représente un nom d’hôte (DNS) ou un service nommé, la valeur retournée dans le membre **PrefixLength** de l' [**\_ adresse NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) est égale à zéro.

Définissez le masque de type d’adresse réseau à l’aide du message [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) avant d’envoyer la macro **NCM \_ GETADDRESS** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**GetAddress NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




