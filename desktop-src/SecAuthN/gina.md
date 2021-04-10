---
description: L’objectif d’une DLL GINA est de fournir une identification utilisateur personnalisable et des procédures d’authentification. Par défaut, GINA effectue cette opération en déléguant l’analyse des événements SAS à Winlogon, qui reçoit et traite les séquences de touches de sécurité + ALT + SUPPR (SASs).
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758266"
---
# <a name="gina"></a>GINA

La bibliothèque [*Gina*](/windows/desktop/SecGloss/g-gly) fonctionne dans le [*contexte*](/windows/desktop/SecGloss/c-gly) du processus [*Winlogon*](/windows/desktop/SecGloss/w-gly) et, par conséquent, la DLL GINA est chargée très tôt dans le processus de démarrage. La DLL GINA doit suivre les règles afin que l’intégrité du système soit maintenue, en particulier en ce qui concerne l’interaction avec l’utilisateur.

> [!Note]  
> Les DLL GINA sont ignorées dans Windows Vista.

 

L’utilisation la plus courante de GINA consiste à communiquer avec un périphérique externe tel qu’un [*lecteur*](/windows/desktop/SecGloss/r-gly)de carte à puce. Il est essentiel de définir le paramètre de démarrage du pilote de périphérique sur System (Winnt. h : SERVICE \_ System \_ Start) pour vous assurer que le pilote est chargé au moment de l’appel de Gina.

L’objectif d’une DLL GINA est de fournir une identification utilisateur personnalisable et des procédures d’authentification. Par défaut, GINA effectue cette opération en déléguant l’analyse des événements SAS à Winlogon, qui reçoit et traite les [*séquences*](/windows/desktop/SecGloss/s-gly) de touches de sécurité + ALT + SUPPR (SASS). Un GINA personnalisé est chargé de configurer lui-même de recevoir des événements SAS (autres que l’événement SAS CTRL + ALT + DEL par défaut) et de notifier Winlogon lorsque des événements SAS se produisent. Winlogon évalue son état pour déterminer ce qui est requis pour traiter la SAP de la GINA personnalisée. Ce traitement comprend généralement des appels aux fonctions de traitement SAS de la GINA.

Pour plus d’informations sur les fonctions d’exportation GINA spécifiques, consultez [fonctions d’exportation Gina](authentication-functions.md). Pour plus d’informations sur l’utilisation des structures GINA pour transmettre des informations, consultez [structures Gina](authentication-structures.md).



| Rubrique                                                                             | Description                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Chargement et exécution d’une DLL GINA](loading-and-running-a-gina-dll.md)<br/>   | Valeur de clé de Registre à modifier pour charger et exécuter une DLL GINA personnalisée.<br/> |
| [Génération et test d’une DLL GINA](building-and-testing-a-gina-dll.md)<br/> | Comment tester une DLL GINA.<br/>                                              |



 

 

