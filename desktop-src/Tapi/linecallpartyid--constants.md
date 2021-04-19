---
description: Les \_ constantes d’indicateur de bit LINECALLPARTYID décrivent la nature des informations disponibles sur les parties impliquées dans un appel.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Constantes LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525642"
---
# <a name="linecallpartyid_-constants"></a>\_Constantes LINECALLPARTYID

Les constantes d’indicateur de bit **LINECALLPARTYID \_** décrivent la nature des informations disponibles sur les parties impliquées dans un appel.

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**\_adresse LINECALLPARTYID**
</dt> <dd> <dl> <dt>



Les informations relatives aux identificateurs de tiers se composent de l’adresse du tiers dans un format d’adresse canonique ou un format d’adresse de numérotation.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloqué**
</dt> <dd> <dl> <dt>



Les informations de l’identificateur de tiers ne sont pas disponibles, car elles ont été bloquées par le tiers distant.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**nom de LINECALLPARTYID \_**
</dt> <dd> <dl> <dt>



Les informations de l’identificateur de tiers se composent du nom du tiers (par exemple, à partir d’un répertoire conservé à l’intérieur du commutateur).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**
</dt> <dd> <dl> <dt>



Les informations d’ID de l’appelant pour l’appel ne sont pas disponibles, car elles ne sont pas propagées de façon inversée par le réseau.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ partiel**
</dt> <dd> <dl> <dt>



Les informations de l’identificateur de tiers sont valides, mais elles ne sont limitées qu’à des informations partielles.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID \_ INdispo**
</dt> <dd> <dl> <dt>



Les informations de l’identificateur de tiers ne sont pas disponibles et ne seront plus disponibles ultérieurement. Les informations peuvent ne pas être disponibles pour des raisons non spécifiées. Par exemple, les informations n’ont pas été remises par le réseau, elles ont été ignorées par le fournisseur de services, et ainsi de suite.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ inconnu**
</dt> <dd> <dl> <dt>



Les informations de l’identificateur de tiers sont actuellement inconnues, mais peuvent devenir connues ultérieurement.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Pour chaque partie possible impliquée dans un appel, les constantes **LINECALLPARTYID \_** décrivent comment les informations de l’identificateur de tiers sont mises en forme. Ces informations sont fournies dans la structure de données [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




