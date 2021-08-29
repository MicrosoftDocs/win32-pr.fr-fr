---
description: Erreurs de Server-Side
ms.assetid: ce8ddb52-237c-4d46-a088-9f592afadcd2
title: Erreurs de Server-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1522f1e4ca07a1a2bfc17273b331a7beb3efc67a8c3f9a90e925161949f694ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793429"
---
# <a name="server-side-errors"></a>Erreurs de Server-Side

L’écouteur et le joueur fonctionnent ensemble pour gérer les messages incohérents. Si une transaction en cours de lecture échoue, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) déplace le message d’entrée vers la file d’attente d’entrée. Le lecteur abandonne la transaction s’il reçoit un HRESULT d’échec du composant serveur ou s’il intercepte une exception. Si le problème persiste, l’écouteur peut effectuer une boucle en continu dans le modèle suivant :

-   Met le message en file d’attente
-   Instancie l’objet
-   Subit une restauration
-   Remet le message en haut de la file d’attente

Le service Queued Components gère cet échec en utilisant une série de files d’attente de nouvelles tentatives spécifiques à l’application. Créé lors de l’installation du composant, il existe sept files d’attente pour chaque application, comme suit :

1.  La file d’attente d’entrée normale. Le nom de cette file d’attente est le nom de l’application COM+. Il s’agit d’une file d’attente publique Message Queuing.

2.  Première file d’attente des nouvelles tentatives. Les messages sont déplacés ici si la transaction échoue à plusieurs reprises lors du traitement des messages à partir de la file d’attente d’entrée normale. Les messages de cette file d’attente sont traités au bout d’une minute. Un message peut être retenté trois fois sur cette file d’attente avant d’être déplacé vers l’arrière de la deuxième file d’attente des nouvelles tentatives. Cette file d’attente est nommée *applicationName* \_ 0. Cette file d’attente est une file d’attente de Message Queuing privée.

3.  Deuxième file d’attente des nouvelles tentatives. Les messages sont déplacés ici si la transaction échoue à plusieurs reprises lors du traitement des messages à partir de la file d’attente des premières tentatives. Les messages de cette file d’attente sont traités au bout de deux minutes. Un message peut être retenté trois fois sur cette file d’attente avant d’être déplacé vers l’arrière de la troisième file d’attente des nouvelles tentatives. Cette file d’attente est nommée *applicationName* \_ 1. Cette file d’attente est une file d’attente de Message Queuing privée.

4.  La troisième file d’attente des nouvelles tentatives. Les messages sont déplacés ici si la transaction échoue à plusieurs reprises lors du traitement des messages à partir de la seconde file d’attente des nouvelles tentatives. Les messages de cette file d’attente sont traités après quatre minutes. Un message peut être retenté trois fois sur cette file d’attente avant d’être déplacé vers l’arrière de la quatrième file d’attente des nouvelles tentatives. Cette file d’attente est nommée *applicationName* \_ 2. Cette file d’attente est une file d’attente de Message Queuing privée.

5.  La quatrième file d’attente des nouvelles tentatives. Les messages sont déplacés ici si la transaction échoue à plusieurs reprises lors du traitement des messages à partir de la file d’attente des trois nouvelles tentatives. Les messages de cette file d’attente sont traités au bout de huit minutes. Un message peut être retenté trois fois sur cette file d’attente avant d’être déplacé vers la cinquième file d’attente des nouvelles tentatives. Cette file d’attente est nommée *applicationName* \_ 3. Cette file d’attente est une file d’attente de Message Queuing privée.

6.  Cinquième file d’attente des nouvelles tentatives. Les messages sont déplacés ici si la transaction échoue à plusieurs reprises lors du traitement des messages à partir de la file d’attente de la quatrième tentative. Les messages de cette file d’attente sont traités après seize minutes. Un message peut être retenté trois fois sur cette file d’attente avant d’être déplacé vers la file d’attente Rest finale. Cette file d’attente est nommée *applicationName* \_ 4. Il s’agit d’une file d’attente de Message Queuing privée.

7.  Une file d’attente de repos finale propre à l’application. Les messages sont déplacés ici si la transaction est abandonnée à plusieurs reprises lors de la nouvelle file d’attente de nouvelles tentatives. Cette file d’attente est nommée *applicationName* \_ DeadQueue. Il s’agit d’une file d’attente de Message Queuing privée. La file d’attente Rest finale n’est pas desservie par un écouteur de file d’attente. Les messages restent ici jusqu’à ce qu’ils soient déplacés manuellement (par exemple, par l’utilitaire de déplacement de messages des composants en file d’attente) ou sont purgés par Message Queuing Explorer.

Les messages qui ne sont pas lisibles parce qu’il est clair que chaque nouvelle tentative échoue peut être déplacé directement vers la file d’attente de repos finale spécifique à l’application, sans passer par tous les niveaux de tentative.

Le lecteur émet un événement COM+ pour notifier les parties intéressées que les messages ne peuvent pas être lus. Les événements COM+ sont émis dans les situations suivantes :

-   Quand une transaction est abandonnée
-   Lors du déplacement d’un message d’une file d’attente à une autre
-   Lorsqu’un message est déposé dans la file d’attente Rest finale

Les messages peuvent être modifiés avant de passer d’une file d’attente à une autre. Le mécanisme de sécurité des composants en file d’attente COM+ autorise le déplacement d’un message vers les files d’attente de nouvelle tentative, puis sa réinsertion dans la file d’attente d’entrée initiale de l’application. Pour plus d’informations sur la sécurité des composants en file d’attente, consultez [sécurité des composants en file d'](queued-components-security.md)attente.

Les files d’attente de nouvelles tentatives sont créées avec la file d’attente principale de l’application lorsque celle-ci est marquée comme mise en file d’attente par l’outil d’administration Services de composants ou en utilisant les fonctions du kit de développement logiciel (SDK) d’administration COM+. Le service Queued Components offre une certaine flexibilité dans le mécanisme de nouvelle tentative en autorisant la suppression des files d’attente de nouvelles tentatives. Par exemple, si toutes les files d’attente de nouvelles tentatives sont supprimées, un message qui s’interrompt de façon permanente est déplacé directement de la file d’attente de l’application vers la file d’attente finale de repos propre à l’application. En supprimant une ou plusieurs des files d’attente des nouvelles tentatives, vous pouvez réduire le nombre et la longueur des nouvelles tentatives. Si les files d’attente sont supprimées de la séquence de nouvelles tentatives, le minutage des files d’attente restantes correspond à la position dans la séquence des files d’attente des nouvelles tentatives. Par exemple, si vous supprimez la file d’attente des nouvelles tentatives *applicationName* \_ 1, *applicationName* \_ 2 et *applicationName* \_ 3, les messages sur *applicationName* \_ 4 sont traités comme si la file d’attente était la deuxième file d’attente des nouvelles tentatives.

Le mécanisme de nouvelle tentative est conçu pour terminer un message si possible. Dans certains cas, il n’est pas possible que le message aboutisse. Par exemple, un client peut tenter de retirer de l’argent d’un compte qui ne dispose pas de fonds suffisants. Dans ces circonstances, vous pouvez gérer l’erreur de plusieurs façons, y compris les éléments suivants :

-   Générer un diagnostic et émettre un avertissement
-   Créer une transaction de compensation
-   Ignorer le problème et ignorer le message

Comme les défaillances persistantes côté client, le service de composants en file d’attente permet à une classe d’exception d’être associée à un composant. La classe d’exception est associée au composant à l’aide de l’onglet **avancé** de la page Propriétés du composant de l’outil d’administration Services de composants ou à l’aide des fonctions d’administration com+. La classe exception permet au développeur d’avoir le contrôle après qu’un message a été retenté et avant que ce message soit déplacé vers la file d’attente de repos finale spécifique à l’application. Pour plus d’informations sur la classe d’exception, consultez [échecs de Client-Side persistantes](persistent-client-side-failures.md).

Voici la séquence d’événements pour la gestion des exceptions côté serveur :

1.  Le message est déplacé via les files d’attente de nouvelles tentatives disponibles spécifiques à l’application.
2.  La dernière tentative sur la file d’attente de la dernière tentative échoue.
3.  Le temps d’exécution du service de composants en file d’attente récupère le composant cible à partir du message et vérifie la disponibilité d’une classe d’exception.
4.  Le runtime instancie la classe d’exception.
5.  Les requêtes Runtime [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) sur la classe d’exception.
6.  Le runtime appelle [**IPlaybackControl :: FinalServerRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalserverretry) dans la classe d’exception.
7.  Le runtime lit tous les appels de propriété et de méthode du message à la classe d’exception.
8.  Si les étapes 4 à 6 échouent, le runtime déplace le message vers la file d’attente de repos finale propre à l’application.

Si vous devez intervenir dans le processus décrit ci-dessus ou si vous devez déplacer un message incohérent hors de sa file d’attente Rest finale, utilisez l’utilitaire de déplacement de messages. Pour plus d’informations sur l’utilitaire de déplacement de messages, consultez [gestion des erreurs](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreurs côté client](client-side-errors.md)
</dt> <dt>

[Échecs de Client-Side persistant](persistent-client-side-failures.md)
</dt> </dl>

 

 



