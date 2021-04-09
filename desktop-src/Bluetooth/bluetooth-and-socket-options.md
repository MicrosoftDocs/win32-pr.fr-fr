---
title: Bluetooth et options de socket
description: Bluetooth pour Windows prend en charge les options de socket suivantes.
ms.assetid: e2e305c2-e749-4566-8e24-c07a7a29c612
keywords:
- Bluetooth et options de Socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84040a98c3dae1fec292e4f0a7086f11d1ee546c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941080"
---
# <a name="bluetooth-and-socket-options"></a>Bluetooth et options de socket

Bluetooth pour Windows prend en charge les options de socket suivantes. Les options de socket sont définies et interrogées à l’aide des fonctions [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) et [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , respectivement. Toutes les options suivantes peuvent être utilisées avec la fonction **setsockopt** , mais seule l’option **SO de l' \_ \_ unité MTU de BTH** est disponible pour une utilisation avec la fonction **getsockopt** .

Les paramètres suivants sont requis pour l’utilisation des options de Socket Bluetooth :

-   Le paramètre *s* doit être un Socket Bluetooth.
-   Le paramètre de *niveau* doit être **sol \_ RFCOMM**.

## <a name="so_bth_authenticate"></a>par conséquent, \_ BTH \_ Authenticate

Pour les sockets déconnectés, l’authentification **\_ BTH de BTH \_** spécifie que l’authentification est requise pour que l’opération de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) ou d' [**acceptation**](/windows/desktop/api/winsock2/nf-winsock2-accept) se termine correctement. La définition de cette option de socket lance activement l’authentification lors de l’établissement de la connexion, si les deux périphériques Bluetooth n’ont pas été authentifiés précédemment. L’interface utilisateur pour l’échange de clé d’aide, si nécessaire, est fournie par le système d’exploitation en dehors du contexte de l’application.

Pour les connexions sortantes qui requièrent une authentification, l’opération de [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) échoue avec **WSAEACCES** si l’authentification échoue. En réponse, l’application peut inviter l’utilisateur à authentifier les deux périphériques Bluetooth avant la connexion.

Pour les connexions entrantes, la connexion est rejetée si l’authentification ne peut pas être établie et renvoie une erreur **WSAEHOSTDOWN** . Pour plus d’informations sur l’authentification des appareils Bluetooth, consultez [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Pour l’option de socket **\_ \_ authentification BTH so** , *OPTVAL* est un pointeur vers ulong BAuthenticate et doit avoir la **valeur true**; *optlen* est équivalent à « sizeof (ULONG) ».

**Windows XP avec SP2 : so \_ BTH \_ Authenticate** démarre l’authentification pour les sockets connectés et force l’authentification lors de la connexion pour les sockets non connectés. Pour les connexions entrantes, la connexion est rejetée si l’authentification ne peut pas être effectuée.

## <a name="so_bth_encrypt"></a>par conséquent, \_ BTH \_ Encrypt

Sur les sockets non connectés, l’option de socket de **\_ \_ chiffrement BTH** permet d’appliquer le chiffrement pour établir une connexion. Le chiffrement est disponible uniquement pour les connexions authentifiées. Pour les connexions entrantes, une connexion pour laquelle le chiffrement ne peut pas être établi est automatiquement rejetée et retourne **WSAEHOSTDOWN** comme erreur. Pour les connexions sortantes, la fonction [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) échoue avec **WSAEACCES** si le chiffrement ne peut pas être établi. En réponse, l’application peut inviter l’utilisateur à authentifier les deux périphériques Bluetooth avant la connexion. Pour plus d’informations sur l’authentification des appareils Bluetooth, consultez [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice).

Pour l' \_ option de \_ Socket de chiffrement BTH so, *optval* est un pointeur vers ulong **BEncrypt** et doit avoir la **valeur true**. *optlen* est équivalent à sizeof (ULONG).

**Windows XP avec SP2 :** Pour un socket qui est connecté et authentifié, par **conséquent, \_ BTH \_ Encrypt** démarre le chiffrement.

## <a name="so_bth_mtu"></a>SO \_ MTU de BTH \_

L’option de socket **\_ \_ MTU BTH** est une option avancée qui est principalement utilisée pour la validation. L’option SO de l’unité **\_ \_ MTU de BTH** obtient ou définit la valeur par défaut de RFCOMM MTU (unité de transmission maximale) pour la négociation de la connexion à une valeur différente de la valeur par défaut du protocole RFCOMM.

Étant donné que l’unité MTU RFCOMM est affectée par l’unité MTU L2CAP sous-jacente, et les valeurs minimales et maximales du protocole et de l’application, la valeur par défaut de cette option est uniquement un point de départ pour la négociation avec l’homologue distant, et l’unité MTU négociée finale est susceptible de varier par rapport à la valeur par défaut. **\_ \_** La définition de la valeur de la **\_ \_ MTU de la vue BTH** peut avoir un impact négatif sur le débit, et en tant que telle, toute modification doit être effectuée avec la connaissance du protocole Bluetooth sous-jacent.

L’option de socket **\_ \_ MTU BTH** peut être exécutée sur des sockets connectés, mais elle n’a aucun effet si la négociation est déjà terminée. Sa définition sur le socket d’écoute (serveur) n’a aucun effet.

La quantité de données qu’une application peut envoyer ou recevoir dans un seul appel de socket n’est pas affectée par l’unité de transmission (MTU). La MTU affecte uniquement la manière dont le fournisseur de services Windows Sockets sous-jacent segmente les paquets pour le transport. L’unité MTU proposée et la MTU en fin de négociation doivent être comprises entre **RFCOMM \_ Min \_ MTU** et **RFCOMM \_ \_ MTU Max**, comme défini dans le fichier d’en-tête Ws2bth. h.

Pour l’option de socket **\_ \_ MTU BTH** , *optval* est un pointeur vers l’unité MTU ulong ; *optlen* est équivalent à « sizeof (ULONG) ».

## <a name="so_bth_mtu_max"></a>Si \_ BTH \_ mtu \_ Max

L’option de socket maximale de l' **\_ \_ unité MTU \_ de BTH** est une option avancée utilisée principalement pour la validation. L’option de socket maximum **\_ \_ MTU MTU \_ Max** définit la valeur maximale de RFCOMM MTU (unité de transmission maximale) pour la négociation de la connexion. Les connexions avec une unité MTU RFCOMM supérieure ou égale à cette valeur échouent au cours du processus d’acceptation de la [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Alors que la définition de cette option de socket est autorisée pour un socket connecté, elle n’a aucun effet si la négociation est terminée. La définition de cette option de socket sur un socket d’écoute propage la valeur de toutes les connexions entrantes. La valeur MTU MAX doit être comprise entre **RFCOMM \_ Min \_ MTU** et **RFCOMM \_ Max \_ MTU**, comme défini dans le fichier d’en-tête Ws2bth. h.

Pour l’option de socket maximale de l' **\_ \_ unité MTU \_ de BTH** , *optval* est un pointeur vers l' \_ unité MTU maximale ulong ; *optlen* est équivalent à « sizeof (ULONG) ».

## <a name="so_bth_mtu_min"></a>SO \_ MTU de BTH \_ \_ min.

L’option de socket de l' **\_ unité de \_ transmission maximale \_ BTH** est une option avancée utilisée principalement pour la validation. L’option de socket de l’unité de transmission maximale **\_ BTH de BTH \_ \_** définit la MTU RFCOMM minimale (unité de transmission maximale) pour la négociation de la connexion. Les connexions avec une MTU RFCOMM inférieure à cette valeur échouent pendant le processus d’acceptation de la [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) / [](/windows/desktop/api/winsock2/nf-winsock2-accept) . Alors que la définition de cette option de socket est autorisée pour un socket connecté, elle n’a aucun effet si la négociation est terminée. La définition de cette option de socket sur un socket d’écoute propage la valeur de toutes les connexions entrantes.

Seul un socket d’écoute peut modifier la MTU vers le bas. par conséquent, si la valeur proposée par le socket de connexion est inférieure à la valeur définie pour **\_ BTH \_ mtu \_ min** sur le socket d’écoute, la connexion est refusée. La valeur MTU minimale doit être comprise entre **RFCOMM \_ Min \_ MTU** et **RFCOMM \_ \_ MTU Max**, comme défini dans le fichier d’en-tête Ws2bth. h.

Pour l’option de socket de l' \_ \_ unité de transmission maximale BTH \_ , *optval* est un pointeur vers ulong min \_ MTU ; *optlen* est équivalent à « sizeof (ULONG) ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)
</dt> <dt>

[**entre**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**accepter**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 