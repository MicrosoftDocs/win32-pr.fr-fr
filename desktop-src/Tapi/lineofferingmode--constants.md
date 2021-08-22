---
description: Les \_ constantes d’indicateur de bit LINEOFFERINGMODE (TAPI versions 1,4 et ultérieures) décrivent différents sous-États d’un appel d’offre.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Constantes LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68c2c36d18d006cdc1e2d9fc79095d58b6f56f1e58f4939c4e08ec6936af6855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518909"
---
# <a name="lineofferingmode_-constants"></a>\_Constantes LINEOFFERINGMODE

Les constantes d’indicateur de bit **LINEOFFERINGMODE \_** (TAPI versions 1,4 et ultérieures) décrivent différents sous-États d’un appel d’offre. Un mode est disponible en tant qu’État d’appel à l’application après l’état d’appel trdansitions à l’offre, et dans le message de [**ligne \_ CALLSTATE**](line-callstate.md) indiquant que l’appel se trouve dans l' \_ offre LINECALLSTATE. Ces valeurs sont utilisées lorsque l’appel est sur une adresse partagée (Bridged) avec d’autres stations (voir [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique.

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ actif**
</dt> <dd> <dl> <dt>



Indique que l’appel est en cours d’alerte au niveau de la station active (est accompagné des \_ messages de sonnerie LINEDEVSTATE) et, si une application est configurée pour répondre automatiquement, elle peut le faire. Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est active (ce qui serait la situation sur une adresse sans pont). (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ inactif**
</dt> <dd> <dl> <dt>



Indique que l’appel est proposé sur plusieurs stations, mais que la station actuelle ne fait pas l’objet d’une alerte (par exemple, il peut s’agir d’une station de surveillance dans laquelle l’état de l’offre est un avis, tel que le clignotement d’une lumière); les logiciels de la station définie pour la réponse automatique doivent de préférence ne pas répondre à l’appel, car il doit s’agir de la prérogative au niveau de la station principale (alerte), mais [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) peut être utilisé pour connecter l’appel. (TAPI versions 1,4 et ultérieures)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Non extensible. Tous les 32 bits sont réservés.

Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser ces \_ valeurs LINEOFFERINGMODE si elles ne sont pas prises en charge sur la version négociée. Les applications qui ne sont pas Cognizant de LINEOFFERINGMODE \_ supposent probablement qu’un appel qui est dans l' \_ offre LINECALLSTATE est dans LINEOFFERINGMODE \_ actif.

Les \_ \_ valeurs inactives LINEOFFERINGMODE actives et LINEOFFERINGMODE sont utilisées lorsque l’appel est sur une adresse partagée avec d’autres stations (Bridged, voir [ \_ constantes LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique. Si le mode d’état d’appel de l’offre est « actif », cela signifie que l’appel est en cours d’alerte au niveau de la station active (est accompagné de \_ messages de sonnerie LINEDEVSTATE), et si une application est configurée pour répondre automatiquement, elle peut le faire. Si le mode d’état de l’appel est « inactif », l’appel est proposé sur plusieurs stations, mais la station actuelle ne fait pas l’objet d’une alerte (par exemple, il peut s’agir d’une station de surveillance dans laquelle l’état de l’offre est un avis, tel que le clignotement d’une lumière); les logiciels de la station définie pour la réponse automatique doivent de préférence ne pas répondre à l’appel, car il doit s’agir de la prérogative au niveau de la station principale (alerte), mais [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) peut être utilisé pour connecter l’appel. Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est active (ce qui serait la situation sur une adresse sans pont).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




