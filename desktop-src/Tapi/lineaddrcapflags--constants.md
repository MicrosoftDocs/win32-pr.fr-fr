---
description: Les \_ constantes d’indicateur de bit LINEADDRCAPFLAGS sont utilisées dans le membre dwAddrCapFlags de la structure de données LINEADDRESSCAPS pour décrire différentes fonctions d’adresse booléennes.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Constantes LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217593"
---
# <a name="lineaddrcapflags_-constants"></a>\_Constantes LINEADDRCAPFLAGS

Les  \_ constantes d’indicateur de bit LINEADDRCAPFLAGS sont utilisées dans le membre **dwAddrCapFlags** de la structure de données [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) pour décrire différentes fonctions d’adresse booléennes.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**True** si un appel d’offre doit être accepté à l’aide de [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) pour commencer à alerter les utilisateurs aux deux extrémités de l’appel ; Sinon, **false**. Cela est généralement utilisé uniquement avec RNIS.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



L’adresse prend en charge les [groupes ACD](about-call-center-controls.md#acd-group-object) en relation avec les opérations du centre d’appels. Pour plus d’informations sur les groupes de ACD, consultez [à propos des contrôles du centre d’appels](./about-call-center-controls.md) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ reconnexion automatique**
</dt> <dd> <dl> <dt>



Spécifie si la suppression d’un appel de consultation se reconnecte automatiquement à l’appel sur la suspension de la consultation. **True** si la reconnexion se produit automatiquement ; Sinon, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



Spécifie si le réseau envoie ou bloque par défaut les informations relatives à l’ID de l’appelant lors d’un appel sur cette adresse. Si la **valeur est true**, les informations d’identificateur sont bloquées par défaut ; Si la **valeur est false**, les informations d’identificateur sont transmises par défaut.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



Spécifie si le paramètre par défaut pour l’envoi ou le blocage des informations d’ID de l’appelant peut être substitué par appel. Si la **valeur est true**, le remplacement est possible ; Si la **valeur est false**, le remplacement n’est pas possible.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS \_ COMPLETIONID**
</dt> <dd> <dl> <dt>



Spécifie si les identificateurs de saisie semi-automatique retournés par [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) sont utiles et uniques. **True** si utile ; Sinon, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



**True** si [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) sur un appel de conférence parent a également pour effet secondaire de supprimer (c’est-à-dire déconnecter) les autres parties impliquées dans l’appel de la Conférence ; **False** si la suppression d’un appel de conférence autorise toujours les autres parties à communiquer entre elles.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**
</dt> <dd> <dl> <dt>



Spécifie si un appel bloqué peut être mis en conférence. Souvent, seuls les appels au blocage de la consultation peuvent être ajoutés à en tant qu’appel de conférence.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



Spécifie si un appel entièrement nouveau peut être établi pour une utilisation en tant qu’appel de consultation (à ajouter) lors d’une conférence.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



Spécifie si le téléphone de la partie appelée peut être automatiquement forcé offhook lors des appels.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ composé**
</dt> <dd> <dl> <dt>



Spécifie si une adresse de destination peut être numérotée sur cette adresse pour effectuer un appel. **True** si une adresse de destination doit être composée ; **False** si l’adresse de destination est fixe (comme avec un « téléphone à chaud »).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



Spécifie si le transfert d’appels pour Busy et pour aucune réponse peut utiliser des adresses de transfert différentes. Cet indicateur n’a de sens que si le transfert pour la disponibilité et l’absence de réponse peut être contrôlé séparément. Cet indicateur a la **valeur true** si le transfert pour Busy et pour aucune réponse peut utiliser des adresses de destination différentes ; Sinon, la **valeur est false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



Spécifie si le transfert d’appels implique l’établissement d’un appel de consultation.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



Spécifie si les appels internes et externes peuvent être transférés vers différentes adresses de transfert. Cet indicateur est significatif uniquement si le transfert d’appels internes et externes peut être contrôlé séparément. Cet indicateur a la **valeur true** si les appels internes et externes peuvent être transférés vers des adresses de destination différentes ; Sinon, la **valeur est false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



Spécifie si le nombre d’anneaux pour une réponse de non-réponse peut être spécifié lors du transfert d’appels en l’absence de réponse. Si la **valeur est true**, la plage valide est fournie dans les membres **dwMinFwdNumRings** et **dwMaxFwdNumRings** de la structure [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



Spécifie si l’état de transfert dans la structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) pour cette adresse est valide ou s’il s’agit d’une « meilleure estimation », en raison de l’absence de confirmation exacte par le commutateur ou le réseau.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



Lorsqu’un appel sur cette adresse est placé en attente (à l’aide de LineHold ou d’une action externe), un nouvel appel est automatiquement créé (probablement dans la [**di**](/windows/desktop/api/Tapi/nf-tapi-linehold) LINECALLSTATE \_ ).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



L’adresse est associée à une ligne interne sur un PBX qui est limitée de telle façon qu’elle ne peut pas être utilisée pour passer des appels à une adresse en dehors du commutateur (par exemple, il s’agit d’un interphone). L’application peut utiliser cette indication pour aider l’utilisateur à sélectionner l’apparence d’appel correcte à utiliser pour effectuer un appel. Lorsque ce bit est désactivé, il n’indique pas nécessairement que l’adresse peut être utilisée pour effectuer des appels externes, car le fournisseur de services ne peut pas être Cognizant du type de ligne.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



L’adresse est associée à une ligne directe (Trunk) directe et ne peut pas être utilisée pour effectuer des appels internes sur un PBX. L’application peut utiliser cette indication pour aider l’utilisateur à sélectionner l’apparence d’appel correcte à utiliser pour effectuer un appel. Lorsque ce bit est désactivé, il n’indique pas nécessairement que l’adresse peut être utilisée pour effectuer des appels internes, car le fournisseur de services ne peut pas être Cognizant du type de ligne.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



Cette adresse ne prend pas en charge la traduction d’adresses de réseau téléphonique commutée publique. Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 3,0 ou supérieure.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Spécifie si le téléphone du tiers d’origine peut être automatiquement pris offhook lors de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



Spécifie si la numérotation partielle est disponible.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



**True** si [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut être utilisé pour récupérer un appel détecté par l’utilisateur en tant qu’appel en attente d’appel ; Sinon, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



Spécifie si un identificateur de groupe est requis pour la collecte d’appels.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



Cette adresse a amélioré les fonctionnalités de surveillance de la progression des appels qui peuvent être appliquées aux appels sortants afin de déterminer les États d’appel tels que les *rappels*, les éléments *occupés*, les *specialinfo* et les *connexions*, ou le type de média de l’appareil qui répond à l’appel. Il peut également avoir la possibilité de transférer automatiquement les appels sortants vers une autre adresse lorsqu’un appel atteint un ensemble prédéfini d’États.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_file d’attente LINEADDRCAPFLAGS**
</dt> <dd> <dl> <dt>



Cette adresse n’est pas associée à une station ou un appareil physique particulier, mais constitue un point de suspension où les appels attendent un traitement supplémentaire. Les appels placés dans la file d’attente peuvent recevoir un traitement particulier. Elles peuvent également être automatiquement transférées lorsqu’une ressource particulière est disponible (par exemple, si la file d’attente est une file d’attente ACD et que des appels attendent un agent disponible).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**
</dt> <dd> <dl> <dt>



Cette adresse n’est pas associée à une station ou un appareil physique particulier, mais est un emplacement de stockage où les appels attendent le routage par l’application (l’application examine l’adresse appelée et peut rediriger l’appel vers une autre adresse). L’appel peut également être transféré automatiquement en cas d’expiration du délai d’attente de routage (le commutateur suppose généralement un routage par défaut).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ sécurisé**
</dt> <dd> <dl> <dt>



Spécifie si les appels sur cette adresse peuvent être sécurisés au moment de la configuration de l’appel.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETCALLINGID**
</dt> <dd> <dl> <dt>



L’application peut choisir de définir le membre **CallingPartyID** dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) lors de l’appel de [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) et d’autres fonctions qui acceptent une structure **LINECALLPARAMS** . Le fournisseur de services, si le contenu de l’identificateur est acceptable et qu’un chemin d’accès est disponible, transmettez l’identificateur au tiers appelé pour indiquer l’identité du tiers appelant.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**
</dt> <dd> <dl> <dt>



Spécifie si la configuration d’un appel de conférence commence par un appel initial (**false**) ou sans appel initial (**true**).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**
</dt> <dd> <dl> <dt>



Spécifie si un appel bloqué peut être transféré. Souvent, seuls les appels au blocage de la consultation peuvent être transférés.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



Spécifie si un appel entièrement nouveau peut être établi pour une utilisation en tant qu’appel de consultation lors du transfert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Aucune extensibilité. Tous les 32 bits sont réservés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

