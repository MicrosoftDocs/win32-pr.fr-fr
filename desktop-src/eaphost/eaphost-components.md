---
title: Composants d’EAPHost
description: En savoir plus sur les trois composants de l’authentification EAPHost. Affichez les ressources disponibles supplémentaires pour l’utilisation de l’authentification EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463718"
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

Si vous créez une nouvelle méthode d’authentification EAP à gérer par EAPHost, reportez-vous à la référence de l' [API de méthode homologue EAPHost](eap-host-peer-method-api-reference.md) et aux [API de méthode d’authentificateur EAPHost](eaphost-authenticator-method-apis.md). Notez que vous allez créer des implémentations de ces API exposées dans une nouvelle DLL que EAPHost charge, au lieu de les appeler directement.

 

 




