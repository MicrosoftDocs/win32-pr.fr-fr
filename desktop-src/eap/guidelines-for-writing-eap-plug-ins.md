---
title: Instructions pour l’écriture de dll EAP
description: Les plug-ins ou dll EAP peuvent être écrits pour optimiser leurs performances dans différents scénarios.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c786da1ca026039ffd052f1213b2904dbfa602ee67c6d74aed7a0fe11fd9d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499154"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Instructions pour l’écriture de dll EAP

Les plug-ins ou dll EAP peuvent être écrits pour optimiser leurs performances dans différents scénarios.

## <a name="general-guidelines"></a>Instructions générales

-   Pour créer une connexion chiffrée, les plug-ins EAP doivent générer des clés de chiffrement et les retourner via les attributs RADIUS spécifiques aux fournisseurs Microsoft MS-MPPE-Send-Keys et MS-MPPE-recv-keys. Pour plus d’informations, consultez la section Notes dans [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .

## <a name="wireless-guidelines"></a>Directives sans fil

Vous trouverez ci-dessous des instructions et des recommandations pour l’écriture d’un plug-in EAP qui prend en charge l’authentification des ordinateurs dans des scénarios sans fil (802.1 X). Cette section ne s’applique pas aux scénarios VPN et d’accès à distance.

-   Afin de ne pas bloquer l’exécution des systèmes sans assistance, les plug-ins EAP ne doivent pas effectuer d’appels d’interface utilisateur.
-   L’implémentation du plug-in EAP de l’étape d’authentification de l’ordinateur doit être effectuée aussi rapidement que possible, de sorte qu’elle n’entrave pas le démarrage du système d’exploitation.
    > [!Note]  
    > Si votre protocole EAP ne prend pas en charge l’authentification de l’ordinateur, il doit vérifier l’indicateur d’authentification de l’ordinateur, l’authentification de l’ordinateur de l' **\_ \_ indicateur EAP \_ \_ RAS** utilisé dans le champ **fFlags** de l' [**\_ \_ entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)et retourner une erreur.

     

 

 




