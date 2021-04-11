---
title: Détails de l’implémentation EAP
description: Les points d’accès, tels que le service d’accès à distance (RAS), interagissent avec les implémentations EAP via l’utilisation d’appels de fonction qui doivent être exportés par la DLL EAP tierce.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314885"
---
# <a name="eap-implementation-details"></a>Détails de l’implémentation EAP

Les points d’accès, tels que le service d’accès à distance (RAS), interagissent avec les implémentations EAP via l’utilisation d’appels de fonction qui doivent être exportés par la DLL EAP tierce. En d’autres termes, EAP est une API de fournisseur, ce qui signifie que les plug-ins ou les dll implémentent du code pour devenir un fournisseur EAP, mais ne doivent pas appeler les API EAP elles-mêmes. Par exemple, un programmeur d’une DLL EAP crée du code pour une routine d’initialisation EAP et place ce code dans la fonction prédéfinie EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). Ensuite, au moment de l’exécution, le gestionnaire de connexions AP appelle la fonction **RasEapInitialize** , qui contient le code, pour initialiser l’implémentation EAP.

Les rubriques suivantes détaillent cette interaction :

-   [Initialisation du point d’accès du protocole EAP](ras-initialization-of-eap.md)
-   [Initialisation du protocole d’authentification](authentication-protocol-initialization.md)
-   [Interaction du protocole d’authentification et du point d’accès](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Fin de la session d’authentification](completion-of-the-authentication-session.md)

 

 