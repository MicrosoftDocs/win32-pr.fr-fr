---
description: Les \_ constantes d’indicateur de bit PHONESTATE décrivent les différents éléments d’état d’un appareil téléphonique.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Constantes PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526017"
---
# <a name="phonestate_-constants"></a>\_Constantes PHONESTATE

Les constantes d’indicateur de bit **PHONESTATE \_** décrivent les différents éléments d’état d’un appareil téléphonique.

<dl> <dt>

<span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) ont changé. L’application doit utiliser [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) pour lire la structure mise à jour. Si un fournisseur de services envoie un message d' [**\_ État de téléphone**](phone-state.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API précédente recevront des messages d’état de téléphone qui \_ spécifient la réinitialisation PHONESTATE, en \_ leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ connecté**
</dt> <dd> <dl> <dt>



La connexion entre l’appareil téléphonique et l’interface TAPI vient d’être établie. Cela se produit lorsque l’interface TAPI est appelée pour la première fois ou lorsque le câble qui connecte le téléphone au PC est branché avec l’interface TAPI active.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Les informations spécifiques à l’appareil du téléphone ont été modifiées.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ déconnecté**
</dt> <dd> <dl> <dt>



La connexion entre l’appareil téléphonique et l’interface TAPI vient d’être rompue. Cela se produit lorsque le câble connectant le téléphone à l’ordinateur est débranché alors que TAPI est actif.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**\_affichage PHONESTATE**
</dt> <dd> <dl> <dt>



L’affichage du téléphone a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**
</dt> <dd> <dl> <dt>



Le paramètre d’augmentation du microphone du combiné a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



L’état de l’hookswitch de téléphone a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**
</dt> <dd> <dl> <dt>



Le paramètre du volume de haut-parleur du téléphone a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**
</dt> <dd> <dl> <dt>



L’état de hookswitch du casque a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**
</dt> <dd> <dl> <dt>



Le paramètre d’augmentation du microphone du casque a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**
</dt> <dd> <dl> <dt>



Le paramètre du volume de haut-parleur du casque a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_lampe PHONESTATE**
</dt> <dd> <dl> <dt>



Une lampe du téléphone a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_analyses PHONESTATE**
</dt> <dd> <dl> <dt>



Nombre d’analyses pour l’appareil téléphonique.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ autre**
</dt> <dd> <dl> <dt>



Les éléments de l’état du téléphone autres que ceux listés ci-dessous ont été modifiés. L’application doit vérifier l’état actuel du téléphone pour déterminer les éléments qui ont été modifiés.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**\_propriétaire PHONESTATE**
</dt> <dd> <dl> <dt>



Nombre de propriétaires de l’appareil mobile.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**Réinit PHONESTATE \_**
</dt> <dd> <dl> <dt>



Les éléments ont été modifiés dans la configuration des appareils téléphoniques. Pour être conscient de ces modifications (comme l’apparence des nouveaux appareils téléphoniques), l’application doit réinitialiser son utilisation de l’interface TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ supprimé**
</dt> <dd> <dl> <dt>



Indique que l’appareil est en cours de suppression du système par le fournisseur de services (probablement via une action de l’utilisateur, via un panneau de configuration ou un utilitaire similaire). Un message d' [**\_ État de téléphone**](phone-state.md) avec cette valeur est normalement immédiatement suivi d’un message de [**\_ fermeture de téléphone**](phone-close.md) sur l’appareil. Les tentatives suivantes d’accès à l’appareil avant la réinitialisation de l’interface TAPI entraînent \_ le retour de PHONEERR nodevice à l’application. Si un fournisseur de services envoie un \_ message d’état de téléphone contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure ne reçoivent aucune notification.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE \_ Resume**
</dt> <dd> <dl> <dt>



L’utilisation de l’appareil téléphonique par l’application reprend après avoir été interrompue pendant un certain temps.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**
</dt> <dd> <dl> <dt>



Le mode Ring du téléphone a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**
</dt> <dd> <dl> <dt>



Le volume de la sonnerie du téléphone a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**
</dt> <dd> <dl> <dt>



L’état de hookswitch du haut-parleur a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**
</dt> <dd> <dl> <dt>



L’état du paramètre de gain du microphone du haut-parleur a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**
</dt> <dd> <dl> <dt>



Le paramètre du volume de haut-parleur de haut-parleur a changé.


</dt> </dl> </dd> <dt>

<span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE \_ suspendre**
</dt> <dd> <dl> <dt>



L’utilisation du téléphone par l’application est temporairement suspendue.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Fermer le téléphone**](phone-close.md)
</dt> <dt>

[**État du téléphone \_**](phone-state.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




