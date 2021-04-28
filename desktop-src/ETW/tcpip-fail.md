---
description: 'Classe TcpIp_Fail : cette classe est la classe de type d’événement pour les événements de défaillance TCP/IP. La syntaxe suivante est simplifiée à partir du code MOF.'
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: Classe TcpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105847"
---
# <a name="tcpip_fail-class"></a>TcpIp ( \_ classe d’échec)

Cette classe est la classe de type d’événement pour les événements de défaillance TCP/IP.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Membres

La classe d' **\_ échec TcpIp** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe d' **\_ échec TcpIp** possède ces propriétés.

<dl> <dt>

**FailureCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Motif de l’échec. Il peut s’agir de l’un des codes suivants :

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Erreur \_ \_Ressources INsuffisantes** (1)
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Erreur \_ TROP \_ d' \_ adresses** (2)
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Erreur \_ L’adresse \_ existe** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Erreur \_ \_Adresse non valide** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**Erreur \_ AUTRE** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Erreur \_ L' \_ adresse TIMEWAIT \_ existe** (6)
</dt> </dl>

</dd> <dt>

**Proto**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie le protocole. Peut avoir l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                                  | Signification                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>     | Famille d’adresses IPv4 (Internet Protocol version 4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl> | Famille d’adresses IPv6 (Internet Protocol version 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Msafd**](tcpip.md)
</dt> </dl>

 

 




