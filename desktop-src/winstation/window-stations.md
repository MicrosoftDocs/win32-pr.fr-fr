---
title: Stations Windows
description: Une station Windows contient un presse-papiers, une table Atom et un ou plusieurs objets de bureau. Chaque objet de station Windows est un objet sécurisable. Quand une station Windows est créée, elle est associée au processus appelant et assignée à la session active.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objets de station Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219708"
---
# <a name="window-stations"></a>Stations Windows

Une *station Windows* contient un presse-papiers, une table Atom et un ou plusieurs objets de [Bureau](desktops.md) . Chaque objet de station Windows est un objet sécurisable. Quand une station Windows est créée, elle est associée au processus appelant et assignée à la session active.

La *station Windows Interactive* est la seule station Windows qui peut afficher une interface utilisateur ou recevoir une entrée d’utilisateur. Elle est assignée à la session d’ouverture de session de l’utilisateur interactif et contient le clavier, la souris et le périphérique d’affichage. Elle est toujours nommée « WinSta0 ». Toutes les autres stations Windows ne sont pas interactives, ce qui signifie qu’elles ne peuvent pas afficher une interface utilisateur ni recevoir d’entrée d’utilisateur.

Lorsqu’un utilisateur se connecte à un ordinateur à l’aide de Services Bureau à distance, une session est démarrée pour l’utilisateur. Chaque session est associée à sa propre station de fenêtre interactive nommée « WinSta0 ». Pour plus d’informations, consultez [Bureau à distance des sessions](/windows/desktop/TermServ/terminal-services-sessions).

Pour plus d’informations sur les stations de Windows, consultez les rubriques suivantes :

-   [Station Windows et création de bureau](window-station-and-desktop-creation.md)
-   [Traiter la connexion à une station Windows](process-connection-to-a-window-station.md)
-   [Sécurité de station Windows et droits d’accès](window-station-security-and-access-rights.md)

 

 