---
description: En règle générale, les services sont des applications console conçues pour s’exécuter sans assistance sans interface utilisateur graphique (GUI).
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Services interactifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6b99eb41d26d6740a30a314654d92fdd4522f5597ea6e4cbb2a3d443de8120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889467"
---
# <a name="interactive-services"></a>Services interactifs

En règle générale, les services sont des applications console conçues pour s’exécuter sans assistance sans interface utilisateur graphique (GUI). Toutefois, certains services peuvent nécessiter une interaction occasionnelle avec un utilisateur. Cette page présente les meilleures façons d’interagir avec l’utilisateur à partir d’un service.

> [!IMPORTANT]
> les Services ne peuvent pas interagir directement avec un utilisateur à partir de Windows Vista. Par conséquent, les techniques mentionnées dans la section intitulée utilisation d’un service interactif ne doivent pas être utilisées dans le nouveau code.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Interaction indirecte avec un utilisateur à partir d’un service

Vous pouvez utiliser les techniques suivantes pour interagir avec l’utilisateur à partir d’un service sur toutes les versions de Windows prises en charge :

-   Affiche une boîte de dialogue dans la session de l’utilisateur à l’aide de la fonction [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) .
-   Créez une application GUI cachée distincte et utilisez la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour exécuter l’application dans le contexte de l’utilisateur interactif. Concevez l’application GUI pour communiquer avec le service par le biais d’une méthode de communication interprocessus (IPC), par exemple, canaux nommés. Le service communique avec l’application GUI pour lui indiquer quand afficher l’interface utilisateur graphique. L’application communique les résultats de l’interaction de l’utilisateur au service afin que le service puisse prendre les mesures appropriées. Notez que IPC peut exposer vos interfaces de service sur le réseau, sauf si vous utilisez une liste de contrôle d’accès (ACL) appropriée.

    si ce service s’exécute sur un système multi-utilisateur, ajoutez l’application à la clé suivante pour qu’elle soit exécutée dans chaque session : **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ run**. Si l’application utilise des canaux nommés pour IPC, le serveur peut faire la distinction entre plusieurs processus utilisateur en attribuant à chaque canal un nom unique basé sur l’ID de session.

la technique suivante est également disponible pour Windows Server 2003 et Windows XP :

-   Affichez une boîte de message en appelant la fonction [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) avec la **\_ \_ notification de service MB**. Cela est recommandé pour afficher des messages d’État simples. N’appelez pas **MessageBox** pendant l’initialisation du service ou à partir de la routine [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) , sauf si vous l’appelez à partir d’un thread distinct, afin de revenir en temps voulu au SCM.

## <a name="using-an-interactive-service"></a>Utilisation d’un service interactif

Par défaut, les services utilisent une [station Windows](/windows/desktop/winstation/window-stations) non interactive et ne peuvent pas interagir avec l’utilisateur. Toutefois, un *service interactif* peut afficher une interface utilisateur et recevoir une entrée d’utilisateur.

> [!Caution]  
> Les services qui s’exécutent dans un contexte de sécurité élevé, tel que le compte LocalSystem, ne doivent pas créer de fenêtre sur le bureau interactif, car toute autre application qui s’exécute sur le bureau interactif peut interagir avec cette fenêtre. Cela expose le service à toute application exécutée par un utilisateur connecté. En outre, les services qui s’exécutent en tant que LocalSystem ne doivent pas accéder au bureau interactif en appelant la fonction [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) ou [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) .

 

Pour créer un service interactif, procédez comme suit lors de l’appel de la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) :

1.  Spécifiez NULL pour le paramètre *lpServiceStartName* pour exécuter le service dans le contexte du [compte LocalSystem](localsystem-account.md).
2.  Spécifiez l’indicateur de **\_ \_ processus interactif du service** .

Pour déterminer si un service s’exécute en tant que service interactif, appelez la fonction [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) pour récupérer un handle vers la station Windows et la fonction [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) pour tester si la station Windows possède l' **attribut \_ visible wsf** .

Toutefois, Notez que la clé de Registre suivante contient une valeur, **NoInteractiveServices**, qui contrôle l’effet du \_ processus interactif de service \_ :

**HKEY \_ local \_ machine \\ SYSTEM \\ CurrentControlSet \\ contrôle \\ Windows**

La valeur de **NoInteractiveServices** par défaut est 1, ce qui signifie qu’aucun service n’est autorisé à s’exécuter de manière interactive, qu’il dispose ou non d’un **\_ \_ processus interactif de service**. Quand **NoInteractiveServices** a la valeur 0, les services avec **le \_ \_ processus interactif service** sont autorisés à s’exécuter de manière interactive.

**Windows 7, Windows server 2008 R2, Windows XP et Windows server 2003 :** La valeur de **NoInteractiveServices** est définie par défaut sur 0, ce qui signifie que les services avec **\_ \_ processus interactif de service** sont autorisés à s’exécuter de manière interactive. Quand **NoInteractiveServices** est défini sur une valeur différente de zéro, aucun service démarré par la suite n’est autorisé à s’exécuter de manière interactive, qu’il dispose ou non d’un **\_ \_ processus interactif de service**.

> [!IMPORTANT]
> Tous les services s’exécutent dans la session des services Terminal Server 0. Par conséquent, si un service interactif affiche une interface utilisateur, il n’est visible que par l’utilisateur qui s’est connecté à la session 0. Étant donné qu’il n’existe aucun moyen de garantir que l’utilisateur interactif est connecté à la session 0, ne configurez pas un service pour qu’il s’exécute en tant que service interactif sous Terminal Services ou sur un système qui prend en charge le changement rapide d’utilisateur (le changement rapide d’utilisateur est implémenté à l’aide des services Terminal Server).

 

 

 
