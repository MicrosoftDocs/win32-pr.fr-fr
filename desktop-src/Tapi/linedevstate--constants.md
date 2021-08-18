---
description: Les \_ constantes d’indicateur de bit LINEDEVSTATE décrivent différents événements d’état de ligne.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Constantes LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb11959614999ff50e421e0b77c63d1215a831040774e3123b43aa3534a3f853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140062"
---
# <a name="linedevstate_-constants"></a>\_Constantes LINEDEVSTATE

Les constantes d’indicateur de bit **LINEDEVSTATE \_** décrivent différents événements d’état de ligne.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_batterie LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Le niveau de batterie a changé de manière significative (cellulaire).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) pour l’adresse ont changé. L’application doit utiliser [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) pour lire la structure mise à jour. Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à l’interface TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version TAPI précédente reçoivent des messages de **ligne \_ LINEDEVSTATE** qui spécifient LINEDEVSTATE \_ Réinit, en leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ Fermer**
</dt> <dd> <dl> <dt>



La ligne a été fermée par une autre application.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Indique que des modifications de configuration ont été apportées à un ou plusieurs périphériques multimédias associés à l’appareil de ligne. L’application, si elle le souhaite, peut utiliser [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) pour lire les informations mises à jour. Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Indique que l’achèvement de l’appel identifié par l’identificateur d’achèvement contenu dans le paramètre *dwParam2* de la [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) message a été annulé de manière externe et n’est plus considéré comme valide (si cette valeur devait être passée dans un appel ultérieur à [**LINEUNCOMPLETECALL**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la fonction échoue avec LINEERR \_ INVALCOMPLETIONID). Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ connecté**
</dt> <dd> <dl> <dt>



La ligne a été déconnectée précédemment et est maintenant connectée à TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Les informations spécifiques à l’appareil de la ligne ont été modifiées.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ déconnecté**
</dt> <dd> <dl> <dt>



Cette ligne a déjà été connectée et est maintenant déconnectée de TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**InService LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



La ligne est connectée à l’interface TAPI. Cela se produit lorsque TAPI est activé pour la première fois ou lorsque le câble de ligne est physiquement branché et en service au commutateur alors que TAPI est actif.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_verrou LINEDEVSTATE**
</dt> <dd> <dl> <dt>



L’état verrouillé de l’appareil de ligne a changé. (Pour plus d’informations, consultez LINEDEVSTATUSFLAGS \_ VERROUILLÉ dans [**les \_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_maintenance LINEDEVSTATE**
</dt> <dd> <dl> <dt>



La maintenance est effectuée sur la ligne au niveau du commutateur. TAPI ne peut pas être utilisé pour fonctionner sur le périphérique de ligne.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



L’indicateur de message en attente est désactivé.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



L’indicateur de message en attente est activé.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



Le nombre d’appels sur le périphérique de ligne a changé.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



Le nombre de saisies semi-automatiques d’appels en attente sur le périphérique de ligne a changé.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ ouvrir**
</dt> <dd> <dl> <dt>



La ligne a été ouverte par une autre application.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ autre**
</dt> <dd> <dl> <dt>



Les éléments d’état de l’appareil autres que ceux listés ci-dessous ont été modifiés. L’application doit vérifier l’état actuel de l’appareil pour déterminer les éléments qui ont été modifiés.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



La ligne est hors service au niveau du commutateur ou physiquement déconnectée. TAPI ne peut pas être utilisé pour fonctionner sur le périphérique de ligne.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**Réinit LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



Les éléments ont été modifiés dans la configuration des appareils en ligne. Pour être conscient de ces modifications (comme l’apparence des nouveaux appareils de ligne), l’application doit réinitialiser son utilisation de l’interface TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ supprimé**
</dt> <dd> <dl> <dt>



Indique que l’appareil est en cours de suppression du système par le fournisseur de services (probablement via une action de l’utilisateur, via un panneau de configuration ou un utilitaire similaire). Un [**message \_ LINEDEVSTATE de ligne**](line-linedevstate.md) avec cette valeur est normalement immédiatement suivi d’un message de [**\_ fermeture de ligne**](line-close.md) sur l’appareil. Les tentatives suivantes d’accès à l’appareil avant la réinitialisation de l’interface TAPI entraînent \_ le retour de LINEERR nodevice à l’application. Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_sonnerie LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Le commutateur indique à la ligne d’alerter l’utilisateur.

**TAPI :** Les fournisseurs de services notifient les applications sur chaque cycle de sonnerie en envoyant de manière répétée des messages [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette constante. Par exemple, dans le États-Unis, les fournisseurs de services envoient un message avec cette constante toutes les six secondes.

**TSPI :** Sur un appareil POTS, le fournisseur de services peut envoyer le message chaque fois que le Bureau central envoie la tension de la sonnerie. Sur les appareils numériques tels que RNIS, le fournisseur de services peut être amené à synthétiser la répétition du message si le commutateur ne génère qu’une seule demande de sonnerie. Chaque répétition du message doit indiquer le nombre de sonneries, afin que les fonctions Toll Save fonctionnent correctement.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



Le mode itinérant du périphérique de ligne a changé.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_signal LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Le niveau de signal a changé de manière significative (cellulaire).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminaux LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Les paramètres du terminal ont été modifiés. Cela peut se produire, par exemple, si plusieurs périphériques de ligne partagent des terminaux entre eux (par exemple, deux lignes partageant un terminal de téléphone).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) ont changé. L’application doit utiliser [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) pour lire la structure mise à jour. Si un fournisseur de services envoie un message [**\_ LINEDEVSTATE de ligne**](line-linedevstate.md) contenant cette valeur à l’interface TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version TAPI précédente reçoivent des messages de **ligne \_ LINEDEVSTATE** qui spécifient LINEDEVSTATE \_ Réinit, en leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**fermeture de ligne \_**](line-close.md)
</dt> <dt>

[**LINEDEVSTATE de ligne \_**](line-linedevstate.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




