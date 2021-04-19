---
description: Les \_ constantes TAPIERR fournissent des informations concernant les échecs d’exécution de la fonction.
ms.assetid: 6d1cf18b-efeb-4703-9b8e-fce59b61b63f
title: Constantes TAPIERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e8a60e2a625ff456a4a8aa2730b80000e92ff54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535911"
---
# <a name="tapierr_-constants"></a>\_Constantes TAPIERR

Les **\_ constantes TAPIERR** fournissent des informations concernant les échecs d’exécution de la fonction.

<dl> <dt>

<span id="TAPIERR_CONNECTED"></span><span id="tapierr_connected"></span>**TAPIERR \_ connecté**
</dt> <dd> <dl> <dt>



L’opération ne peut pas être effectuée tant que l’état de l’appel est connecté.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTBUSY"></span><span id="tapierr_destbusy"></span>**TAPIERR \_ DESTBUSY**
</dt> <dd> <dl> <dt>



La destination de l’appel est occupée.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTNOANSWER"></span><span id="tapierr_destnoanswer"></span>**TAPIERR \_ DESTNOANSWER**
</dt> <dd> <dl> <dt>



La destination de l’appel n’a pas répondu.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTUNAVAIL"></span><span id="tapierr_destunavail"></span>**TAPIERR \_ DESTUNAVAIL**
</dt> <dd> <dl> <dt>



La destination de l’appel n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICECLASSUNAVAIL"></span><span id="tapierr_deviceclassunavail"></span>**TAPIERR \_ DEVICECLASSUNAVAIL**
</dt> <dd> <dl> <dt>



La classe d’appareil requise n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEIDUNAVAIL"></span><span id="tapierr_deviceidunavail"></span>**TAPIERR \_ DEVICEIDUNAVAIL**
</dt> <dd> <dl> <dt>



L’identificateur de périphérique requis n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEINUSE"></span><span id="tapierr_deviceinuse"></span>**TAPIERR \_ DEVICEINUSE**
</dt> <dd> <dl> <dt>



L’appareil requis est en cours d’utilisation.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DROPPED"></span><span id="tapierr_dropped"></span>**TAPIERR \_ supprimé**
</dt> <dd> <dl> <dt>



L’appel a été supprimé.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDESTADDRESS"></span><span id="tapierr_invaldestaddress"></span>**TAPIERR \_ INVALDESTADDRESS**
</dt> <dd> <dl> <dt>



Le pointeur vers l’adresse de destination n’est pas valide, est **null** ou la chaîne d’adresse de destination est trop longue.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICECLASS"></span><span id="tapierr_invaldeviceclass"></span>**TAPIERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



La classe de périphérique demandée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICEID"></span><span id="tapierr_invaldeviceid"></span>**TAPIERR \_ INVALDEVICEID**
</dt> <dd> <dl> <dt>



L’identificateur de classe d’appareil demandé n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALPOINTER"></span><span id="tapierr_invalpointer"></span>**TAPIERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Le pointeur ne fait pas référence à un emplacement de mémoire valide. Un ou plusieurs des pointeurs *lpszDestAddress*, *lpszAppName*, *lpszCalledParty* ou *lpszComment* ont été spécifiés mais ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALWINDOWHANDLE"></span><span id="tapierr_invalwindowhandle"></span>**TAPIERR \_ INVALWINDOWHANDLE**
</dt> <dd> <dl> <dt>



Le handle de fenêtre n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOREQUESTRECIPIENT"></span><span id="tapierr_norequestrecipient"></span>**TAPIERR \_ NOREQUESTRECIPIENT**
</dt> <dd> <dl> <dt>



Aucune application destinataire n’est disponible pour traiter la demande. L’utilisateur doit démarrer l’application destinataire et réessayer.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOTADMIN"></span><span id="tapierr_notadmin"></span>**TAPIERR \_ NOTADMIN**
</dt> <dd> <dl> <dt>



L’opération demandée requiert des privilèges d’administrateur.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTCANCELLED"></span><span id="tapierr_requestcancelled"></span>**TAPIERR \_ REQUESTCANCELLED**
</dt> <dd> <dl> <dt>



La demande de téléphonie assistée a été annulée.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTFAILED"></span><span id="tapierr_requestfailed"></span>**TAPIERR \_ REQUESTFAILED**
</dt> <dd> <dl> <dt>



La requête a échoué pour des raisons non spécifiées.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTQUEUEFULL"></span><span id="tapierr_requestqueuefull"></span>**TAPIERR \_ REQUESTQUEUEFULL**
</dt> <dd> <dl> <dt>



Une application de destinataire est active, mais la file d’attente de demandes est pleine ou la mémoire est insuffisante pour étendre la file d’attente. L’application peut réessayer plus tard.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNREQUESTID"></span><span id="tapierr_unknownrequestid"></span>**TAPIERR \_ UNKNOWNREQUESTID**
</dt> <dd> <dl> <dt>



L’identificateur de demande référencé n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNWINHANDLE"></span><span id="tapierr_unknownwinhandle"></span>**TAPIERR \_ UNKNOWNWINHANDLE**
</dt> <dd> <dl> <dt>



Un handle de fenêtre inconnu a été référencé.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Toutes les autres \_ valeurs TAPIERR sont obsolètes et ne doivent pas être utilisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




