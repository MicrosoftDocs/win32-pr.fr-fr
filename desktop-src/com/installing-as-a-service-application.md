---
title: Installation d’une application en tant que service
description: Installation d’une application en tant que service
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998890"
---
# <a name="installing-as-a-service-application"></a>Installation d’une application en tant que service

En plus de s’exécuter en tant qu’exécutable de serveur local (EXE), un objet COM peut également s’empaqueter lui-même pour s’exécuter en tant qu’application de service lorsqu’il est activé par un client local ou distant. Les services prennent en charge de nombreuses fonctionnalités d’administration intégrées, telles que le démarrage, l’arrêt, l’interruption et le redémarrage locaux et interface, ainsi que la possibilité d’établir le serveur à exécuter sous un [compte d’utilisateur](/windows/desktop/Services/service-user-accounts) et une [station Windows](/windows/desktop/winstation/window-stations)spécifiques.

Un objet écrit en tant que service est installé pour une utilisation par COM en établissant une valeur [LocalService](localservice.md) sous sa clé [AppID](appid-key.md) et en effectuant une installation de service standard.

Les classes peuvent également être configurées pour s’exécuter sous un compte d’utilisateur spécifique lorsqu’elles sont activées par un client distant sans être écrites en tant qu’application de service. Pour ce faire, la classe installe un nom d’utilisateur et un mot de passe à utiliser lorsque le SCM lance son processus serveur local.

Quand une classe est configurée de cette manière, les appels à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) avec ce CLSID échouent, sauf si le processus a été lancé par com pour le compte d’une demande d’activation réelle. En d’autres termes, les classes configurées pour s’exécuter en tant qu’utilisateur particulier peuvent ne pas être enregistrées sous une autre identité.

Le nom d’utilisateur est extrait de la valeur nommée [runas](runas.md) sous la clé AppID de la classe. Si le nom d’utilisateur est « utilisateur interactif », le code de la classe est exécuté dans le contexte de sécurité de l’utilisateur actuellement connecté et est connecté à la station Windows Interactive.

Dans le cas contraire, le mot de passe est récupéré à partir d’une partie cachée du Registre, accessible uniquement aux administrateurs de l’ordinateur et au système. Le nom d’utilisateur et le mot de passe sont ensuite utilisés pour créer une session de connexion dans laquelle le code de la classe est exécuté. Lorsqu’il est lancé de cette manière, le code de la classe s’exécute avec son propre bureau et sa propre station de travail et ne partage pas les handles de fenêtre, le presse-papiers ou d’autres éléments de l’interface utilisateur avec l’utilisateur interactif ou d’autres classes s’exécutant dans d’autres comptes d’utilisateur.

Un serveur inscrit avec **LocalService** ou **runas** peut inscrire un objet dans la table d’objets en cours d’exécution pour permettre à n’importe quel client de s’y connecter. Pour ce faire, l’appel du serveur à [**IRunningObjectTable :: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) doit définir l' \_ indicateur ROTFLAGS ALLOWANYCLIENT. Un paramètre de serveur doit avoir son nom d’exécutable dans la section AppID du Registre qui fait référence à l’AppID pour l’exécutable. Un serveur « Activate As Activator » (non inscrit comme **LocalService** ou **runas**) ne peut pas inscrire un objet avec cet indicateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription d’une classe lors de l’installation](registering-a-class-at-installation.md)
</dt> <dt>

[Inscription d’un serveur exécutable en cours d’exécution](registering-a-running-exe-server.md)
</dt> <dt>

[Inscription d’objets dans le ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Inscription automatique](self-registration.md)
</dt> </dl>

 

 