---
description: découvrez comment empêcher les blocages dans les applications Windows pour les plateformes Windows 7 et Windows Server 2008 R2.
ms.assetid: 698a046b-1934-49cd-a717-d61e7e1ec534
title: Prévention des blocages dans les applications Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a2d8fac95039f20c8c684c50138933c54750c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414549"
---
# <a name="preventing-hangs-in-windows-applications"></a>Prévention des blocages dans les applications Windows

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="description"></a>Description

**Blocages-perspective de l’utilisateur**

Les utilisateurs comme les applications réactives. Lorsqu’il clique sur un menu, il souhaite que l’application réagisse instantanément, même si elle est en train d’imprimer son travail. Lorsqu’ils enregistrent un long document dans leur traitement de texte préféré, ils souhaitent continuer à taper alors que le disque est toujours en cours de rotation. Les utilisateurs sont impatients plutôt rapidement lorsque l’application ne réagit pas en temps utile à leur entrée.

Un programmeur peut reconnaître de nombreuses raisons légitimes pour qu’une application ne puisse pas répondre instantanément aux entrées d’utilisateur. L’application peut être chargée de recalculer certaines données ou d’attendre la fin de l’exécution de l’e/s disque. Toutefois, à partir de la recherche des utilisateurs, nous savons que les utilisateurs sont mécontents et frustrés après quelques secondes d’inactivité. Après 5 secondes, ils tenteront de mettre fin à une application bloquée. À la suite des blocages, les blocages d’applications sont la source la plus courante de perturbation de l’utilisateur lors de l’utilisation d’applications Win32.

Il existe de nombreuses causes racines pour les blocages des applications, et non pas toutes les manifestes dans une interface utilisateur qui ne répond pas. Toutefois, une interface utilisateur qui ne répond pas est l’une des expériences de blocage les plus courantes, et ce scénario reçoit actuellement la prise en charge de système d’exploitation la plus courante pour la détection et la récupération. Windows détecte automatiquement, collecte les informations de débogage et met éventuellement fin à des applications bloquées ou les redémarre. Dans le cas contraire, l’utilisateur devra peut-être redémarrer l’ordinateur pour pouvoir récupérer une application bloquée.

**Blocages-perspective du système d’exploitation**

Quand une application (ou plus précisément, un thread) crée une fenêtre sur le bureau, elle entre dans un contrat implicite avec le Gestionnaire de fenêtrage (DWM) pour traiter les messages de fenêtre en temps opportun. Le DWM publie des messages (entrée clavier/souris et messages provenant d’autres fenêtres, ainsi que lui-même) dans la file d’attente de messages spécifique au thread. Le thread récupère et distribue ces messages par le biais de sa file d’attente de messages. Si le thread ne traite pas la file d’attente en appelant GetMessage (), les messages ne sont pas traités et la fenêtre se bloque : il ne peut ni redessiner, ni accepter d’entrée de la part de l’utilisateur. Le système d’exploitation détecte cet État en joignant un minuteur aux messages en attente dans la file d’attente de messages. Si un message n’a pas été récupéré dans un délai de 5 secondes, le DWM déclare que la fenêtre est bloquée. Vous pouvez interroger cet état de fenêtre particulier à l’aide de l’API IsHungAppWindow ().

La détection n’est que la première étape. À ce stade, l’utilisateur ne peut toujours pas mettre fin à l’application. le fait de cliquer sur le bouton X (fermer) se traduirait par un \_ message de fermeture WM, qui serait bloqué dans la file d’attente de messages comme n’importe quel autre message. Le Gestionnaire de fenêtrage aide à masquer et à remplacer en toute transparence la fenêtre bloquée par une copie « fantôme » affichant une image bitmap de la zone cliente précédente de la fenêtre d’origine (et ajoutant « ne pas répondre » à la barre de titre). Tant que le thread de la fenêtre d’origine ne récupère pas les messages, le DWM gère simultanément les deux fenêtres, mais permet à l’utilisateur d’interagir uniquement avec la copie fantôme. À l’aide de cette fenêtre fantôme, l’utilisateur peut uniquement déplacer, réduire et, plus important encore, fermer l’application qui ne répond pas, mais ne modifie pas son état interne.

L’expérience fantôme complète ressemble à ceci :

![capture d’écran montrant la boîte de dialogue « Bloc-notes ne répond pas ».](images/preventinghangs-ghostwindow.gif)

La Gestionnaire de fenêtrage effectue une dernière chose ; il s’intègre à Rapport d’erreurs Windows, permettant à l’utilisateur de fermer et éventuellement de redémarrer l’application, mais également de renvoyer des données de débogage précieuses à Microsoft. Vous pouvez obtenir ces données de blocage pour vos propres applications en vous inscrivant sur le site Web winqual.

Windows 7 a ajouté une nouvelle fonctionnalité à cette expérience. Le système d’exploitation analyse l’application bloquée et, dans certaines circonstances, donne à l’utilisateur la possibilité d’annuler une opération de blocage et de rendre l’application réactive. L’implémentation actuelle prend en charge l’annulation des appels de socket bloquants ; d’autres opérations seront annulées par l’utilisateur dans les versions ultérieures.

Pour intégrer votre application à l’expérience de récupération des blocages et tirer le meilleur parti des données disponibles, procédez comme suit :

-   Assurez-vous que votre application s’inscrit au redémarrage et à la récupération, ce qui rend le blocage aussi simple que possible pour l’utilisateur. Une application correctement inscrite peut redémarrer automatiquement avec la plupart de ses données non enregistrées intactes. Cela fonctionne pour les blocages d’application et les blocages.
-   Obtenir des informations sur la fréquence, ainsi que des données de débogage pour vos applications bloquées et bloquées à partir du site Web winqual. Vous pouvez utiliser ces informations même pendant votre version bêta pour améliorer votre code. pour obtenir une vue d’ensemble, consultez « présentation de Rapport d’erreurs Windows ».
-   Vous pouvez désactiver la fonctionnalité de ghosting dans votre application via un appel à DisableProcessWindowsGhosting (). Toutefois, cela empêche l’utilisateur moyen de fermer et redémarrer une application bloquée et se termine souvent par un redémarrage.

**Blocages-perspective développeur**

Le système d’exploitation définit le blocage d’une application en tant que thread d’interface utilisateur qui n’a pas traité de messages pendant au moins 5 secondes. Des bogues évidents provoquent des blocages, par exemple, un thread qui attend un événement qui n’est jamais signalé, et deux threads contenant chacun un verrou et tentant d’acquérir les autres. Vous pouvez corriger ces bogues sans trop d’efforts. Toutefois, de nombreux blocages ne sont pas si clairs. Oui, le thread d’interface utilisateur ne récupère pas les messages, mais il est également occupé à effectuer un autre travail « important », puis à revenir au traitement des messages.

Toutefois, l’utilisateur perçoit cela comme un bogue. La conception doit correspondre aux attentes de l’utilisateur. Si la conception de l’application entraîne une application qui ne répond pas, la conception devra changer. Enfin, ce qui est important, l’absence de réponse ne peut pas être corrigée comme un bogue de code. elle nécessite un travail initial au cours de la phase de conception. Essayer de répartir la base de code existante d’une application pour améliorer la réactivité de l’interface utilisateur est souvent trop cher. Les instructions de conception suivantes peuvent vous aider.

-   Faire de la réactivité de l’interface utilisateur une exigence de niveau supérieur ; l’utilisateur doit toujours maîtriser votre application
-   Assurez-vous que les utilisateurs peuvent annuler des opérations qui prennent plus d’une seconde à se terminer et/ou que les opérations peuvent se terminer en arrière-plan. fournir une interface utilisateur de progression appropriée, si nécessaire

![Capture d’écran montrant la boîte de dialogue « copie d’éléments ».](images/preventinghangs-progressbar.gif)

-   Met en file d’attente les opérations de longue durée ou de blocage en tant que tâches en arrière-plan (cela nécessite un mécanisme de messagerie bien pensé pour informer le thread d’interface utilisateur lorsque le travail est terminé)
-   Gardez le code pour les threads de l’interface utilisateur simple ; supprimer autant d’appels d’API bloquant que possible
-   Affiche les fenêtres et les boîtes de dialogue uniquement lorsqu’elles sont prêtes et entièrement opérationnelles. Si la boîte de dialogue doit afficher des informations qui nécessitent trop de ressources pour être calculées, affichez d’abord des informations génériques et mettez-les à jour à la volée lorsque davantage de données sont disponibles. la boîte de dialogue propriétés du dossier de Windows Explorer en est un bon exemple. Il doit afficher la taille totale du dossier, les informations qui ne sont pas immédiatement disponibles à partir du système de fichiers. La boîte de dialogue s’affiche immédiatement et le champ « taille » est mis à jour à partir d’un thread de travail :

![capture d’écran montrant la page « général » des propriétés de Windows dont le texte est « taille », « taille sur le disque » et « contient » le texte entouré d’un cercle.](images/preventinghangs-updatingdialog.gif)

Malheureusement, il n’existe aucun moyen simple de concevoir et d’écrire une application réactive. Windows ne fournit pas une infrastructure asynchrone simple qui permet une planification facile des opérations de blocage ou de longue durée. Les sections suivantes présentent quelques-unes des meilleures pratiques pour empêcher les blocages et mettre en évidence certains des pièges les plus courants.

## <a name="best-practices"></a>Bonnes pratiques

**Garder le thread d’interface utilisateur simple**

La responsabilité principale du thread d’interface utilisateur est de récupérer et de distribuer les messages. Tout autre type de travail présente le risque de suspendre les fenêtres détenues par ce thread.

**Ne**

-   Déplacer des algorithmes gourmands en ressources ou non liés qui entraînent des opérations de longue durée vers les threads de travail
-   Identifiez autant que possible les appels de fonctions bloquantes et essayez de les déplacer vers les threads de travail. toute fonction appelant dans une autre DLL doit être suspecte
-   Faites un effort supplémentaire pour supprimer toutes les e/s de fichier et les appels d’API réseau de votre thread de travail. Ces fonctions peuvent se bloquer pendant de nombreuses secondes si elles ne sont pas des minutes. Si vous devez effectuer n’importe quel type d’e/s dans le thread d’interface utilisateur, envisagez d’utiliser des e/s asynchrones
-   N’oubliez pas que votre thread d’interface utilisateur traite également tous les serveurs COM STA (Single-Threaded Apartment) hébergés par votre processus. Si vous effectuez un appel bloquant, ces serveurs COM ne répondront pas tant que vous n’aurez pas reservi la file d’attente de messages

**Ne pas:**

-   Attendre un objet de noyau (comme un événement ou un mutex) pendant plus d’un laps de temps. Si vous devez attendre, envisagez d’utiliser MsgWaitForMultipleObjects (), qui se débloquera à l’arrivée d’un nouveau message
-   Partagez la file d’attente de messages de fenêtre d’un thread avec un autre thread à l’aide de la fonction AttachThreadInput (). il est non seulement extrêmement difficile de synchroniser correctement l’accès à la file d’attente, mais également d’empêcher le système d’exploitation Windows de détecter correctement une fenêtre bloquée
-   Utilisez TerminateThread () sur l’un de vos threads de travail. L’arrêt d’un thread de cette manière ne lui permet pas de libérer des verrous ou des événements de signal et peut facilement entraîner des objets de synchronisation orphelins
-   Appelez un code inconnu de votre thread d’interface utilisateur. Cela est particulièrement vrai si votre application a un modèle d’extensibilité ; Il n’y a aucune garantie que le code tiers respecte vos instructions de réactivité
-   Effectuer tout type d’appel de diffusion en blocage ; SendMessage ( \_ diffusion HWND) vous place à la merci de chaque application mal écrite en cours d’exécution

**Implémenter des modèles asynchrones**

La suppression d’opérations de longue durée ou de blocage à partir du thread d’interface utilisateur requiert l’implémentation d’une infrastructure asynchrone qui permet de décharger ces opérations sur les threads de travail.

**Ne**

-   Utilisez des API de message de fenêtre asynchrones dans votre thread d’interface utilisateur, notamment en remplaçant SendMessage par l’un de ses homologues non bloquant : PostMessage, SendNotifyMessage ou SendMessageCallback
-   Utilisez les threads d’arrière-plan pour exécuter des tâches de longue durée ou de blocage. Utiliser la nouvelle API de pool de threads pour implémenter vos threads de travail
-   Assurez la prise en charge de l’annulation des tâches en arrière-plan de longue durée. Pour les opérations d’e/s bloquantes, utilisez l’annulation d’e/s, mais uniquement en dernier recours. Il n’est pas facile d’annuler l’opération « Right ».
-   Implémenter une conception asynchrone pour du code managé à l’aide du modèle IAsyncResult ou à l’aide d’événements

**Utiliser les verrous avec prudence**

Votre application ou DLL nécessite des verrous pour synchroniser l’accès à ses structures de données internes. L’utilisation de plusieurs verrous augmente le parallélisme et rend votre application plus réactive. Toutefois, l’utilisation de plusieurs verrous augmente également la possibilité d’acquérir ces verrous dans des ordres différents et de provoquer un blocage des threads. Si deux threads maintiennent chacun un verrou, puis essaient d’acquérir le verrou de l’autre thread, leurs opérations forment une attente circulaire qui bloque toute progression vers l’avant pour ces threads. Vous pouvez éviter ce blocage uniquement en vous assurant que tous les threads de l’application acquièrent toujours tous les verrous dans le même ordre. Toutefois, il n’est pas toujours facile d’acquérir des verrous dans l’ordre « Right ». Les composants logiciels peuvent être composés, mais les acquisitions de verrous ne le peuvent pas. Si votre code appelle un autre composant, les verrous de ce composant deviennent désormais partie intégrante de votre ordre de verrouillage implicite, même si vous n’avez aucune visibilité sur ces verrous.

Les choses sont encore plus difficiles, car les opérations de verrouillage incluent bien plus que les fonctions habituelles pour les sections critiques, les mutex et les autres verrous traditionnels. Tout appel bloquant qui traverse les limites de thread a des propriétés de synchronisation qui peuvent provoquer un interblocage. Le thread appelant effectue une opération avec la sémantique « Acquire » et ne peut pas se débloquer tant que le thread cible n’est pas appelé. Certaines fonctions User32 (par exemple, SendMessage), ainsi que de nombreux appels COM bloquants, appartiennent à cette catégorie.

Pire encore, le système d’exploitation a son propre verrou interne propre au processus qui est parfois conservé pendant l’exécution de votre code. Ce verrou est acquis lorsque les dll sont chargées dans le processus et est donc appelé « verrouillage du chargeur ». La fonction DllMain s’exécute toujours sous le verrou du chargeur. Si vous acquérez des verrous dans DllMain (et que vous ne le faites pas), vous devez faire en sorte que le chargeur verrouille la partie de votre ordre de verrouillage. L’appel de certaines API Win32 peut également acquérir le verrou du chargeur sur vos fonctions, telles que LoadLibraryEx, GetModuleHandle, et en particulier CoCreateInstance.

Pour regrouper tout cela, examinez l’exemple de code ci-dessous. Cette fonction acquiert plusieurs objets de synchronisation et définit implicitement un ordre de verrouillage, ce qui n’est pas nécessairement évident sur l’inspection des curseurs. Dans l’entrée de la fonction, le code acquiert une section critique et ne le libère pas jusqu’à la sortie de la fonction, ce qui en fait le nœud supérieur dans la hiérarchie des verrous. Le code appelle ensuite la fonction Win32 LoadIcon (), qui sous les couvertures peut appeler le chargeur du système d’exploitation pour charger ce fichier binaire. Cette opération permet d’acquérir le verrou du chargeur, qui devient également une partie de cette hiérarchie de verrous (Assurez-vous que la fonction DllMain n’acquiert pas le \_ verrou g cs). Le code appelle ensuite SendMessage (), une opération de blocage inter-threads, qui n’est pas retournée, sauf si le thread d’interface utilisateur répond. Encore une fois, assurez-vous que le thread d’interface utilisateur n’acquiert jamais g \_ cs.

```
bool foo::bar (char* buffer)  
{  
      EnterCriticalSection(&g_cs);  
      // Get 'new data' icon  
      this.m_Icon = LoadIcon(hInst, MAKEINTRESOURCE(5));  
      // Let UI thread know to update icon SendMessage(hWnd,WM_COMMAND,IDM_ICON,NULL);  
      this.m_Params = GetParams(buffer);  
      LeaveCriticalSection(&g_cs);
      return true;  
}  
```

En examinant ce code, il est évident que nous avons implicitement établi g \_ cs le verrou de niveau supérieur dans notre hiérarchie de verrous, même si nous voulions uniquement synchroniser l’accès aux variables de membre de classe.

**Ne**

-   Concevoir une hiérarchie de verrous et la respecter. Ajoutez tous les verrous nécessaires. Il existe beaucoup plus de primitives de synchronisation que simplement mutex et CriticalSections ; ils doivent tous être inclus. Inclure le verrou du chargeur dans votre hiérarchie si vous prenez des verrous dans DllMain ()
-   Acceptez le protocole de verrouillage avec vos dépendances. Tout code que votre application appelle ou qui peut appeler votre application doit partager la même hiérarchie de verrouillage
-   Les structures de données de verrouillage ne fonctionnent pas. Déplacez les acquisitions de verrous hors des points d’entrée de fonction et protégez uniquement l’accès aux données avec des verrous. Si moins de code fonctionne sous un verrou, il y a moins de risques de blocages
-   Analyser les acquisitions et les libérations de verrous dans votre code de gestion des erreurs. Souvent la hiérarchie de verrous si elle est oubliée lors d’une tentative de récupération après une condition d’erreur
-   Remplacer les verrous imbriqués par des compteurs de référence : ils ne peuvent pas se bloquer. Les éléments verrouillés individuellement dans les listes et les tables sont de bons candidats
-   Soyez prudent lors de l’attente d’un handle de thread à partir d’une DLL. Supposez toujours que votre code peut être appelé sous le verrou du chargeur. Il est préférable de faire référence à vos ressources et de laisser le thread de travail effectuer son propre nettoyage (puis utiliser FreeLibraryAndExitThread pour s’arrêter correctement)
-   Utiliser l’API traversée de chaîne d’attente si vous souhaitez diagnostiquer vos propres blocages

**Ne pas:**

-   Effectuez tout autre opération d’initialisation très simple dans votre fonction DllMain (). Pour plus d’informations, consultez fonction de rappel DllMain. En particulier, n’appelez pas LoadLibraryEx ou CoCreateInstance
-   Écrivez vos propres primitives de verrouillage. Le code de synchronisation personnalisé peut facilement introduire des bogues subtils dans votre base de code. Utilisez plutôt la sélection enrichie d’objets de synchronisation du système d’exploitation.
-   Effectuez n’importe quel travail dans les constructeurs et les destructeurs pour les variables globales, ils sont exécutés dans le cadre du verrouillage du chargeur

**Soyez vigilant avec les exceptions**

Les exceptions permettent de séparer le déroulement normal du programme et la gestion des erreurs. En raison de cette séparation, il peut être difficile de connaître l’état précis du programme avant l’exception, et le gestionnaire d’exceptions peut manquer des étapes essentielles pour restaurer un état valide. Cela est particulièrement vrai pour les acquisitions de verrous qui doivent être libérées dans le gestionnaire afin d’éviter les blocages futurs.

L’exemple de code ci-dessous illustre ce problème. L’accès illimité à la variable « buffer » entraîne parfois une violation d’accès (AV). Cette solution antivirus est interceptée par le gestionnaire d’exceptions natif, mais elle n’a aucun moyen simple de déterminer si la section critique a déjà été acquise au moment de l’exception (l’AV peut même avoir été placé quelque part dans le code EnterCriticalSection).

```
 BOOL bar (char* buffer)  
{  
   BOOL rc = FALSE;  
   __try {  
      EnterCriticalSection(&cs);  
      while (*buffer++ != '&') ;  
      rc = GetParams(buffer);  
      LeaveCriticalSection(&cs);  
   } __except (EXCEPTION_EXECUTE_HANDLER)  
   {  
      return FALSE;  
   } 
   return rc;  
}  
```

**Ne**

-   Supprimer les \_ \_ tentatives/ \_ \_ sauf si possible ; n’utilisez pas SetUnhandledExceptionFilter
-   Encapsulez vos verrous dans des \_ modèles de type PTR automatique personnalisés si vous utilisez des exceptions C++. Le verrou doit être libéré dans le destructeur. Pour les exceptions natives, les verrous sont libérés dans votre \_ \_ instruction finally
-   Faites attention au code s’exécutant dans un gestionnaire d’exceptions natif ; l’exception peut avoir divulgué de nombreux verrous, donc votre gestionnaire ne doit pas acquérir

**Ne pas:**

-   Gérez les exceptions natives si elles ne sont pas nécessaires ou requises par les API Win32. si vous utilisez des gestionnaires d’exceptions natifs pour la création de rapports ou la récupération de données après des défaillances catastrophiques, envisagez d’utiliser le mécanisme de système d’exploitation par défaut de Rapport d’erreurs Windows à la place
-   Utilisez des exceptions C++ avec n’importe quel type de code d’interface utilisateur (User32). une exception levée dans un rappel transite par des couches de code C fournies par le système d’exploitation. Ce code ne connaît pas les sémantiques de la désroll C++

## <a name="links-to-resources"></a>Liens vers les ressources

-   [Rapport d’erreurs Windows](../wer/windows-error-reporting.md)
-   [Conception asynchrone](https://msdn.microsoft.com/library/ms228969(v=VS.80).aspx)
-   [E/s asynchrones](../fileio/synchronous-and-asynchronous-i-o.md)
-   [**AttachThreadInput fonction)**](/windows/win32/api/winuser/nf-winuser-attachthreadinput)
-   [**\_classe PTR automatique**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [**DisableProcessWindowsGhosting fonction)**](/windows/win32/api/winuser/nf-winuser-disableprocesswindowsghosting)
-   [**Fonction de rappel DllMain**](../dlls/dllmain.md)
-   [Événements](https://msdn.microsoft.com/library/wewwczdw(v=VS.80).aspx)
-   [**Fonction GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
-   [Annulation d’e/s](../fileio/canceling-pending-i-o-operations.md)
-   [**IsHungAppWindow fonction)**](/windows/win32/api/winuser/nf-winuser-ishungappwindow)
-   [File d’attente de messages](../winmsg/using-messages-and-message-queues.md)
-   [**MsgWaitForMultipleObjects fonction)**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects)
-   [Nouvelle API de pool de threads](../procthread/thread-pool-api.md)
-   [**PostMessage, fonction**](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   [Redémarrage et récupération](../recovery/registering-for-application-restart.md)
-   [**SendMessageCallback fonction)**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)
-   [**SendNotifyMessage fonction)**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)
-   [Objets de synchronisation](../sync/about-synchronization.md)
-   [**Fonction TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)
-   [Rapport d’erreurs Windows](../wer/windows-error-reporting.md)
-   [Winqual](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

 

 
