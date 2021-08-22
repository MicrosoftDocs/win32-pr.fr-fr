---
description: La fonction de rappel CPlApplet traite tous les messages envoyés à un élément du panneau de configuration par Windows. Les messages envoyés à la fonction sont dans un ordre spécifique. Par le même jeton, l’élément .cpl nécessite le traitement des messages d’une manière spécifique.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Traitement des messages du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e697c603b69790d17c4d6771666a1111fa6f968eb97a30256696921f133530d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719950"
---
# <a name="control-panel-message-processing"></a>Traitement des messages du panneau de configuration

La fonction de rappel [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite tous les messages envoyés à un élément du panneau de configuration par Windows. Les messages envoyés à la fonction sont dans un ordre spécifique. Par le même jeton, l’élément .cpl nécessite le traitement des messages d’une manière spécifique.

tout d’abord, la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) reçoit le \_ message d’initialisation CPL quand Windows charge pour la première fois l’élément du panneau de configuration. La fonction doit effectuer toute initialisation, telle que l’allocation de mémoire, et retourner une valeur différente de zéro. si **CPlApplet** ne peut pas terminer l’initialisation, il doit retourner zéro, en dirigeant Windows pour terminer la communication et libérer la DLL.

ensuite, si le message d’initialisation de cpl \_ a réussi, Windows envoie le \_ message cpl GETCOUNT. La fonction doit ensuite retourner le nombre d’éléments du panneau de configuration pris en charge par le fichier .dll.

La fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) reçoit alors un message \_ de recherche cpl et un \_ message NEWINQUIRE CPL pour chaque élément du panneau de configuration pris en charge par le fichier .dll. La fonction remplit une structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) avec des informations sur votre élément, telles que son nom, son icône et une chaîne descriptive. La plupart des applications doivent traiter le message de recherche de CPL \_ et ignorer le \_ message NEWINQUIRE cpl. le \_ message de recherche de CPL fournit des informations dans un format qui Windows peut être mis en cache, ce qui améliore considérablement les performances. Le \_ message NEWINQUIRE cpl est utilisé uniquement si vous devez modifier l’icône de l’élément ou afficher des chaînes en fonction de l’état de l’ordinateur. les éléments du panneau de configuration qui utilisent CPL \_ NEWINQUIRE sont introuvables par une recherche dans le menu **démarrer** dans Windows Vista, car ils s’appuient sur la mise en cache.

La fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) reçoit ensuite un \_ message DBLCLK Cpl comme une notification indiquant que l’utilisateur a choisi l’icône qui représente l’élément du panneau de configuration. La fonction peut recevoir ce message autant de fois que vous le souhaitez. Le message comprend l’identificateur d’élément et le pointeur **lpData** retourné dans la [**structure CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) lors de l’appel à [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md). La fonction doit afficher la boîte de dialogue correspondante et traiter l’entrée d’utilisateur suivante.

Outre CPL \_ DBLCLK, le \_ message Cpl STARTWPARMS peut être envoyé si un élément du panneau de configuration est appelé avec des paramètres d’entrée, par exemple à partir d’une invite de commandes ou d’un autre programme. Le message comprend l’identificateur d’élément avec la chaîne de paramètre supplémentaire.

Avant la fin de l’application de contrôle, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) reçoit le \_ message d’arrêt Cpl une fois pour chaque élément du panneau de configuration pris en charge par le fichier .dll. Le message comprend l’identificateur de l’élément du panneau de configuration et le pointeur **lpData** retournés dans la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) dans l’appel à [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md). La fonction doit libérer la mémoire qu’elle a allouée pour la boîte de dialogue spécifiée.

Après le dernier \_ message d’arrêt de cpl, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) reçoit un message de \_ sortie cpl. La fonction doit libérer toute la mémoire allouée restante et annuler l’inscription des classes de fenêtres privées qu’elle peut avoir inscrites. immédiatement après le retour de la fonction à partir de ce message, Windows libère l’élément du panneau de configuration en appelant la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Affectation des catégories du panneau de configuration](assigning-control-panel-categories.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> <dt>

[accès au panneau de configuration en Mode Coffre sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
