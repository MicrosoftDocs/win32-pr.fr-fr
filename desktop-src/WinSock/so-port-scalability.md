---
description: Active l’extensibilité de port local pour un Socket.
ms.assetid: c5142baf-9e2d-4c06-8719-9090fd2d9487
title: SO_PORT_SCALABILITY (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 925d6337bc5b9d4633117fc1d8e1b8db2657f31b91a9cce602702ceb67e7e92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993369"
---
# <a name="so_port_scalability"></a>\_ \_ l’évolutivité des ports

L’option de socket d' **\_ \_ extensibilité de port so** active l’évolutivité de port local pour un Socket.

<dl> <dt>

<span id="SO_PORT_SCALABILITY"></span><span id="so_port_scalability"></span>**\_ \_ l’évolutivité des ports**
</dt> <dd> <dl> <dt>

0x3006
</dt> <dt>



L’option de socket d' **\_ \_ extensibilité de port so** permet l’évolutivité de port local en permettant l’optimisation de l’allocation de port en allouant des ports génériques plusieurs fois pour différentes paires de ports d’adresse locale sur un ordinateur local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Remarque : sur les plateformes où \_ \_ l’évolutivité des ports et la \_ réutilisation \_ UNICASTPORT sont prises en charge, préférez utiliser \_ \_ UNICASTPORT.

Les environnements de serveur proxy présentent des problèmes d’évolutivité en raison de la disponibilité limitée du port local. Pour contourner ce cas, vous pouvez ajouter d’autres adresses IP à la machine. Toutefois, par défaut, les ports génériques utilisés avec la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) sont limités à la taille de la plage de ports dynamiques sur l’ordinateur local (jusqu’à 64 Ko de ports, mais généralement moins), quel que soit le nombre d’adresses IP sur l’ordinateur local. Pour contourner ce dysfonctionnement, l’application doit conserver son propre pool de ports avec la réservation de port ou à l’aide de l’heuristique.

pour éviter que chaque application nécessitant une évolutivité gère son propre pool de ports et qu’elle permet une plus grande évolutivité tout en conservant la compatibilité des applications, Windows Server 2008 a introduit l’option de socket d' **\_ \_ évolutivité de port** pour optimiser l’allocation de port générique. L’allocation de port est optimisée en permettant à une application d’allouer des ports génériques pour chaque paire adresse locale et port unique. Par conséquent, si un ordinateur local possède quatre adresses IP, il est possible d’allouer jusqu’à 256 K ports génériques (64 ports × 4 adresses IP) par des demandes de fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) de caractères génériques.

Lorsque l’option de socket d' **\_ \_ extensibilité de port so** est définie sur un socket et qu’un appel à la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) est effectué pour une adresse spécifiée et un port générique (le paramètre *Name* est défini avec une adresse spécifique et un port de 0), Winsock alloue un port pour l’adresse spécifiée. Cette allocation sera basée sur toutes les adresses IP et ports/par adresse possibles sur l’ordinateur local. Si un port générique est acquis à l’aide de l’option de mise à l' **\_ \_ échelle du port** , ce port ne peut pas être alloué par un autre socket sans l’option de mise à l' **\_ \_ échelle du port** . Cette restriction est en place afin d’éviter les problèmes de compatibilité descendante avec les applications qui supposent qu’un port local générique ne peut pas être réutilisé. Notez que cela signifie que les applications qui acquièrent un grand nombre de ports à l’aide de **pour \_ \_ l’évolutivité** des ports peuvent priver des applications héritées de ports. Si tous les ports éphémères disponibles ont été acquis pour au moins une adresse avec l' **\_ \_ évolutivité des ports** , aucune allocation de port générique n’est alors possible sans l’option de Socket.

Pour avoir un effet, l’option de mise à l' **\_ \_ échelle du port** doit être définie avant l’appel de la fonction de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) . Vous trouverez ci-dessous un exemple de l’utilisation de cette méthode sur un ordinateur avec deux adresses :

-   La fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) est appelée par un processus pour créer un Socket.
-   La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) est appelée pour activer l’option de socket de mise à l' **\_ \_ échelle du port,** sur le socket nouvellement créé.
-   La fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) est appelée pour effectuer une liaison sur l’une des adresses IP de l’ordinateur local et le port 0.
-   La fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) est ensuite appelée pour se connecter à une adresse IP distante. Le socket est utilisé par l’application en fonction des besoins.
-   Une fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) est appelée par le même processus (éventuellement un thread différent) pour créer un deuxième Socket.
-   La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) est appelée pour activer l’option de socket de mise à l' **\_ \_ échelle du port,** sur le second Socket nouvellement créé.
-   La fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) est appelée avec la deuxième adresse IP et le port 0 de l’ordinateur local. Même lorsque tous les ports ont été alloués précédemment, cet appel réussit, car plusieurs adresses IP sont disponibles sur l’ordinateur local et l’option de socket de mise à l' **\_ \_ échelle du port so** a été définie sur les deux sockets dans le même processus.
-   La fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) est ensuite appelée pour se connecter à une adresse IP distante. Le deuxième Socket est utilisé par l’application en fonction des besoins.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Ws2def. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Options de socket de socket SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**Options de socket**](socket-options.md)
</dt> </dl>

 

 




