---
title: Constantes WINBIO_OPERATION_TYPE ( \_ types WINBIO. h)
description: Spécifiez le type d’opération asynchrone en cours d’exécution.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237822"
---
# <a name="winbio_operation_type-constants"></a>\_Constantes de type d’opération WINBIO \_

les constantes suivantes peuvent être retournées par l’Windows Biometric Framework dans un [**\_ \_ résultat asynchrone WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) pour spécifier le type d’opération asynchrone en cours d’exécution.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_opération WINBIO \_ aucun**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Aucune opération n’a été identifiée.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_opération WINBIO \_ ouverte**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Une session biométrique a été ouverte. Pour plus d’informations, consultez [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_opération WINBIO \_ Close**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Une session biométrique a été fermée. Pour plus d’informations, consultez [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**vérification de l' \_ opération WINBIO \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Un échantillon biométrique a été vérifié par rapport à une identité de l’utilisateur. Pour plus d’informations, consultez [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**identification de l' \_ opération WINBIO \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Un échantillon biométrique a été capturé et comparé à un modèle existant. Pour plus d’informations, consultez [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**capteur de recherche de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Le numéro d’identification d’une unité biométrique a été récupéré. Pour plus d’informations, consultez [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**début de l’inscription de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Une séquence d’inscription biométrique a été lancée. Pour plus d’informations, consultez [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**CAPTURE d’inscription de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Un échantillon biométrique a été capturé et ajouté au modèle. Pour plus d’informations, consultez [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**validation d’inscription de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Un modèle biométrique en attente a été finalisé. Pour plus d’informations, consultez [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**annulation de l’inscription de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Un modèle biométrique en attente a été ignoré. Pour plus d’informations, consultez [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ inscriptions enum de l’opération WINBIO \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Les sous-facteurs d’un modèle donné ont été énumérés. Pour plus d’informations, consultez [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ opération \_ supprimer le \_ modèle**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Un modèle biométrique a été supprimé du magasin. Pour plus d’informations, consultez [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_exemple de \_ capture d’opération WINBIO \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Un échantillon biométrique a été capturé. Pour plus d’informations, consultez [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**propriété d’extraction de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Une session biométrique, une unité ou une propriété de modèle a été récupérée. Pour plus d’informations, consultez [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO \_ operation \_ Set, \_ propriété**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Une session biométrique, une unité, un modèle ou une propriété de compte a été définie. Pour plus d’informations, consultez [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**événement d’extraction de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Non utilisé.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**unité de verrouillage de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Une unité biométrique a été verrouillée pour une utilisation exclusive par une session. Pour plus d’informations, consultez [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unité de \_ déverrouillage de l’opération WINBIO \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Le verrou de session sur une unité biométrique a été relâché. Pour plus d’informations, consultez [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**unité de contrôle de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Les opérations définies par le fournisseur ont été effectuées sur une unité de contrôle. Pour plus d’informations, consultez [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_unité de contrôle d’opération WINBIO \_ \_ \_ privilégiée**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Les opérations définies par le fournisseur privilégié ont été effectuées sur une unité de contrôle. Pour plus d’informations, consultez [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**\_ \_ infrastructure ouverte de l’opération WINBIO \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Un descripteur de l’infrastructure biométrique a été ouvert.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**Framework de fermeture de l' \_ opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Un descripteur de l’infrastructure biométrique a été fermé. Pour plus d’informations, consultez [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_fournisseurs de \_ services d’énumération d’opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Les fournisseurs de services biométriques installés ont été énumérés. Pour plus d’informations, consultez [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ unités biométriques de l’opération WINBIO \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Les unités biométriques attachées ont été énumérées. Pour plus d’informations, consultez [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_opération WINBIO \_ énumérer les \_ bases de données**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Les bases de données inscrites ont été énumérées. Pour plus d’informations, consultez [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**arrivée de l' \_ unité d’opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Une unité biométrique a été créée. Pour plus d’informations, consultez [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**suppression de l' \_ unité d’opération WINBIO \_ \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Une unité biométrique a été supprimée. Pour plus d’informations, consultez [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO \_ d' \_ identifier \_ et de \_ libérer le \_ ticket de l’opération**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Réservé. Cette valeur est prise en charge à partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_ \_ \_ ticket de vérification et de \_ libération de \_ l’opération WINBIO**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Réservé. Cette valeur est prise en charge à partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_présence du \_ moniteur d’opération WINBIO \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



La reconnaissance faciale ou le mécanisme de surveillance de l’IRIS a été activé. Pour plus d’informations, consultez [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Cette valeur est prise en charge à partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**\_opération WINBIO \_ inscrire \_ Select**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Un individu d’un groupe de personnes qui sont représentées par des données dans l’exemple de mémoire tampon a été spécifié comme individu à inscrire. Pour plus d’informations, consultez [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Cette valeur est prise en charge à partir de Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                                                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





