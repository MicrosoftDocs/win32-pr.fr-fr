---
description: avant Windows Vista, vous avez créé un élément du panneau de configuration en créant un fichier .dll et en le nommant avec une extension de .cpl.
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: Utilisation de CPLApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196384"
---
# <a name="using-cplapplet"></a>Utilisation de CPLApplet

avant Windows Vista, vous avez créé un élément du panneau de configuration en créant un fichier .dll et en le nommant avec une extension de .cpl. Ce fichier a exporté la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) . ce schéma est toujours pris en charge dans Windows Vista et les versions ultérieures. il est abordé dans cette rubrique. Toutefois, les instructions pour les nouveaux éléments du panneau de configuration recommandent une approche plus simple avec l’élément du panneau de configuration créé comme un fichier de .exe qui utilise une disposition de workflow de tâche.

Lorsque le panneau de configuration charge un fichier .dll (ou .cpl), il appelle la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) pour obtenir des informations telles que le nombre d’éléments du panneau de configuration que le fichier héberge, ainsi que des informations sur chaque élément. Le panneau de configuration appelle également la fonction lorsque la fenêtre de l’élément est initialisée, ouverte ou fermée.

lorsque Windows charge pour la première fois l’élément du panneau de configuration, il récupère l’adresse de la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) et utilise ensuite cette adresse pour appeler la fonction et lui transmettre des messages. Il peut envoyer les messages suivants.



| Message                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DBLCLK cpl**](cpl-dblclk.md)           | Envoyé pour notifier à [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que l’utilisateur a choisi l’icône associée à un élément de panneau de configuration donné. **CPlApplet** doit afficher la boîte de dialogue pour l’élément spécifié et effectuer toutes les tâches spécifiées par l’utilisateur. Le paramètre **CPlApplet** *lParam1* est un entier qui représente l’index de base zéro de l’élément du panneau de configuration. Le *paramètre lParam2* est le pointeur **lpData** retourné dans la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) dans le message [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) . La valeur de retour est ignorée.                                                                |
| [**fermeture de CPL \_**](cpl-exit.md)               | envoyé après le dernier \_ message d’arrêt de CPL et immédiatement avant Windows utilise la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) pour libérer la DLL qui contient l’élément du panneau de configuration. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) doit libérer la mémoire restante et préparer la fermeture. La valeur de retour est ignorée.                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CPL \_ GETCOUNT**](cpl-getcount.md)       | Envoyé après le \_ message d’initialisation de CPL pour inviter [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) à retourner un nombre qui indique le nombre de sous-programmes qu’il prend en charge.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_init cpl**](cpl-init.md)               | Envoyé immédiatement après le chargement de la DLL qui contient l’élément du panneau de configuration. Le message invite [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) à effectuer des procédures d’initialisation, y compris l’allocation de mémoire.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Rechercher dans CPL \_**](cpl-inquire.md)         | Envoyé après le \_ message Cpl GETCOUNT pour inviter [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) à fournir des informations sur un sous-programme spécifié. La valeur *lParam1* est un entier qui représente l’index de base zéro du sous-programme sur les informations demandées. Le paramètre *lParam2* de **CPlApplet** pointe vers une structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . La valeur de retour est ignorée.                                                                                                                                                                                                                                                                                                    |
| [**\_NEWINQUIRE cpl**](cpl-newinquire.md)   | Envoyé après le \_ message Cpl GETCOUNT pour inviter [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) à fournir des informations sur un élément du panneau de configuration spécifié. La valeur *lParam1* est un entier qui représente l’index de base zéro du sous-programme sur les informations demandées. Le paramètre *lParam2* est un pointeur vers une structure [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . La \_ NEWINQUIRE de cpl doit normalement être ignorée. votre application doit traiter uniquement les \_ recherches de CPL sur les systèmes Windows 95, Microsoft Windows NT 4,0 et versions ultérieures, car les performances du panneau de configuration sont affectées par l’utilisation de cpl \_ NEWINQUIRE. Cela est dû au fait que les chaînes et les icônes retournées ne peuvent pas être mises en cache. La valeur de retour est ignorée. |
| [**CPL \_ Sélectionner**](cpl-select.md)           | Obsolète. les versions actuelles de Windows n’envoient pas ce message.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_STARTWPARMS cpl**](cpl-startwparms.md) | Envoyé pour notifier à [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que l’utilisateur a choisi l’icône associée à une boîte de dialogue donnée. **CPlApplet** doit afficher la boîte de dialogue correspondante et effectuer toutes les tâches spécifiées par l’utilisateur. Ce message est similaire à CPL \_ DBLCLK, mais il peut y avoir des informations supplémentaires. Le paramètre *lParam1* est le numéro d’élément du panneau de configuration et *LParam2* est un **LPCTSTR** à toute direction supplémentaire qui peut être nécessaire. Retourne la **valeur true** si ce message est géré ; Sinon, **false**. Ce message est valide pour la [version 5,00](versions.md) et les versions ultérieures de Shell32.dll.                                                                                         |
| [**arrêt de CPL \_**](cpl-stop.md)               | envoyé une fois pour chaque élément du panneau de configuration dans le fichier .cpl avant que Windows décharge l’extension du panneau de configuration. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) doit libérer toute mémoire associée au numéro d’élément fourni dans *lParam1*. Le paramètre *lParam2* est un pointeur **lpData** retourné dans la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) dans le message [**Cpl \_ inquire**](cpl-inquire.md) ou [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) . La valeur de retour est ignorée.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
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

 

 
