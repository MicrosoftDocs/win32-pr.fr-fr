---
description: Représente les types d’adresses réseau. Utilisez une ou plusieurs (combinaison d’opérations de bits) des constantes suivantes pour créer un masque d’adresse réseau à utiliser avec la macro NETADDR \_ SetAllowType.
title: NET_STRING (iphlpapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991109"
---
# <a name="net_string"></a>\_chaîne net

Représente les types d’adresses réseau. Utilisez une ou plusieurs (combinaison d’opérations de bits) des constantes suivantes pour créer un masque d’adresse réseau à utiliser avec la macro [**NETADDR \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Constante                                                                                                                                                                                                                   | Description                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**\_ \_ Adresse IPv4 de chaîne réseau \_**</dt> </dl>                              | La chaîne identifie un hôte/routeur IPv4 à l’aide d’une adresse littérale (port ou préfixe non autorisé).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**\_ \_ Service IPv4 de chaîne .NET \_**</dt> </dl>                              | La chaîne identifie un service IPv4 à l’aide d’une adresse littérale (port requis ; le préfixe n’est pas autorisé).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**\_ \_ Réseau IPv4 de chaîne NET \_**</dt> </dl>                              | La chaîne identifie un réseau IPv4 (préfixe requis ; port non autorisé).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**\_ \_ Adresse IPv6 de chaîne NET \_**</dt> </dl>                              | La chaîne identifie un hôte/routeur IPv6 à l’aide d’une adresse littérale (le port ou le préfixe n’est pas autorisé ; ID d’étendue autorisé).<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**L' \_ étendue de l' \_ \_ adresse IPv6 \_ \_ de la chaîne net**</dt> </dl> | La chaîne identifie un hôte/routeur IPv6 utilisant une adresse littérale où le contexte de l’interface est déjà connu (port ou préfixe non autorisé ; ID d’étendue non autorisé).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**\_ \_ Service IPv6 de chaîne NET \_**</dt> </dl>                              | La chaîne identifie un service IPv6 à l’aide d’une adresse littérale (port requis ; le préfixe n’est pas autorisé ; ID d’étendue autorisé).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**\_Service IPv6 de chaîne NET \_ \_ \_ sans \_ étendue**</dt> </dl> | La chaîne identifie un service IPv6 à l’aide d’une adresse littérale où le contexte de l’interface est déjà connu (port requis ; prefix non autorisé ; Scope-ID non autorisé).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**\_ \_ Réseau IPv6 de chaîne NET \_**</dt> </dl>                              | La chaîne identifie un réseau IPv6 (préfixe requis ; port ou étendue-ID non autorisé).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**\_chaîne réseau \_ nommée \_ Address**</dt> </dl>                           | La chaîne identifie un hôte Internet utilisant le DNS (le port ou le préfixe ou l’ID d’étendue n’est pas autorisé).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**\_chaîne réseau \_ nommée \_ service**</dt> </dl>                           | La chaîne identifie un service Internet utilisant DNS (port requis ; le préfixe ou l’ID d’étendue n’est pas autorisé).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**\_ \_ adresse IP de la chaîne NET \_**</dt> </dl>                                    | Adresse IPv6 de la chaîne .net de l' \_ \_ \_ adresse IPv4 \| \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**l' \_ étendue de l' \_ \_ adresse IP \_ \_ de la chaîne net**</dt> </dl>       | L’adresse IPv6 de la chaîne net de l’adresse IPv6 de la chaîne NET \_ \_ n’est pas une \_ \| \_ \_ \_ \_ \_ étendue. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**\_ \_ service IP de chaîne .NET \_**</dt> </dl>                                    | Le \_ service IPv6 de chaîne net de \_ service IPv4 de chaîne NET \_ \| \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**\_service IP de chaîne .NET \_ \_ \_ sans \_ étendue**</dt> </dl>       | \_chaîne réseau \_ nommée \_ address \| NET \_ String \_ \_ adresse IP \_ no \_ Scope.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**\_ \_ réseau IP de chaînes \_ réseau**</dt> </dl>                                    | \_Réseau IPv6 de chaîne \_ réseau IPv4 \_ réseau IPv4 \| \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**\_chaîne NET \_ n’importe quelle \_ adresse**</dt> </dl>                                 | \_chaîne réseau \_ nommée \_ address \| NET \_ String \_ \_ adresse IP.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**\_chaîne NET \_ any n' \_ adresse \_ aucune \_ étendue**</dt> </dl>    | \_chaîne réseau \_ nommée \_ address \| NET \_ String \_ \_ adresse IP \_ no \_ Scope.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**\_chaîne NET \_ Any \_ service**</dt> </dl>                                 | \_chaîne .NET \_ nommée \_ service \| NET \_ String \_ IP \_ service.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**\_chaîne NET \_ Any \_ service \_ sans \_ étendue**</dt> </dl>    | \_chaîne réseau \_ nommée \_ address \| NET \_ String \_ \_ adresse IP \_ no \_ Scope.<br/>                                                                                                 |



## <a name="remarks"></a>Notes

Ces valeurs sont définies dans iphlpapi. h.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Iphlpapi. h</dt> </dl> |



 

 




