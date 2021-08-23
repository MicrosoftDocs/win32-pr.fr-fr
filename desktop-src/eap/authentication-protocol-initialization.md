---
title: Initialisation du protocole d’authentification
description: La connexion sécurisée EAP est initialisée entre le client et le serveur de la même façon pour les clients RAS et sans fil (802.1 X).
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d53643718f747e1f39aaf68393f92a0577455041ec765ca19bea710f2c3aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984459"
---
# <a name="authentication-protocol-initialization"></a>Initialisation du protocole d’authentification

La connexion sécurisée EAP est initialisée entre le client et le serveur de la même façon pour les clients RAS et sans fil (802.1 X).

## <a name="client"></a>Client

Lorsque le client tente d’établir la connexion, le service d’authentification obtient les [informations d’identité](obtaining-identity-information.md) de l’utilisateur. Si la valeur NAMEDLG de l' **\_ \_ \_ appel \_ du valueName EAP RAS** est présente dans le registre pour ce protocole d’authentification et que cette valeur est définie à zéro, le service d’authentification appelle [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Cette fonction affiche généralement une interface utilisateur qui permet d’obtenir des informations d’identité d’un type spécifique au protocole d’authentification. par exemple, un certificat ou un ID numérique. Si le nom d' **appel d’accès distant \_ EAP \_ \_ \_ NAMEDLG** n’est pas présent ou est défini sur un, le service d’authentification affiche la boîte de dialogue nom d’utilisateur standard du système.

Une fois que le service d’authentification a obtenu les informations d’identité de l’utilisateur, il appelle l’implémentation de [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))par le protocole d’authentification. Cet appel permet au protocole d’authentification d’allouer et d’initialiser une mémoire tampon de travail que le service transmet lors des appels suivants à [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) et [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)). La mémoire tampon de travail est opaque pour le service et n’accède jamais au contenu de la mémoire tampon de travail. Si le protocole d’authentification crée une mémoire tampon de travail distincte pour chaque session EAP, la mémoire tampon de travail est session et thread-safe. Étant donné que le protocole d’authentification alloue la mémoire pour la mémoire tampon de travail, le protocole d’authentification doit également libérer cette mémoire à l’aide de la fonction [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) .

Dans l’appel à [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), le service passe également une [**structure \_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) qui contient des pointeurs vers les informations de configuration de la connexion, ainsi que les informations d’identité de l’utilisateur. Le service transmet toujours une valeur au membre **pszIdentity** de l' **\_ \_ entrée EAP PPP**. Toutefois, le membre **pszPassword** de [**l' \_ \_ entrée PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) peut avoir la **valeur null**.

Dans la [**structure \_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) , le membre **fAuthenticator** indique si le protocole d’authentification est appelé pour être authentifié (sur le client) ou en tant qu’authentificateur (sur le serveur).

## <a name="server"></a>Serveur

Sur le serveur, le membre **bInitialID** de [**l' \_ \_ entrée PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) spécifie l’ID que le serveur utilise pour le premier paquet EAP. Le serveur incrémente cet ID pour les paquets suivants.

De même, sur le serveur, le pointeur **pUserAttributes** dans l' [**\_ \_ entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) pointe vers un tableau d’attributs du type d' [**\_ \_ attribut \_ d’authentification RAS**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) . Il s’agit des attributs de l’utilisateur qui ont été obtenus à partir du client.

Si l’appel [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) retourne une valeur autre qu' **aucune \_ erreur**, la session est déconnectée. L’erreur renvoyée est enregistrée (sur le serveur) ou affichée à l’utilisateur (sur le client).

 

 