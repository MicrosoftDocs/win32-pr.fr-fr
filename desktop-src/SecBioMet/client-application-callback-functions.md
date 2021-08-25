---
title: Fonctions de rappel d’application cliente
description: Deux types de signatures de rappel.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977099"
---
# <a name="client-application-callback-functions"></a>Fonctions de rappel d’application cliente

le Windows Biometric Framework prend en charge deux types de signatures de rappel. à partir de Windows 8, le rappel suivant est pris en charge. Nous vous recommandons d’implémenter ce rappel pour toutes les nouvelles applications. toutefois, ce rappel ne peut pas être utilisé dans Windows 7.



| Rappel                                                                                     | Description                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel d' \_ achèvement \_ asynchrone PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Indique à l’application cliente qu’une opération asynchrone démarrée à l’aide de [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) ou de [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) est terminée.<br/> |



 

les fonctions de rappel suivantes ont été introduites dans Windows 7. nous vous recommandons de ne pas les implémenter pour les nouvelles applications qui ciblent les Windows 8 et les systèmes d’exploitation ultérieurs.



| Rappel                                                                                 | Description                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel de capture PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Retourne les résultats de la fonction asynchrone [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .<br/> |
| [**\_rappel de \_ capture d’inscription PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Retourne les résultats de la fonction asynchrone [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .<br/> |
| [**\_rappel d’événement PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Retourne les résultats de la fonction asynchrone [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .<br/>           |
| [**PWINBIO \_ identifier le \_ rappel**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Retourne les résultats de la fonction asynchrone [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .<br/>           |
| [**PWINBIO \_ Rechercher \_ le \_ rappel de capteur**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Retourne les résultats de la fonction asynchrone [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .<br/>   |
| [**\_rappel de vérification de PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Retourne les résultats de la fonction asynchrone [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .<br/>               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’application cliente](client-application-reference.md)
</dt> </dl>

 

 





