---
description: MUI permet à vos applications de gérer les langues d’interface utilisateur de deux manières.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Gestion de la langue de l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224113"
---
# <a name="user-interface-language-management"></a>Gestion de la langue de l’interface utilisateur

MUI permet à vos applications de gérer les langues d’interface utilisateur de deux manières. Une application peut utiliser une approche simple de la gestion des langues en utilisant par défaut les paramètres de langue du système d’exploitation. L’application peut également prendre en charge ses propres langues que l’utilisateur peut sélectionner. L’API MUI permet également à votre application d’accéder directement aux langues et aux listes de langues prises en charge par le système d’exploitation et gérée par le chargeur de ressources. Le reste de cette rubrique définit les langues prises en charge par le système et le mécanisme de secours pour les langages.

## <a name="languages-maintained-by-the-operating-system"></a>Langues gérées par le système d’exploitation

### <a name="system-default-ui-languageinstall-language"></a>Langue de l’interface utilisateur par défaut du système/langue d’installation

La langue de l’interface utilisateur par défaut du système est la langue de la version localisée utilisée pour configurer Windows. Tous les menus, les boîtes de dialogue, les messages d’erreur et les fichiers d’aide sont représentés dans cette langue, sauf lorsque l’utilisateur sélectionne une autre langue.

sur Windows Vista et versions ultérieures, la langue de l’interface utilisateur par défaut du système est appelée « langue d’installation » et joue un rôle plus limité. Dans la plupart des cas, il est remplacé par les langues d’interface utilisateur préférées du système. Toutefois, dans certains contextes, il est utile de disposer d’une seule langue d’installation, toujours connue pour être entièrement prise en charge.

Aucune fonction MUI n’est disponible pour définir la langue de l’interface utilisateur par défaut du système. Pour récupérer cette langue, l’application peut appeler [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage).

### <a name="system-ui-language"></a>Langue de l’interface utilisateur système

Le système d’exploitation définit la langue de l’interface utilisateur du système en tant que langue de l’interface utilisateur qui peut être définie par un administrateur sous l’onglet **avancé** de la section Options régionales et linguistiques du panneau de configuration. Le système d’exploitation utilise cette langue si l’utilisateur actuel n’a pas défini de paramètres de langue spécifiques ou si aucun compte actif n’est connecté. La langue ne peut être modifiée que si plusieurs langues de l’interface utilisateur sont installées sur l’ordinateur.

> [!Note]  
> Le système d’exploitation doit être redémarré pour tous les utilisateurs et services afin de voir l’effet de la modification de la langue.

 

Aucune fonction MUI n’est disponible pour définir la langue de l’interface utilisateur système. pour récupérer cette valeur, une application ciblée sur Windows Vista et versions ultérieures peut appeler [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) et obtenir la première langue dans la liste des langues d’interface utilisateur préférées du système. les Applications ciblées sur les systèmes d’exploitation antérieurs à Windows Vista ne peuvent pas utiliser [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) et doivent reposer sur l’hypothèse que la langue de l’interface utilisateur système est toujours la même que la langue de l’interface utilisateur par défaut du système.

### <a name="user-ui-language"></a>Langue de l’interface utilisateur

La langue de l’interface utilisateur de l’utilisateur détermine la langue de l’interface utilisateur utilisée pour les menus, les boîtes de dialogue, les fichiers d’aide, etc. Il peut être défini par l’utilisateur actuel dans l’onglet **langue** de la section Options régionales et linguistiques du panneau de configuration. Cette langue ne peut être modifiée que si plusieurs langues de l’interface utilisateur sont installées sur l’ordinateur. Notez que l’utilisateur doit se déconnecter puis se reconnecter pour voir l’effet. par exemple, une entreprise multinationale souhaite déployer des Windows dans toutes ses filiales. la société crée une tâche d’installation globale, qui installe la version en langue anglaise de Windows sur tous les clients, quel que soit l’emplacement. En même temps, il installe des modules linguistiques spécifiques en fonction de l’unité d’organisation dont un ordinateur est membre. lorsque l’utilisateur ouvre une session pour la première fois sur un système d’exploitation nouvellement installé, Windows s’affiche sous la forme d’une version localisée.

sur Windows Vista et versions ultérieures, la langue de l’interface utilisateur de l’utilisateur est la première langue de la liste langues d’interface utilisateur préférées de l’utilisateur. Notez que les langues de secours peuvent être utilisées si des ressources particulières ne sont pas disponibles dans cette langue.

sur les systèmes d’exploitation antérieurs à Windows Vista, la langue de l’interface utilisateur de l’utilisateur est généralement identique à la langue de l’interface utilisateur par défaut du système. toutefois, pour Windows MUI, les deux langages peuvent être différents.

Pour récupérer la langue de l’interface utilisateur, une application peut appeler [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) ou [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages). L’application ne peut pas modifier la langue de l’interface utilisateur de l’utilisateur, car il n’existe aucune fonction pour la définir.

## <a name="language-lists-maintained-by-the-operating-system"></a>Listes de langues gérées par le système d’exploitation

### <a name="system-preferred-ui-languages-list"></a>Liste des langues de l’interface utilisateur par défaut du système

Le chargeur de ressources gère une liste de langues d’interface utilisateur par défaut du système. Cette liste contient des langues préférées par le système d’exploitation pour ses propres ressources, telles que des menus et des boîtes de dialogue, des messages, des fichiers INF et des fichiers d’aide. La liste est constituée de la langue de l’interface utilisateur par défaut du système et de la langue de l’interface utilisateur système, ainsi que de leurs secours. Une application peut récupérer les langues d’interface utilisateur par défaut du système en appelant [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages).

### <a name="user-preferred-ui-languages-list"></a>Liste des langues d’interface utilisateur préférées de l’utilisateur

Le chargeur de ressources utilise une liste de langues de l’interface utilisateur par défaut de l’utilisateur qui comprend les langues que l’utilisateur préfère. Le chargeur de ressources utilise des ressources correspondant aux langages de cette liste, le cas échéant, pour un thread d’application particulier. Ces langues sont prioritaires sur les préférences système. Pour récupérer les langues d’interface utilisateur préférées de l’utilisateur, votre application peut appeler [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages).

### <a name="process-preferred-ui-languages-list"></a>Traiter la liste des langues d’interface utilisateur préférées

sur Windows Vista et versions ultérieures, le chargeur de ressources gère une liste de langues d’interface utilisateur par défaut qui comprend jusqu’à cinq langues valides définies par un processus en cours d’exécution pour une application MUI. Les langages peuvent être définis par l’application avec un appel à [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages). L’application peut récupérer les langues en appelant [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages).

### <a name="thread-preferred-ui-languages-list"></a>Liste des langues de l’interface utilisateur préférée du thread

sur Windows Vista et versions ultérieures, le chargeur de ressources utilise une liste de langues de l’interface utilisateur préférée du thread qui se compose de cinq langues valides au maximum définies par un thread dans un processus en cours d’exécution pour une application MUI. Ces langues sont utilisées pour personnaliser les langues de l’interface utilisateur de l’application et les rendre différentes de la langue du système d’exploitation. La liste des langues de l’interface utilisateur préférée du thread est basée sur les langues d’interface utilisateur préférées de l’utilisateur, les langues d’interface utilisateur préférées du système et la langue de l’interface utilisateur par défaut du système.

Pour définir les langues d’interface utilisateur préférées du thread, l’application doit appeler [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Pour récupérer ces langues, l’application appelle [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages).

## <a name="neutral-language-representation"></a>Représentation de langue neutre

Une langue neutre est représentée en tant que langue seule, sans région ou paramètres régionaux. Par exemple, la représentation neutre de la langue anglaise (Canada), en-CA, est représentée sous la forme « en ». Même si une langue neutre n’est pas associée aux aspects d’une région ou de paramètres régionaux, vous pouvez l’associer à un ensemble de ressources. En règle générale, une ressource de langue neutre est basée sur l’utilisation dans la région la plus courante pour la langue.

À titre d’illustration, supposons que votre application MUI localise les ressources en langue allemande pour l’allemand (Suisse) représenté en tant que en-CH et en allemand (Autriche) représenté comme étant de-AT, tout en générant un ensemble complet de ressources pour l’allemand (Allemagne) représenté sous la forme de-DE. Vous devez prendre des décisions pour cette application en tenant compte des fichiers de ressources complets. Si l’application duplique les ressources de-DE en tant que ressources de langage neutre, elle doit fournir une langue de secours pour le chargeur de ressources. Si le chargeur ne trouve pas de fichier de ressources spécifique à un langage particulier pour la valeur de-CH ou pour la désactivation, il revient aux ressources « de » indépendantes du langage. Ces ressources sont probablement plus appropriées que les ressources pour une langue complètement différente, par exemple l’anglais (États-Unis), qui sont les seuls autres secours possibles.

Autre exemple : une application peut ne pas être localisée du tout pour la Belize. Toutefois, la prise en charge d’une préférence linguistique de l’anglais (Belize), représentée sous la forme en-via, permet à l’application de revenir à des ressources en « en ».

## <a name="language-fallback-in-the-resource-loader"></a>Langue de secours dans le chargeur de ressources

Windows Vista et versions ultérieures organisent les paramètres de langue de l’interface utilisateur dans une liste de langues de secours prétriée utilisée par le chargeur de ressources. Pour former la liste, le système d’exploitation combine plusieurs langues, dans l’ordre indiqué :

-   Les langues d’interface utilisateur préférées du thread, qui se composent du langage de l’interface utilisateur du thread et de sa forme neutre. Exemples : fr-FR pour français (France) et sa forme neutre « fr » et es-ES pour l’espagnol (Espagne) et sa forme neutre « es ».
-   Traitez les langues d’interface utilisateur préférées, qui consistent en une langue d’interface utilisateur de processus et sa forme neutre. Par exemple, de-de pour l’allemand (Allemagne) et sa forme neutre « de ».
-   Langue de l’interface utilisateur de l’utilisateur et sa forme neutre. Par exemple, ja-JP pour le japonais (Japon) et sa forme neutre « ja ».
-   Langue de l’interface utilisateur système et sa forme neutre. C’est le cas, par exemple, pour l’italien (Italie) et sa forme neutre « informatique ».
    > [!Note]  
    > Cette langue est incluse uniquement dans la liste de secours lorsque la langue de l’interface utilisateur de l’utilisateur n’est pas définie.

     

-   Langue de l’interface utilisateur par défaut du système et sa forme neutre. Par exemple, es-ES pour l’espagnol (Espagne) et sa forme neutre « es ».

L’exemple suivant montre la liste de secours fusionnée. Notez que la duplication des langues, par exemple es-ES et es, est éliminée. Étant donné que l’exemple affecte la valeur ja-JP à la langue de l’interface utilisateur, la langue de l’interface utilisateur du système n’apparaît pas dans la liste de secours fusionnée.

fr-FR, FR, es-ES, ES, de--de, de, ja-JP, ja

Lors du chargement de ressources pour une application MUI, le chargeur de ressources tente de sélectionner l’un des fichiers correspondant à la liste des langues de l’interface utilisateur préférée du thread pour le thread d’application en cours d’exécution. Si le chargeur de ressources ne peut pas trouver de correspondance directe entre une langue sélectionnée et la première ressource spécifique à la langue dans la liste de secours fusionnée, il vérifie les langues suivantes dans la liste jusqu’à ce qu’il trouve un secours acceptable.

Si le chargeur de ressources ne trouve aucun fichier dont il a besoin, il doit utiliser un langage de secours « correct ». Pour la technologie de ressources MUI, le chargeur de ressources détermine le langage de secours à partir des données de configuration de ressource fournies. Pour plus d’informations, consultez [gestion des ressources MUI](mui-resource-management.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de interface utilisateur multilingue](about-multilingual-user-interface.md)
</dt> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Terminologie NLS](nls-terminology.md)
</dt> </dl>

 

 



