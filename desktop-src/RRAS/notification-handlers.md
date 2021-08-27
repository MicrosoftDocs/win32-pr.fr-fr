---
title: Gestionnaires de notification
description: Un appel de RasDial asynchrone doit spécifier un gestionnaire de notification.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7210072e0542eeb63e3de6116d61995ef2363ca7b43e7a9e2c309165c0e862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074029"
---
# <a name="notification-handlers"></a>Gestionnaires de notification

Un appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchrone doit spécifier un gestionnaire de notification. Au cours d’une opération de connexion asynchrone, le gestionnaire de connexions d’accès à distance utilise le gestionnaire de notifications pour informer le client RAS chaque fois que l’état de la [connexion](connection-states.md) change ou qu’une erreur se produit.

Les actions effectuées par un gestionnaire de notification peuvent être réparties dans les catégories suivantes :

-   [Gestion des erreurs](handling-ras-errors.md).
-   Fournir des commentaires à l’utilisateur lorsque l’opération de connexion continue à travers les différents États de connexion. Consultez [notifications d’information](informational-notifications.md).
-   Gestion des [États en pause](paused-states.md).
-   Signalement de l’application cliente RAS lorsque l’opération de connexion est terminée. Consultez [notifications de fin d’exécution](completion-notifications.md).

Il existe trois types de gestionnaires de notifications, chacun d’entre eux recevant les mêmes informations de base : l’état actuel de la connexion et un code d’erreur différent de zéro uniquement si une erreur s’est produite.



| Valeur                                | Définition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Prototype de fonction de rappel qui reçoit uniquement l’état de connexion actuel et les informations de code d’erreur.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Un prototype de fonction de rappel qui reçoit le handle de connexion **HRASCONN** et des informations d’erreur étendues en plus des informations de base. Le paramètre de handle de connexion rend [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) utile pour les applications clientes qui prennent en charge plusieurs opérations de connexion simultanées. Cela permet au client de spécifier la même fonction de rappel pour toutes les opérations et permet à la fonction de rappel de déterminer quelle connexion change d’État. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Fonction de rappel semblable à [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1). Toutefois, [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) a été amélioré pour prendre en charge les connexions à liaisons multiples.                                                                                                                                                                                                                                                                                                                             |
| Handle de fenêtre                        | Handle de fenêtre auquel RAS envoie les messages [**WM \_ RASDIALEVENT**](wm-rasdialevent.md) contenant l’état de connexion actuel et les informations de code d’erreur. utilisez cette méthode si votre code source doit être compatible avec les Windows 16 bits, car le Windows 16 bits ne prend pas en charge l’une des fonctions de rappel.                                                                                                                                                                            |



 

Le gestionnaire de connexions d’accès à distance interrompt l’opération de connexion jusqu’à ce que le gestionnaire de notification retourne. Pour cette raison, le gestionnaire doit retourner dès que possible, à moins qu’une erreur ne se soit produite.

La fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ne doit pas être appelée à partir d’un gestionnaire de notifications. Les autres fonctions d’accès à distance ( [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa), [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa), [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa), [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)et [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) peuvent être appelées à partir d’un gestionnaire.

 

 




