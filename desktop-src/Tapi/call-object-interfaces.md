---
description: L’objet d’appel est créé lorsqu’un appel est en vigueur. Les interfaces associées obtiennent et définissent les informations relatives à l’appel.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Appeler des interfaces d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952098"
---
# <a name="call-object-interfaces"></a>Appeler des interfaces d’objet

L' [objet d’appel](call-object.md) est créé lorsqu’un appel est en vigueur. Les interfaces associées obtiennent et définissent les informations relatives à l’appel.

Les interfaces d’énumérateur et d’événement ne sont pas directement exposées sur l’objet d’appel, mais elles sont répertoriées ici pour des raisons de commodité de référence.

Les interfaces [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent), [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent), [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent), [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)et [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) ne sont pas directement exposées sur l’objet d’appel, mais sont étroitement liées à celle-ci et sont répertoriées ici pour des raisons de commodité de référence.



| Interface                                                      | Description                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Fournit des informations concernant un objet d’appel, tel que l’état d’appel ou les terminaux en cours d’utilisation.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Étend [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) en fournissant des méthodes pour définir le filtrage des événements sur la base de chaque appel.                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Utilisé pour la connexion, la réponse et l’exécution d’opérations de téléphonie de base sur un objet d’appel.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Étend [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) en fournissant des méthodes pour sélectionner un terminal sur un appel.              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Interface de notification pour [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Interface de notification pour les modifications des informations sur les appels.                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Obtient des informations relatives à un événement d’appel.                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Obtient des informations relatives à un événement de média d’appel.                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Fournit des méthodes pour contrôler les tonalités personnalisées possibles avec certains ensembles de téléphones.                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Fournit des méthodes pour spécifier les tonalités et les caractéristiques de ton qui génèrent des événements de tonalité.                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Prend en charge les applications héritées qui doivent communiquer directement avec un appareil.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Étend [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) en fournissant des méthodes pour la détection et la génération de fréquences. |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Énumère [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



