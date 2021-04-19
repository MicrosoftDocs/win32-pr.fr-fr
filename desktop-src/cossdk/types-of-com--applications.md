---
description: Types d’applications COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Types d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515787"
---
# <a name="types-of-com-applications"></a>Types d’applications COM+

Voici les quatre types de base d’applications COM+ :

-   **Applications serveur.** Une *application serveur* com+ s’exécute dans son propre processus. Les applications serveur peuvent prendre en charge tous les services COM+.
-   **Applications de bibliothèque.** Une *application de bibliothèque* com+ s’exécute dans le processus du client qui la crée. Plus précisément, les composants d’une application de bibliothèque sont toujours chargés dans le processus du créateur. Les applications de bibliothèque ne sont pas explicitement associées à un processus serveur. Ils peuvent utiliser la sécurité basée sur les rôles, mais ne prennent pas en charge l’accès à distance ou les composants en file d’attente.
-   **Proxys d’application.** Un *proxy d’application* est un ensemble de fichiers contenant des informations d’inscription permettant à un client d’accéder à distance à une application serveur. Lorsqu’il est exécuté sur un ordinateur client, un fichier de proxy d’application écrit les informations relatives à l’application serveur COM+, y compris les CLSID, les ProgID, les RemoteServerName et les informations de marshaling, sur l’ordinateur client. L’application serveur est ensuite accessible à distance à partir de l’ordinateur client.
-   **Applications préinstallées par com+**. COM+ comprend un ensemble d’applications préinstallées qui gèrent les fonctions internes. Les applications préinstallées sont répertoriées dans le dossier applications COM+ de l’outil d’administration Services de composants, mais elles ne peuvent pas être modifiées ou supprimées. Ces applications sont les suivantes :
    -   Utilitaires .NET
    -   Application de l’éditeur de contrôle de l’analyseur
    -   Explorateur COM+
    -   Écouteur de file d’attente de lettres mortes QC COM+
    -   Utilitaires COM+
    -   Applications de In-Process IIS
    -   Applications regroupées hors processus IIS
    -   Application système

## <a name="notes"></a>Notes

À compter de Windows Server 2003, il est possible d’exécuter des applications COM+ même si l’application système est désactivée. Les applications COM+ seront exécutées, mais sans les services généralement fournis par l’application système. Ces services incluent l’utilisation de l’outil d’administration Services de composants et le suivi des événements système.

À compter de Windows Server 2003, la fonctionnalité d’authentification de l’application système COM+ comprend également la valeur EOAC \_ Disable \_ AAA. Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée avec la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système. La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.

 

 
