---
description: Il s’agit de la liste des codes d’erreur que l’implémentation peut retourner lors de l’appel d’opérations sur des appareils téléphoniques. Consultez les descriptions des fonctions individuelles pour déterminer lequel de ces codes d’erreur chaque fonction peut retourner.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Constantes PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66c4dd2078b7de1572137ee1d759e7b186328dc5604c9790e444db428eb774a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060657"
---
# <a name="phoneerr_-constants"></a>\_Constantes PHONEERR

Il s’agit de la liste des codes d’erreur que l’implémentation peut retourner lors de l’appel d’opérations sur des appareils téléphoniques. Consultez les descriptions des fonctions individuelles pour déterminer lequel de ces codes d’erreur chaque fonction peut retourner.

<dl> <dt>

<span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ allouée**
</dt> <dd> <dl> <dt>



La ressource spécifiée est déjà allouée.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



L’identificateur d’appareil spécifié n’est pas valide ou est hors limites.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ déconnecté**
</dt> <dd> <dl> <dt>



L’appel a été déconnecté.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



L’application a demandé une version ou une plage de versions d’API qui ne peut pas être prise en charge par l’implémentation de l’API de téléphonie ou le fournisseur de services correspondant.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



L’application a demandé une version d’extension ou une plage de versions qui ne peut pas être prise en charge par le fournisseur de services.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



En raison d’incohérences internes ou de problèmes de mise en forme dans le fichier Telephon.ini, il est impossible de les lire et de les comprendre correctement par l’interface TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ Inuse**
</dt> <dd> <dl> <dt>



L’appareil est en cours d’utilisation. L’appareil ne peut pas être configuré.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



Le handle d’utilisation ou le descripteur d’enregistrement spécifié de l’application n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



Le nom d’application spécifié n’est pas valide. Si un nom d’application est spécifié par l’application, il est supposé que la chaîne ne contient pas de caractères non affichables et qu’elle se termine par un caractère **null**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**
</dt> <dd> <dl> <dt>



L’identificateur de bouton/lampe spécifié est hors limites ou n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**
</dt> <dd> <dl> <dt>



Le paramètre de mode du bouton n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**
</dt> <dd> <dl> <dt>



Le paramètre États du bouton n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**
</dt> <dd> <dl> <dt>



L’identificateur de données spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



Le téléphone spécifié ne prend pas en charge la classe d’appareil indiquée.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



Le numéro de version de l’extension du fournisseur de services n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



Le paramètre d’appareil hookswitch n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**
</dt> <dd> <dl> <dt>



Le paramètre de mode hookswitch n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**
</dt> <dd> <dl> <dt>



Le paramètre de mode de lampe spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Un paramètre, tel qu’une valeur de ligne ou de colonne ou un handle de fenêtre, n’est pas valide ou est hors limites.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**
</dt> <dd> <dl> <dt>



Le handle d’appareil spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**
</dt> <dd> <dl> <dt>



L’appareil téléphonique n’est pas dans un état valide pour l’opération demandée.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Un ou plusieurs des paramètres de pointeur spécifiés ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**
</dt> <dd> <dl> <dt>



Le paramètre *dwPrivilege* n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**
</dt> <dd> <dl> <dt>



Le paramètre de mode Ring n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NOdevice**
</dt> <dd> <dl> <dt>



L’identificateur de périphérique spécifié, qui était précédemment valide, n’est plus accepté, car l’appareil associé a été supprimé du système depuis que l’interface TAPI a été initialisée pour la dernière fois, ou endommagée d’une façon qui n’a pas été détectée lors de l’initialisation.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOdriver**
</dt> <dd> <dl> <dt>



Le fournisseur de services téléphoniques de l’appareil spécifié a détecté que l’un de ses composants est manquant ou endommagé d’une manière qui n’a pas été détectée au moment de l’initialisation. L’utilisateur doit être invité à utiliser le panneau de configuration de la téléphonie pour corriger le problème.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Mémoire insuffisante pour terminer l’opération demandée, ou impossible d’allouer ou de verrouiller la mémoire.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_**
</dt> <dd> <dl> <dt>



L’application ne dispose pas de privilèges de propriétaire sur le périphérique téléphonique spécifié.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



L’opération a échoué pour une raison non spécifiée.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



L’opération n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**Réinit PHONEERR \_**
</dt> <dd> <dl> <dt>



Si la réinitialisation TAPI a été demandée, par exemple suite à l’ajout ou à la suppression d’un fournisseur de services de téléphonie, les demandes [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) ou [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) sont rejetées avec cette erreur jusqu’à ce que la dernière application arrête son utilisation de l’API (à l’aide de [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), et que les applications soient de nouveau autorisées à appeler **phoneInitialize** ou **phoneInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Le nombre maximal de demandes de téléphone en suspens a été dépassé.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



L’opération ne peut pas être effectuée en raison d’un surengagement de ressources.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



La structure des majuscules de téléphone spécifiée est trop petite.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR \_ non initialisé**
</dt> <dd> <dl> <dt>



L’opération a été appelée avant toute application appelée [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Les valeurs 0xC0000000 à 0xFFFFFFFF sont disponibles pour les extensions spécifiques à l’appareil ; les valeurs 0x80000000 à 0xBFFFFFFF sont réservées ; et 0x00000000 à 0x7FFFFFFF sont utilisés en tant qu’identificateurs de demande.

Si une application obtient une erreur indiquant qu’elle n’est pas spécifiquement gérée (par exemple, une erreur définie par une extension spécifique à l’appareil), elle doit traiter l’erreur comme un \_ OPERATIONFAILED PHONEERR (pour une raison non spécifiée).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




