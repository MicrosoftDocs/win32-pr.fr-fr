---
title: Composants d’EAPHost
description: En savoir plus sur les trois composants de l’authentification EAPHost. Affichez les ressources disponibles supplémentaires pour l’utilisation de l’authentification EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa86f09473b14df6dbcc8bbc667dc4a1cc1badf9e0b6dd67ac95f8d11f2bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086413"
---
# <a name="components-of-eaphost"></a>Composants d’EAPHost

Cette rubrique décrit les trois composants de l’authentification EAPHost.

## <a name="eaphost-components"></a>Composants EAPHost

L’authentification EAPHost comporte les trois composants suivants.

-   Le demandeur, qui effectue les demandes d’authentification.
-   Les méthodes EAP homologue (ou client), qui implémentent les méthodes EAP spécifiques et gèrent la session d’authentification côté client.
-   Les méthodes EAP de l’authentificateur (ou du serveur) qui implémentent le côté serveur du protocole EAP.

Les API du demandeur sont appelées directement à partir d’une application qui souhaite s’authentifier via EAPHost. Toutefois, les API de méthode d’homologue et de méthode d’authentificateur sont des prototypes de fonction qui doivent être implémentés pour un type de méthode d’authentification EAP spécifique, tel que MS-CHAPv2 (Microsoft Challenge Handshake Authentication Protocol version 2,0).

Si vous créez une application qui utilisera EAPHost pour l’authentification, reportez-vous à la référence de l' [API du demandeur EAPHost](eap-host-supplicant-api-reference.md).

si vous créez une nouvelle méthode d’authentification EAP à gérer par EAPHost, reportez-vous à la référence de l' [api de méthode homologue eaphost](eap-host-peer-method-api-reference.md) et aux [api de méthode Authenticator eaphost](eaphost-authenticator-method-apis.md). Notez que vous allez créer des implémentations de ces API exposées dans une nouvelle DLL que EAPHost charge, au lieu de les appeler directement.

 

 




