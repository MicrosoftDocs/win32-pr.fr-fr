---
description: L’interface IX509SCEPEnrollment expose les méthodes suivantes.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Méthodes IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993539"
---
# <a name="ix509scepenrollment-methods"></a>Méthodes IX509SCEPEnrollment

L’interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expose les méthodes suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                              | Description                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Méthode CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Créez un message de demande PKCS10 avec un mot de passe de stimulation. Le message de demande se trouve dans un PKCS7 enveloppé chiffré avec le certificat de chiffrement de serveur SCEP et signé par le certificat de signature du serveur.<br/> |
| [**Méthode CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Récupérez un certificat émis précédemment.<br/>                                                                                                                                                                   |
| [**Méthode CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Créez un message pour l’interrogation de certificat (inscription manuelle).<br/>                                                                                                                                               |
| [**Méthode DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Supprimez les certificats ou les clés créés pour la demande.<br/>                                                                                                                                                    |
| [**Initialize (méthode)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Initialisez l’instance en vue d’une nouvelle demande.<br/>                                                                                                                                                   |
| [**Méthode InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Initialisez l’instance pour préparer la génération d’un message pour récupérer un certificat émis ou installez une réponse pour une demande précédente de l’émetteur.<br/>                                              |
| [**Méthode ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Traite un message de réponse et retourne la disposition du message.<br/>                                                                                                                                       |



 

 

 




