---
description: Les éléments suivants peuvent affecter les installations de Windows Installer lors de l’utilisation d’un serveur Terminal Server. Les développeurs du programme d’installation doivent toujours vérifier que leur package Windows Installer s’installe comme prévu quand les utilisateurs utilisent également un serveur Terminal Server.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Utilisation de Windows Installer avec un Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d471fa19b4588a01a2730af44fa5e9d978d18859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484657"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Utilisation de Windows Installer avec un Terminal Server

Les éléments suivants peuvent affecter les installations de Windows Installer lors de l’utilisation d’un serveur Terminal Server. Les développeurs du programme d’installation doivent toujours vérifier que leur package Windows Installer s’installe comme prévu quand les utilisateurs utilisent également un serveur Terminal Server.

-   Sur les systèmes d’exploitation antérieurs à Windows Server 2008 et Windows Vista, la stratégie système [EnableAdminTSRemote](enableadmintsremote.md) doit être définie pour permettre aux administrateurs d’effectuer des installations dans la session cliente. À partir de Windows Server 2008 et Windows Vista, la stratégie EnableAdminTSRemote n’a plus aucun effet. Quel que soit son paramètre, les administrateurs et les non-administrateurs peuvent effectuer une installation dans la session cliente ou la session de la console. Les administrateurs et les non-administrateurs peuvent toujours effectuer des installations Windows Installer dans la session de la console.
-   Le Windows Installer empêche l’installation dans le contexte d' [installation](installation-context.md) par utilisateur si la[stratégie système](system-policy.md) [DisableUserInstalls](disableuserinstalls.md)est définie sur 1. Dans ce cas, le programme d’installation ignore toutes les applications inscrites en tant qu’utilisateur et recherche uniquement les applications inscrites en tant qu’ordinateur.
-   Lorsqu’un administrateur effectue une installation dans une session cliente d’un serveur Terminal Server hébergé dans Windows 2000, l’installation doit utiliser un chemin d’accès UNC et non une lettre de lecteur mappée.

Les développeurs doivent respecter les instructions suivantes lors du développement d’un composant Windows Installer qui peut être utilisé avec un serveur Terminal Server.

-   Écrire toutes les informations de Registre **HKCU** dans la partie du  \\ **logiciel** HKCU du Registre.
-   Le stockage des informations de configuration dans les fichiers INI n’est pas recommandé.
-   Écrire les informations par utilisateur dans le registre lorsque l’application est exécutée pour la première fois et non au moment de l’installation. Si vous devez écrire des informations par utilisateur dans le registre au moment de l’installation, séparez les informations par utilisateur et par ordinateur dans différents composants de Windows Installer. Créez le package de sorte que le programme d’installation ne tente pas de valider et de réparer les composants contenant des informations par utilisateur lors de l’installation de l’application.
-   Un package utilisé uniquement pour les installations par ordinateur doit écrire les variables d’environnement dans l’environnement de l’ordinateur en incluant \* dans la colonne nom de la [table d’environnement](environment-table.md). Si le package peut être utilisé pour des installations par utilisateur ou par ordinateur, utilisez deux composants. Incluez le composant pour chaque utilisateur dans la [table des composants](condition-table.md) et entrez les paramètres utilisateur dans la table d’environnement. Incluez le composant par ordinateur dans la table des composants et entrez les paramètres de l’ordinateur dans la table d’environnement. Contrôlez le composant qui est installé à l’aide d’instructions conditionnelles basées sur la propriété [**ALLUSERS**](allusers.md) dans le champ condition de la table des composants.
-   Lors de l’exécution d’installations par ordinateur à partir d’un serveur Terminal Server, le programme d’installation écrit les variables d’environnement par utilisateur dans **HKCU** \\ **. Environnement par défaut** \\ . Étant donné que le serveur Terminal Server ne réplique pas cette section du Registre, l’installation ne définit pas les variables d’environnement par utilisateur.
-   Étant donné qu’un serveur peut être configuré pour empêcher les utilisateurs de réparer des applications, votre application doit gérer le cas de clés de Registre manquantes normalement.

Les éléments suivants s’appliquent lorsqu’un package Windows Installer qui utilise des [actions personnalisées](custom-actions.md) dll, exe ou de script est installé dans le contexte d’installation par ordinateur sur un serveur Terminal Server. Dans ce cas, le programme d’installation définit la propriété [**TerminalServer**](terminalserver.md) .

-   Les actions personnalisées différées s’exécutent dans le contexte du système local, sauf si l’action a l’attribut **msidbCustomActionTypeTSAware** . Cela est vrai même si l’action personnalisée emprunte l’identité de l’utilisateur sur un système qui n’est pas un serveur Terminal Server. Notez que si une action personnalisée ayant l’attribut **msidbCustomActionTypeTSAware** modifie le registre de l’utilisateur, le programme d’installation ne vérifie pas automatiquement que ces modifications sont également apportées au registre de chaque utilisateur sur l’ordinateur.
-   Toutes les opérations du Registre dans une action personnalisée différée qui lisent à partir de la ruche du Registre **HKCU** voient la ruche du Registre par défaut du système et non la ruche du registre de l’utilisateur actuel.
-   Toutes les opérations du Registre dans une action personnalisée différée qui écrivent dans le \\ **logiciel** HKCU sont détectées par le programme d’installation et copiées sur chaque utilisateur de l’ordinateur à la prochaine ouverture de session de l’utilisateur.
-   Toutes les opérations de Registre dans une action personnalisée différée qui écrivent dans **HKCU**, mais qui ne sont pas sous la clé de Registre **HKCU** \\ **Software** , ne sont pas détectées par le programme d’installation ou copiées.

Pour plus d’informations, consultez [services Terminal Server](../termserv/terminal-services-portal.md) dans le kit de développement logiciel (SDK) Microsoft Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**Propriété TerminalServer**](terminalserver.md)
</dt> <dt>

[**Propriété RemoteAdminTS**](remoteadmints.md)
</dt> <dt>

[Terminal Services](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
