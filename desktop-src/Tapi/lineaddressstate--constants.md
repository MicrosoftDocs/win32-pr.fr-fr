---
description: Les \_ constantes d’indicateur de bit LINEADDRESSSTATE décrivent les différents éléments d’état d’adresse.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Constantes LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535021"
---
# <a name="lineaddressstate_-constants"></a>\_Constantes LINEADDRESSSTATE

Les constantes d’indicateur de bit **LINEADDRESSSTATE \_** décrivent les différents éléments d’état d’adresse.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) pour l’adresse ont changé. L’application doit utiliser [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) pour lire la structure mise à jour. Si un fournisseur de services envoie un message [**\_ ADDRESSSTATE de ligne**](line-addressstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure recevront les messages de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) qui spécifient LINEDEVSTATE \_ Réinit, en leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



L’élément spécifique à l’appareil de l’état de l’adresse a changé.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ vers l’avant**
</dt> <dd> <dl> <dt>



L’état de transfert de l’adresse a changé, y compris éventuellement le nombre d’anneaux pour déterminer une condition de non-réponse. L’application doit vérifier l’état de l’adresse pour déterminer les détails sur l’état de transfert actuel de l’adresse.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



L’adresse surveillée ou de pont est passée de l’utilisation d’une station à l’utilisation par plusieurs stations.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



L’adresse est passée de inactif ou en cours d’utilisation par de nombreuses stations de pont en cours d’utilisation par une seule station.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



L’adresse est passée à inactif (elle n’est pas utilisée par les stations).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



Le nombre d’appels sur l’adresse a changé. Il s’agit du résultat d’événements tels qu’un nouvel appel entrant, d’un appel sortant sur l’adresse ou d’un appel modifiant son état de suspension. Cet indicateur couvre les modifications apportées à l’un des membres **dwNumActiveCalls**, **dwNumOnHoldCalls** et **dwNumOnHoldPendingCalls** dans la structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) . L’application doit vérifier les trois membres lorsqu’elle reçoit un message de [**ligne \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ autre**
</dt> <dd> <dl> <dt>



Les éléments d’état d’adresse autres que ceux listés ci-dessous ont été modifiés. L’application doit vérifier l’état actuel de l’adresse pour déterminer les éléments qui ont été modifiés.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminaux LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



Les paramètres de terminal pour l’adresse ont été modifiés.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

Une application est avertie des modifications apportées à ces éléments d’État dans le message de [**ligne \_ ADDRESSSTATE**](line-addressstate.md) . Les fonctionnalités de l’appareil de l’adresse indiquent les modifications d’état d’adresse qui peuvent être signalées pour cette adresse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ADDRESSSTATE de ligne \_**](line-addressstate.md)
</dt> <dt>

[**LINEDEVSTATE de ligne \_**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




