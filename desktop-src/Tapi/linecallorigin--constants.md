---
description: Les \_ constantes LINECALLORIGIN décrivent l’origine d’un appel.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Constantes LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 296bcc27f3f238e20608279a14ab00c0ab04060faef458fade3f222c7fa35fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944910"
---
# <a name="linecallorigin_-constants"></a>\_Constantes LINECALLORIGIN

Les constantes **LINECALLORIGIN \_** décrivent l’origine d’un appel.

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_Conférence LINECALLORIGIN**
</dt> <dd> <dl> <dt>



Le descripteur d’appel est destiné à un appel de conférence, autrement dit, il s’agit de la connexion de l’application au pont de conférence dans le commutateur.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ externe**
</dt> <dd> <dl> <dt>



L’appel est issu d’un appel entrant sur une ligne externe.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN \_ entrant**
</dt> <dd> <dl> <dt>



L’appel est issu d’un appel entrant, mais le fournisseur de services ne peut pas déterminer s’il provient d’une autre station sur le même commutateur ou à partir d’une ligne externe. Les fournisseurs de services peuvent utiliser cette constante uniquement lorsque TAPI version 1,4 ou ultérieure a été négocié. Dans le cas contraire, le fournisseur de services peut substituer LINECALLORIGIN \_ .


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interne**
</dt> <dd> <dl> <dt>



L’appel est issu d’un appel entrant au niveau d’une station interne au même environnement de basculement.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN \_ sortant**
</dt> <dd> <dl> <dt>



L’appel provient de cette station en tant qu’appel sortant.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN \_ INdispo**
</dt> <dd> <dl> <dt>



L’origine de l’appel n’est pas disponible et ne sera jamais connue pour cet appel.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ inconnu**
</dt> <dd> <dl> <dt>



L’origine de l’appel est actuellement inconnue, mais peut devenir connue ultérieurement.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

L’origine d’un appel est stockée dans le membre **dwOrigin** de la structure [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) de l’appel.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




