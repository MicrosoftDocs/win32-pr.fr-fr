---
title: Fonctions de rappel d’application cliente
description: Deux types de signatures de rappel.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380243"
---
# <a name="client-application-callback-functions"></a>Fonctions de rappel d’application cliente

Le Windows Biometric Framework prend en charge deux types de signatures de rappel. À partir de Windows 8, le rappel suivant est pris en charge. Nous vous recommandons d’implémenter ce rappel pour toutes les nouvelles applications. Toutefois, ce rappel ne peut pas être utilisé dans Windows 7.



| Rappel                                                                                     | Description                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel d' \_ achèvement \_ asynchrone PWINBIO**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Indique à l’application cliente qu’une opération asynchrone démarrée à l’aide de [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) ou de [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) est terminée.<br/> |



 

Les fonctions de rappel suivantes ont été introduites dans Windows 7. Nous vous recommandons de ne pas les implémenter pour les nouvelles applications qui ciblent les systèmes d’exploitation Windows 8 et versions ultérieures.



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

 

 





