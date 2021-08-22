---
title: Interaction du point d’accès et du protocole d’authentification pendant l’authentification
description: La fonction RasEapMakeMessage contrôle la majorité de l’interaction entre le protocole d’authentification et le point d’accès.
ms.assetid: edc128e0-3104-4df9-80f4-b2aebcfe1087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea18883225a2a34e592b73e0cdc93b019c1bf466124976f01851febb2a17d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117769"
---
# <a name="access-point-and-authentication-protocol-interaction-during-authentication"></a>Interaction du point d’accès et du protocole d’authentification pendant l’authentification

La fonction [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) contrôle la majorité de l’interaction entre le protocole d’authentification et le point d’accès. **RasEapMakeMessage** traite les paquets EAP entrants et crée des paquets EAP à transmettre à l’homologue distant. Il traite également les événements tels que les délais d’expiration et l’exécution de l’authentification.

Si un message est reçu de l’homologue distant, le service d’authentification AP appelle [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), en passant un pointeur vers le message reçu dans le paramètre *pReceivePacket* .

Si le service appelle [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) avec *PReceivePacket* défini sur **null**, le point d’accès est en cours de lancement de la boîte de dialogue avec le protocole d’authentification ou en demandant que le protocole renvoie le dernier paquet. Le protocole d’authentification doit déterminer l’action que le service prend en fonction de son état et du contexte du message.

Au retour de [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)), la valeur du membre **action** de la structure [**de \_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) indique l’action que le service d’authentification effectue, le cas échéant. Le membre **action** prend des valeurs du type énuméré de l' [**\_ \_ action EAP PPP**](/windows/desktop/api/Raseapif/ne-raseapif-ppp_eap_action) .

Si **action** est **EAPACTION \_ Send**, **EAPACTION \_ SendAndDone**, **EAPACTION \_ SendWithTimeout** ou **EAPACTION \_ SendWithTimeoutInteractive**, le service transmet le paquet désigné par le paramètre *pSendPacket* à l’homologue distant.

La valeur **EAPACTION \_ SendWithTimeout** permet d’obtenir un délai d’expiration, après quoi le service d’authentification suppose que le lien a été perdu et déconnecte la session.

La valeur **EAPACTION \_ SendWithTimeoutInteractive** permet d’effectuer un laps de temps infini. L’authentificateur doit utiliser cette valeur lors de l’entrée d’utilisateur sur le client. Ce délai permet à l’utilisateur d’effectuer une durée non spécifiée pour terminer l’entrée requise.

Si **action** est **EAPACTION \_ SendWithTimeout** ou **EAPACTION \_ SendWithTimeoutInteractive**, le protocole d’authentification doit définir le membre **dwIdExpected** de la structure de [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) sur l’identificateur du paquet suivant attendu de l’homologue distant. Même si le paquet suivant reçu de l’homologue correspond à cette valeur, le service d’authentification transmet le paquet au protocole d’authentification lors d’un appel ultérieur à [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). Le protocole d’authentification peut ignorer silencieusement le paquet en renvoyant simplement une **erreur de \_ \_ \_ paquet non valide PPP**. Si un paquet avec l’identificateur attendu n’est pas reçu dans le délai d’attente configuré, le service d’authentification appelle toujours **RasEapMakeMessage**. Dans ce cas, l’appel est effectué avec le paramètre *pReceivePacket* défini sur **null** pour indiquer que le paquet précédent doit être renvoyé.

Si le membre d' **action** est **EAPACTION \_ terminé** ou **EAPACTION \_ SendAndDone**, le service d’authentification examine le membre **dwAuthResultCode** de la [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Si **dwAuthResultCode** n’est pas une \_ erreur, l’authentification a réussi. Si **dwAuthResultCode** est une valeur autre qu’aucune \_ erreur, l’authentification a échoué. Le code d’erreur retourné pour le cas d’échec doit provenir de Raserror. h, Mprerror. h ou winerror. h. Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants :

-   ERREUR \_ aucune \_ autorisation de numérotation \_
-   ERREUR \_ passwd \_ expirée
-   compte d’erreur \_ \_ désactivé
-   \_ \_ heures d’ouverture de session limitées à l’erreur \_
-   ERREUR d' \_ authentification \_ interne

Dans le cas où l' **action** est **EAPACTION \_ effectuée** ou **EAPACTION \_ SendAndDone**, le membre **pUserAttributes** doit pointer vers des attributs qui remplacent les attributs du même type qui ont été transmis au serveur dans l’appel à [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

Le protocole d’authentification sur le serveur peut demander à ce que le service d’authentification appelle le fournisseur d’authentification actuel en retournant **EAPACTION \_ Authenticate** dans le membre **action** dans la [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output). Dans ce cas, le pointeur **pUserAttributes** dans **le \_ \_ résultat EAP PPP** pointe uniquement vers les attributs qui ont été générés par le protocole d’authentification sur le serveur. Elle n’inclut pas les attributs passés au serveur dans l’appel à [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Le fournisseur d’authentification n’a pas besoin de ces attributs initiaux, car les informations d’authentification se trouvent dans le message EAP lui-même et non dans un attribut RADIUS distinct. Lorsque le service d’authentification répond à l’action d’authentification **EAPACTION \_** , **pUserAttributes** dans l' [**\_ \_ entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), pointe vers tous les attributs générés pendant l’authentification. Ces attributs sont retournés au protocole d’authentification sur le client.

Si le protocole d’authentification utilise **EAPACTION \_ Authenticate**, le fournisseur d’authentification exécute PAP ou MD5-chap. cette méthode d’authentification ne peut être utilisée qu’avec des clients Windows.

Si le protocole d’authentification authentifie l’utilisateur sans s’appuyer sur un fournisseur d’authentification, le protocole n’a pas besoin de définir d' **action** pour l’authentification **EAPACTION \_**. Un exemple de ce cas de figure est EAP-Transport la sécurité de couche (TLS).

Le paquet de réussite EAP est un paquet non reconnu. Par conséquent, il peut être perdu et n’est pas renvoyé par le serveur. Si le service d’authentification sur le client reçoit un paquet NCP (Network Control Protocol), le service d’authentification côté serveur se poursuit comme si l’authentification était réussie. Cela est dû au fait que le serveur est passé à la phase NCP de PPP. En conséquence, le service d’authentification appelle [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) avec le membre **fSuccessPacketReceived** de la structure [**\_ \_ d’entrée EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) ayant la valeur **true**.

Au cours de la session d’authentification, le protocole d’authentification peut nécessiter une interaction directe avec l’utilisateur sur le client. Le fournisseur du protocole d’authentification peut fournir une interface utilisateur interactive à cet effet. Le protocole d’authentification peut demander que le service affiche l’interface utilisateur interactive en définissant les membres **fInvokeInteractiveUI**, **pUIContextData** et **dwSizeOfUIContextData** dans la structure de [**\_ \_ sortie EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) . Pour plus d’informations sur l’utilisation d’une interface utilisateur interactive, consultez [interface utilisateur interactive](interactive-user-interface.md).

Le protocole d’authentification doit afficher une interface utilisateur uniquement via le mécanisme décrit sous [interface utilisateur interactive](interactive-user-interface.md). Si le protocole d’authentification affiche lui-même l’interface utilisateur, le thread PPP se bloque jusqu’à ce que l’interface utilisateur soit fermée.

Si, au cours du processus d’authentification, [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) retourne une valeur autre qu' **aucune \_ erreur** ou une **erreur de \_ \_ \_ paquet PPP non valide**, la session est déconnectée et l’erreur est consignée (sur le serveur) ou affichée à l’utilisateur (sur le client).

 

 