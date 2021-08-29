---
title: Windows Opérations de mise en réseau
description: Une application peut utiliser les fonctions WNet pour parcourir, ajouter ou annuler des connexions réseau n’importe où dans la hiérarchie du réseau.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1763f7261dd17fa6f21355ef2f1de404c2b34ec13d6ad6e9769aee3be55283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760339"
---
# <a name="windows-networking-operations"></a>Windows Opérations de mise en réseau

Une application peut utiliser les fonctions WNet pour parcourir, ajouter ou annuler des connexions réseau n’importe où dans la hiérarchie du réseau.

Une *connexion permanente* est une connexion réseau que le système restaure automatiquement lorsque l’utilisateur ouvre une session. Vous pouvez appeler les fonctions [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (ou [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) et [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) pour contrôler si une connexion réseau est persistante d’une session à la suivante.

Pour rechercher le nom d’utilisateur par défaut ou le nom d’utilisateur utilisé pour établir une connexion réseau, appelez la fonction [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .

En plus d’appeler les fonctions WNet, un processus peut également utiliser des mailslots et des canaux nommés pour communiquer avec un autre processus. Pour plus d’informations, consultez les [mailslots](/windows/desktop/ipc/mailslots) et les [canaux](/windows/desktop/ipc/pipes).

 

 