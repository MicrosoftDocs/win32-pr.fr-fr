---
description: Types d’applications COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Types d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bf55f7c2f25c490f0806a7924d32c6cbf981e79b8461ba12fc0f95964691c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499669"
---
# <a name="types-of-com-applications"></a>Types d’applications COM+

Voici les quatre types de base d’applications COM+ :

-   **Applications serveur.** Une *application serveur* com+ s’exécute dans son propre processus. Les applications serveur peuvent prendre en charge tous les services COM+.
-   **Applications de bibliothèque.** Une *application de bibliothèque* com+ s’exécute dans le processus du client qui la crée. Plus précisément, les composants d’une application de bibliothèque sont toujours chargés dans le processus du créateur. Les applications de bibliothèque ne sont pas explicitement associées à un processus serveur. Ils peuvent utiliser la sécurité basée sur les rôles, mais ne prennent pas en charge l’accès à distance ou les composants en file d’attente.
-   **Proxys d’application.** Un *proxy d’application* est un ensemble de fichiers contenant des informations d’inscription permettant à un client d’accéder à distance à une application serveur. Lorsqu’il est exécuté sur un ordinateur client, un fichier de proxy d’application écrit les informations relatives à l’application serveur COM+, y compris les CLSID, les ProgID, les RemoteServerName et les informations de marshaling, sur l’ordinateur client. L’application serveur est ensuite accessible à distance à partir de l’ordinateur client.
-   **Applications préinstallées par com+**. COM+ comprend un ensemble d’applications préinstallées qui gèrent les fonctions internes. Les applications préinstallées sont répertoriées dans le dossier applications COM+ de l’outil d’administration Services de composants, mais elles ne peuvent pas être modifiées ou supprimées. Ces applications sont les suivantes :
    -   Utilitaires .NET
    -   Application Publisher contrôle de l’analyseur
    -   Explorateur COM+
    -   Écouteur de file d’attente de lettres mortes QC COM+
    -   Utilitaires COM+
    -   Applications de In-Process IIS
    -   Applications regroupées hors processus IIS
    -   Application système

## <a name="notes"></a>Notes

à partir de Windows Server 2003, il est possible d’exécuter des applications COM+ même si l’Application système est désactivée. Les applications COM+ seront exécutées, mais sans les services généralement fournis par l’application système. Ces services incluent l’utilisation de l’outil d’administration Services de composants et le suivi des événements système.

à partir de Windows Server 2003, la fonction d’authentification de l’Application système COM+ comprend également la valeur EOAC \_ DISABLE \_ AAA. Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée avec la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système. La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.

 

 
