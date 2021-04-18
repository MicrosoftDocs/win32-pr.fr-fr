---
description: La liste suivante répertorie les codes d’erreur que TAPI peut retourner lors de l’appel d’opérations sur des lignes, des adresses ou des appels.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Constantes LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540092"
---
# <a name="lineerr_-constants"></a>\_Constantes LINEERR

La liste suivante répertorie les codes d’erreur que TAPI peut retourner lors de l’appel d’opérations sur des lignes, des adresses ou des appels. Pour plus d’informations sur la façon de déterminer les codes d’erreur qu’une fonction particulière peut retourner, consultez les descriptions des fonctions individuelles.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



L’adresse spécifiée est bloquée et ne peut pas être numérotée sur l’appel spécifié.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



Le blocage des appels est activé pour l’adresse de l’appel cible.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ allouée**
</dt> <dd> <dl> <dt>



La ligne ne peut pas être ouverte en raison d’une condition persistante, telle que celle d’un port série qui est ouvert en mode exclusif par un autre processus.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



L’identificateur d’appareil ou l’identificateur de périphérique de ligne spécifié, par exemple dans un paramètre *dwDeviceID* , n’est pas valide ou est hors limites.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**
</dt> <dd> <dl> <dt>



Le membre du mode porteur dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) n’est pas valide, le mode porteur spécifié dans **LINECALLPARAMS** n’est pas disponible, ou le mode porteur de l’appel ne peut pas être remplacé par le mode de support spécifié.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**
</dt> <dd> <dl> <dt>



Le mode de facturation de l’appel a été rejeté.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**
</dt> <dd> <dl> <dt>



Toutes les apparences des appels sur l’adresse spécifiée sont en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**
</dt> <dd> <dl> <dt>



Le nombre maximal d’appels terminés en attente a été dépassé.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**
</dt> <dd> <dl> <dt>



Le nombre maximal de tiers pour une conférence a été atteint ou le nombre demandé de tiers ne peut pas être respecté.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**
</dt> <dd> <dl> <dt>



Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Le paramètre d’adresse de numérotation contient des caractères de contrôle de numérotation qui ne sont pas traités par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**
</dt> <dd> <dl> <dt>



Utilisation du modificateur de numérotation ( :) n’est pas pris en charge. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ déconnecté**
</dt> <dd> <dl> <dt>



L’appel a été déconnecté. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,2 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



L’application a demandé une version ou une plage de versions TAPI qui est incompatible avec, ou ne peut pas être prise en charge par, l’implémentation de l’API de téléphonie et le fournisseur de services correspondant.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



L’application a demandé une plage de versions d’extension qui n’est pas valide ou qui ne peut pas être prise en charge par le fournisseur de services correspondant.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



L’interface TAPI ne peut pas lire ou comprendre correctement le fichier Telephon.ini en raison d’incohérences internes ou de problèmes de mise en forme. Par exemple, la \[ \] section emplacements, \[ cartes \] ou \[ pays \] du fichier Telephon.ini peut être endommagée ou incohérente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ Inuse**
</dt> <dd> <dl> <dt>



Le périphérique de ligne est en cours d’utilisation et ne peut pas être configuré, autoriser l’ajout d’un tiers, autoriser la réponse à un appel, autoriser le placement d’un appel ou autoriser le transfert d’un appel.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**
</dt> <dd> <dl> <dt>



L’adresse spécifiée n’est pas valide ou n’est pas autorisée. Si ce n’est pas le cas, l’adresse contient des caractères ou des chiffres non valides, ou l’adresse de destination contient des caractères de contrôle de numérotation (W, @, $ ou ?) qui ne sont pas pris en charge par le fournisseur de services. Si cette valeur n’est pas autorisée, l’adresse spécifiée n’est pas affectée à la ligne spécifiée ou n’est pas valide pour la redirection d’adresse.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**
</dt> <dd> <dl> <dt>



L’identificateur d’adresse spécifié n’est pas valide ou est hors limites.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**
</dt> <dd> <dl> <dt>



Le mode d’adresse spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**
</dt> <dd> <dl> <dt>



L’état de l’adresse spécifiée contient un ou plusieurs bits qui ne sont pas des [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**
</dt> <dd> <dl> <dt>



L’application a référencé un type d’adresse qui n’est pas valide. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 3,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



L’activité de l’agent spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



L’application qui appelle cette opération est la cible du transfert indirect. Autrement dit, TAPI a déterminé que l’application appelante est également l’application de priorité la plus élevée pour le type de média donné. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



Les informations de groupe d’agents spécifiées ne sont pas valides ou contiennent des erreurs. L’action demandée n’a pas été effectuée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



L’application a référencé un groupe d’agents non valide. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



L’identificateur d’agent spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



Un identificateur d’agent non valide a été utilisé. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



L’état de session de l’agent n’est pas valide. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,2 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



L’état spécifié de l’agent n’est pas valide ou contient des erreurs. Aucune modification n’a été apportée à l’état de l’agent de l’adresse spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



L’application a référencé un état d’agent non valide. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



Le descripteur d’application (tel que spécifié par un paramètre *hLineApp* ) ou le descripteur d’inscription de l’application n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



Le nom d’application spécifié n’est pas valide. Si un nom d’application est spécifié par l’application, il est supposé que la chaîne ne contient pas de caractères non affichables et qu’elle se termine par zéro.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**
</dt> <dd> <dl> <dt>



Le mode de support spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**
</dt> <dd> <dl> <dt>



La saisie semi-automatique spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**
</dt> <dd> <dl> <dt>



Le descripteur d’appel spécifié n’est pas valide. Par exemple, le handle n’est pas **null** , mais n’appartient pas à la ligne spécifiée. Dans certains cas, le descripteur d’appareil d’appel spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**
</dt> <dd> <dl> <dt>



Les paramètres d’appel spécifiés ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**
</dt> <dd> <dl> <dt>



Le paramètre de privilège d’appel spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**
</dt> <dd> <dl> <dt>



Le paramètre Select spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**
</dt> <dd> <dl> <dt>



L’état actuel d’un appel n’est pas dans un état valide pour l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**
</dt> <dd> <dl> <dt>



La liste d’États d’appels spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**
</dt> <dd> <dl> <dt>



L’identificateur de carte permanente spécifié dans *dwCard* est introuvable dans une entrée de la \[ section des cartes du \] Registre.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**
</dt> <dd> <dl> <dt>



L’identificateur de saisie semi-automatique n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**
</dt> <dd> <dl> <dt>



Le descripteur d’appel spécifié pour l’appel de conférence n’est pas valide ou n’est pas un handle pour un appel de conférence.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**
</dt> <dd> <dl> <dt>



Le handle de l’appel de consultation spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**
</dt> <dd> <dl> <dt>



Le code du pays ou de la région spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



Le périphérique de ligne n’a aucun appareil associé pour la classe d’appareil donnée, ou la ligne spécifiée ne prend pas en charge la classe d’appareil indiquée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**
</dt> <dd> <dl> <dt>



Le handle de périphérique de ligne n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**
</dt> <dd> <dl> <dt>



Les paramètres de numérotation ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**
</dt> <dd> <dl> <dt>



La liste de chiffres spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**
</dt> <dd> <dl> <dt>



Le mode de chiffrement spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**
</dt> <dd> <dl> <dt>



Les chiffres de fin spécifiés ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



Le numéro de version de l’extension du fournisseur de services n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



Le paramètre *dwFeature* n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



L’application a appelé une fonctionnalité qui n’est pas disponible sur cette ligne.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**
</dt> <dd> <dl> <dt>



L’identificateur de groupe spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**
</dt> <dd> <dl> <dt>



L’appel, l’appareil, le périphérique de ligne ou le handle de ligne spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**
</dt> <dd> <dl> <dt>



La configuration de l’appareil ne peut pas être modifiée dans l’état actuel de la ligne. La ligne peut être utilisée par une autre application ou un paramètre *dwLineStates* contient un ou plusieurs bits qui ne sont pas des [ \_ constantes LINEDEVSTATE](linedevstate--constants.md). La valeur **LINEERR \_ INVALLINESTATE** peut également indiquer que l’appareil est déconnecté ou hors service. Ces États sont indiqués en définissant les bits correspondant aux valeurs d' *\_ InService* *LINEDEVSTATUSFLAGS \_ Connected* et LINEDEVSTATUSFLAGS sur 0 dans le membre **dwDevStatusFlags** de la structure [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) retournée par la fonction [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**
</dt> <dd> <dl> <dt>



L’identificateur d’emplacement permanent spécifié dans *dwLocation* est introuvable dans une entrée de la \[ section locations du \] Registre.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**
</dt> <dd> <dl> <dt>



La liste de médias spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**
</dt> <dd> <dl> <dt>



La liste des types de média (modes) à analyser contient des informations non valides, le paramètre de type de média spécifié n’est pas valide ou le fournisseur de services ne prend pas en charge le type de média spécifié. Les types de médias pris en charge sur la ligne sont répertoriés dans le membre **dwMediaModes** de la structure [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**
</dt> <dd> <dl> <dt>



Le nombre donné dans *dwMessageID* est en dehors de la plage spécifiée par le membre **dwNumCompletionMessages** dans la structure [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Un paramètre ou une structure vers laquelle pointe un paramètre contient des informations non valides, un code de pays ou de région n’est pas valide, un handle de fenêtre n’est pas valide ou le paramètre de liste de transfert spécifié contient des informations non valides.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**
</dt> <dd> <dl> <dt>



L’identificateur de parc n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**
</dt> <dd> <dl> <dt>



Le mode de parc spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



Le mot de passe spécifié n’est pas correct et l’action demandée n’a pas été effectuée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



L’application a utilisé un mot de passe non valide. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,0 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Un ou plusieurs des paramètres de pointeur spécifiés (tels que *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* et *lpToneList*) ne sont pas valides, ou un pointeur obligatoire vers un paramètre de sortie a la **valeur null**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**
</dt> <dd> <dl> <dt>



Un indicateur ou une combinaison d’indicateurs non valide a été défini pour le paramètre *dwPrivileges* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**
</dt> <dd> <dl> <dt>



Le taux spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**
</dt> <dd> <dl> <dt>



L’indicateur [**LINEREQUESTMODE**](linerequestmode--constants.md) n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**
</dt> <dd> <dl> <dt>



L’identificateur de terminal spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**
</dt> <dd> <dl> <dt>



Le paramètre du mode terminal spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**
</dt> <dd> <dl> <dt>



Les délais d’attente ne sont pas pris en charge ou une valeur se trouve en dehors de la plage valide spécifiée dans [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**
</dt> <dd> <dl> <dt>



Le ton personnalisé spécifié ne représente pas un ton valide ou est constitué d’un trop grand nombre de fréquences ou la structure tonale spécifiée ne décrit pas un ton valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**
</dt> <dd> <dl> <dt>



La liste de tonalités spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**
</dt> <dd> <dl> <dt>



Le paramètre de mode de tonalité spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**
</dt> <dd> <dl> <dt>



Le paramètre de mode de transfert spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**
</dt> <dd> <dl> <dt>



LINEMAPPER était la valeur passée dans le paramètre *dwDeviceID* , mais aucune ligne ne correspond aux critères spécifiés dans le paramètre *lpCallParams* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOconference**
</dt> <dd> <dl> <dt>



L’appel spécifié n’est pas un handle d’appel de conférence ou un appel de participant.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NOdevice**
</dt> <dd> <dl> <dt>



L’identificateur de périphérique spécifié, qui était précédemment valide, n’est plus accepté, car l’appareil associé a été supprimé du système depuis le dernier initialisation de l’interface TAPI. Sinon, le périphérique de ligne n’a aucun appareil associé pour la classe d’appareil donnée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOdriver**
</dt> <dd> <dl> <dt>



Soit Tapiaddr.dll est introuvable, soit le fournisseur de service téléphonique pour l’appareil spécifié a détecté que l’un de ses composants est manquant ou endommagé d’une façon qui n’a pas été détectée lors de l’initialisation. L’utilisateur doit être invité à utiliser le panneau de configuration de la téléphonie pour corriger le problème.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Mémoire insuffisante pour effectuer l’opération ou impossible de verrouiller la mémoire.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Un fournisseur de services de téléphonie qui ne prend pas en charge plusieurs instances est listé plusieurs fois dans la \[ section fournisseurs du \] Registre. L’application doit demander à l’utilisateur d’utiliser le panneau de configuration de la téléphonie pour supprimer le pilote dupliqué.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Plusieurs instances de ce fournisseur de services ne sont pas autorisées.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOrequest**
</dt> <dd> <dl> <dt>



Il n’y a actuellement aucune demande en attente du mode indiqué, ou l’application n’est plus la priorité la plus élevée pour le mode de demande spécifié.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_**
</dt> <dd> <dl> <dt>



L’application n’a pas de privilège de propriétaire pour l’appel spécifié.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ NOTREGISTERED**
</dt> <dd> <dl> <dt>



L’application n’est pas inscrite en tant que destinataire de la demande pour le mode de requête indiqué.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



L’opération a échoué pour une raison non spécifiée ou inconnue.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



L’opération n’est pas disponible, par exemple pour l’appareil donné ou la ligne spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**
</dt> <dd> <dl> <dt>



Actuellement, le fournisseur de services n’a pas suffisamment de bande passante disponible pour la vitesse spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**Réinit LINEERR \_**
</dt> <dd> <dl> <dt>



Si la réinitialisation TAPI a été demandée, par exemple suite à l’ajout ou à la suppression d’un fournisseur de services de téléphonie, les demandes [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)ou [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) sont rejetées avec cette erreur jusqu’à ce que la dernière application arrête son utilisation de l’API (à l’aide de [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), et que les applications soient de nouveau autorisées à appeler **lineInitialize** ou **lineInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**Réinit LINEERR \_**
</dt> <dd> <dl> <dt>



L’application a tenté d’initialiser TAPI deux fois.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Plus de demandes sont en attente que l’appareil ne peut en gérer.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



Ressources insuffisantes pour terminer l’opération. Par exemple, une ligne ne peut pas être ouverte en raison d’un surengagement de ressources dynamique.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



Le membre **dwTotalSize** d’une structure ne spécifie pas suffisamment de mémoire pour contenir la partie fixe de la structure spécifiée.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**
</dt> <dd> <dl> <dt>



Une cible pour le transfert d’appel est introuvable. Cela peut se produire si l’application nommée n’a pas ouvert la même ligne avec le \_ bit de propriétaire LINECALLPRIVILEGE dans le paramètre *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen). Ou, dans le cas de la remise en mode Media, aucune application n’a ouvert la même ligne avec le \_ bit de propriétaire LINECALLPRIVILEGE dans le paramètre *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) et avec le type de média spécifié dans le paramètre *dwMediaMode* ayant été spécifié dans le paramètre *dwMediaModes* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**
</dt> <dd> <dl> <dt>



L’application qui appelle cette opération est la cible du transfert indirect. Autrement dit, TAPI a déterminé que l’application appelante est également l’application de priorité la plus élevée pour le type de média donné.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR \_ non initialisé**
</dt> <dd> <dl> <dt>



L’opération a été appelée avant toute application appelée [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**
</dt> <dd> <dl> <dt>



L’utilisateur a annulé l’appel. Cette valeur est exposée uniquement aux applications qui négocient une version TAPI 2,2 ou ultérieure.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**
</dt> <dd> <dl> <dt>



La chaîne contenant les informations utilisateur-utilisateur dépasse le nombre maximal d’octets spécifié dans le membre **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** ou **dwUUISendUserUserInfoSize** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), ou la chaîne contenant les informations utilisateur-utilisateur est trop longue.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs 0xC0000000 à 0xFFFFFFFF sont disponibles pour les extensions spécifiques à l’appareil. Les valeurs 0x80000000 à 0xBFFFFFFF sont réservées, tandis que 0x00000000 à 0x7FFFFFFF sont utilisées en tant qu’identificateurs de demande.

Si une application obtient une erreur indiquant qu’elle n’est pas spécifiquement gérée (par exemple, une erreur définie par une extension spécifique à l’appareil), elle doit traiter l’erreur comme un \_ OPERATIONFAILED LINEERR (pour une raison non spécifiée).

Lors de l’appel des \_ constantes LINEERR qui sont nouvelles avec TAPI 3,0, le fichier Tapierr.MC doit être mis à jour avec de nouveaux messages.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




