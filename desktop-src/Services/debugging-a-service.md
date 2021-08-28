---
description: Vous pouvez utiliser l’une des méthodes suivantes pour déboguer votre service.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Déboguer un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b79217e4c2e9fe9f17457693260e9041e303511d3805b3bd636622fcbabdf29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126439"
---
# <a name="debugging-a-service"></a>Déboguer un service

Vous pouvez utiliser l’une des méthodes suivantes pour déboguer votre service.

-   Utilisez votre débogueur pour déboguer le service pendant qu’il est en cours d’exécution. Tout d’abord, obtenez l’identificateur de processus (PID) du processus de service. Une fois que vous avez obtenu le PID, attachez-le au processus en cours d’exécution. Pour plus d’informations sur la syntaxe, consultez la documentation fournie avec votre débogueur.
-   Appelez la fonction [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) pour appeler le débogueur pour le débogage juste-à-temps.
-   Spécifiez un débogueur à utiliser lors du démarrage d’un programme. Pour ce faire, créez une clé nommée **Image File Execution Options** à l’emplacement de Registre suivant :

    **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion**

    Créez une sous-clé avec le même nom que votre service (par exemple, MYSERV.EXE). Pour cette sous-clé, ajoutez une valeur de type **reg \_ SZ**, **débogueur** nommé. Utilisez le chemin d’accès complet au débogueur comme valeur de chaîne. Dans l’applet services du panneau de configuration, sélectionnez votre service, cliquez sur **démarrage** , puis activez **autoriser le service à interagir avec le bureau**. Le service doit être un service interactif, sinon le débogueur ne peut pas s’exécuter sur le bureau par défaut. notez que cette technique n’est plus prise en charge à partir de Windows Vista, car tous les services sont exécutés dans une session réservée exclusivement aux services et ne prennent pas en charge l’affichage d’une interface utilisateur.

-   Utilisez [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) pour enregistrer des informations.

Pour déboguer le code d’initialisation d’un service à démarrage automatique, vous devez installer et exécuter temporairement le service en tant que service de démarrage à la demande.

Parfois, il peut être nécessaire d’exécuter un service en tant qu’application console à des fins de débogage. Dans ce scénario, la fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) retourne une **erreur \_ échec \_ de \_ \_ connexion du contrôleur de service**. Par conséquent, veillez à structurer votre code de façon à ce que le code propre au service ne soit pas appelé lorsque cette erreur est retournée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage d’une application de service](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Outils de débogage pour Windows](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
