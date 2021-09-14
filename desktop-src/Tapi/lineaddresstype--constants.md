---
description: Le type d’adresse identifie le format d’adresse, par exemple le numéro de téléphone standard ou l’adresse de messagerie. Seules les applications qui négocient TAPI version 3,0 ou ultérieure peuvent utiliser des types d’adresse.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Constantes LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217545"
---
# <a name="lineaddresstype_-constants"></a>\_Constantes LINEADDRESSTYPE

Le type d’adresse identifie le format d’adresse, par exemple le numéro de téléphone standard ou l’adresse de messagerie. Seules les applications qui négocient TAPI version 3,0 ou ultérieure peuvent utiliser des types d’adresse.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Le type d’adresse est un numéro de téléphone standard.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**\_SDP LINEADDRESSTYPE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Le type d’adresse est Conférence SDP (session Description Protocol).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Le type d’adresse est un nom de messagerie électronique.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ nomdomaine**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Le type d’adresse est un nom de domaine.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**\_adresse IP LINEADDRESSTYPE**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Le type d’adresse est une adresse IP.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




