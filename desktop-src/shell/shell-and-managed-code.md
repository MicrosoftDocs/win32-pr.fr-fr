---
description: Les extensions in-process sont chargées dans tous les processus qui les déclenchent.
title: Conseils pour l’implémentation des extensions de In-Process
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FE830DBF-3F18-453c-9A51-91E10559D0E8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e4dc9fd0573f3f98f0ec1110079f95f56a8c42e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953109"
---
# <a name="guidance-for-implementing-in-process-extensions"></a>Conseils pour l’implémentation des extensions de In-Process

Les extensions in-process sont chargées dans tous les processus qui les déclenchent. Par exemple, une extension d’espace de noms de Shell peut être chargée dans n’importe quel processus qui accède directement ou indirectement à l’espace de noms Shell. L’espace de noms Shell est utilisé par de nombreuses opérations de Shell, telles que l’affichage d’une boîte de dialogue de fichier commune, le lancement d’un document via son application associée ou l’obtention de l’icône utilisée pour représenter un fichier. Étant donné que les extensions in-process peuvent être chargées dans des processus arbitraires, vous devez veiller à ce qu’elles n’aient pas d’impact négatif sur l’application hôte ou sur d’autres extensions in-process.

L’un des éléments à prendre en compte est le *Common Language Runtime (CLR)*, également appelé *code managé* ou le *.NET Framework*. **Microsoft recommande d’écrire des extensions gérées dans le processus dans l’Explorateur Windows ou Windows Internet Explorer et ne les considère pas comme un scénario pris en charge.**

Cette rubrique décrit les facteurs à prendre en compte lorsque vous déterminez si un runtime autre que le CLR peut être utilisé par les extensions in-process. Java, Visual Basic, JavaScript/ECMAScript, Delphi et la bibliothèque Runtime C/C++ sont des exemples d’autres runtimes. Cette rubrique fournit également des raisons pour lesquelles le code managé n’est pas pris en charge dans les extensions in-process.

## <a name="version-conflicts"></a>Conflits de versions

Un conflit de version peut résulter d’un Runtime qui ne prend pas en charge le chargement de plusieurs versions du Runtime au sein d’un même processus. Les versions du CLR antérieures à la version 4,0 appartiennent à cette catégorie. Si le chargement d’une version d’un Runtime exclut le chargement d’autres versions du même Runtime, cela peut créer un conflit si l’application hôte ou une autre extension in-process utilise une version conflictuelle. Dans le cas d’un conflit de version avec une autre extension in-process, le conflit peut être difficile à reproduire, car l’échec nécessite les extensions conflictuelles appropriées et le mode d’échec dépend de l’ordre dans lequel les extensions conflictuelles sont chargées.

Prenons l’exemple d’une extension in-process écrite à l’aide d’une version du CLR antérieure à la version 4,0. Chaque application sur l’ordinateur qui utilise une boîte de dialogue d' **ouverture** de fichier peut éventuellement disposer du code managé de la boîte de dialogue et de sa dépendance CLR de surveillance chargée dans le processus de l’application. L’application ou l’extension qui est la première à charger une version pré-4,0 du CLR dans le processus de l’application restreint les versions du CLR qui peuvent être utilisées par la suite par ce processus. Si une application managée avec une boîte de dialogue **ouvrir** est générée sur une version conflictuelle du CLR, l’exécution de l’extension peut échouer et provoquer des erreurs dans l’application. À l’inverse, si l’extension est la première à être chargée dans un processus et qu’une version conflictuelle du code managé tente de se lancer après cela (peut-être une application managée ou une application en cours d’exécution charge le CLR à la demande), l’opération échoue. Pour l’utilisateur, il semble que certaines fonctionnalités de l’application cessent de fonctionner de façon aléatoire ou que l’application se bloque de façon mystérieuse.

Notez que les versions du CLR égales ou ultérieures à la version 4,0 ne sont généralement pas exposées au problème de versioning, car elles sont conçues pour coexister entre elles et avec la plupart des versions antérieures à 4,0 du CLR (à l’exception de la version 1,0, qui ne peut pas coexister avec d’autres versions). Toutefois, des problèmes autres que des conflits de versions peuvent survenir comme indiqué dans le reste de cette rubrique.

## <a name="performance-issues"></a>Problèmes de performance

Des problèmes de performances peuvent survenir avec les runtimes qui imposent une baisse significative des performances lorsqu’ils sont chargés dans un processus. La baisse des performances peut se présenter sous la forme de l’utilisation de la mémoire, de l’utilisation du processeur, du temps écoulé ou même de la consommation d’espace d’adressage. Le CLR, JavaScript/ECMAScript et Java sont connus comme étant des runtimes à fort impact. Étant donné que les extensions in-process peuvent être chargées dans de nombreux processus et sont souvent effectuées à des moments sensibles aux performances (par exemple, lors de la préparation d’un menu à afficher à l’utilisateur), les runtimes à fort impact peuvent avoir un impact négatif sur la réactivité globale.

Un runtime à fort impact qui consomme des ressources significatives peut provoquer un échec dans le processus hôte ou une autre extension in-process. Par exemple, un runtime à fort impact qui consomme des centaines de mégaoctets d’espace d’adressage pour son tas peut entraîner l’incapacité de l’application hôte à charger un jeu de données volumineux. En outre, étant donné que les extensions in-process peuvent être chargées dans plusieurs processus, une consommation élevée de ressources dans une seule extension peut rapidement augmenter la consommation de ressources élevée sur l’ensemble du système.

Si un Runtime reste chargé ou continue à consommer des ressources même lorsque l’extension qui utilise ce runtime a été déchargée, ce Runtime ne peut pas être utilisé dans une extension.

## <a name="issues-specific-to-the-net-framework"></a>Problèmes spécifiques au .NET Framework

Les sections suivantes présentent des exemples de problèmes rencontrés avec l’utilisation du code managé pour les extensions. Il ne s’agit pas d’une liste complète de tous les problèmes que vous pouvez rencontrer. Les problèmes abordés ici sont les deux raisons pour lesquelles le code managé n’est pas pris en charge dans les extensions et les points à prendre en compte lorsque vous évaluez l’utilisation d’autres runtimes.

### <a name="re-entrancy"></a>Réentrance

Quand le CLR bloque un thread cloisonné (STA, Single-Threaded Apartment), par exemple en raison d’une instruction Monitor. Enter, WaitHandle. WaitOne ou d’une instruction [**Lock**](https://msdn.microsoft.com/library/c5kehkcz(v=VS.71).aspx) , le CLR, dans sa configuration standard, entre dans une boucle de messages imbriquée pendant qu’il attend. De nombreuses méthodes d’extension ne sont pas autorisées à traiter des messages, et cette réentrance imprévisible et inattendue peut entraîner un comportement anormal, difficile à reproduire et à diagnostiquer.

### <a name="the-multithreaded-apartment"></a>Le cloisonnement multithread

Le CLR crée des *wrappers pouvant être appelés* par le runtime pour les objets COM (Component Object Model). Ces mêmes wrappers pouvant être appelés par le runtime sont détruits ultérieurement par le finaliseur du CLR, qui fait partie du cloisonnement multithread (MTA). Le déplacement du proxy du STA vers le MTA nécessite un marshaling, mais toutes les interfaces utilisées par les extensions ne peuvent pas être marshalées.

### <a name="non-deterministic-object-lifetimes"></a>Durées de vie des objets non déterministes

Le CLR offre des garanties de durée de vie d’objet plus faibles que le code natif. De nombreuses extensions ont des exigences de nombre de références sur les objets et les interfaces, et le modèle de garbage collection utilisé par le CLR ne peut pas répondre à ces exigences.

-   Si un objet CLR obtient une référence à un objet COM, la référence d’objet COM détenue par le wrapper pouvant être appelé par le runtime n’est pas libérée tant que le wrapper pouvant être appelé par le runtime n’est pas récupéré par le garbage collector. Le comportement de la version non déterministe peut être en conflit avec certains contrats d’interface. Par exemple, la méthode [**IPersistPropertyBag :: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768206(v=vs.85)) exige qu’aucune référence au conteneur de propriétés ne soit conservée par l’objet lorsque la méthode **Load** est retournée.
-   Si une référence d’objet CLR est retournée en code natif, le wrapper [**pouvant être appelé**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) par le runtime abandonne sa référence à l’objet CLR lorsque l’appel final du wrapper Runtime Callable est effectué, mais l’objet CLR sous-jacent n’est pas finalisé tant qu’il n’est pas récupéré par le garbage collector. La finalisation non déterministe peut entrer en conflit avec certains contrats d’interface. Par exemple, les gestionnaires de miniatures sont requis pour libérer toutes les ressources immédiatement lorsque leur nombre de références est inférieur à zéro.

## <a name="acceptable-uses-of-managed-code-and-other-runtimes"></a>Utilisations acceptables du code managé et d’autres runtimes

Il est acceptable d’utiliser du code managé et d’autres runtimes pour implémenter des extensions hors processus. Voici quelques exemples d’extensions de Shell out-of-process :

-   Gestionnaires d’aperçus
-   Actions basées sur la ligne de commande, telles que celles enregistrées sous les sous-clés de commande de \\ *verbe* de Shell \\  .
-   Objets COM implémentés dans un serveur local, pour les points d’extension du shell qui autorisent l’activation hors processus.

Certaines extensions peuvent être implémentées en tant qu’extensions in-process ou out-of-process. Vous pouvez implémenter ces extensions en tant qu’extensions hors processus si elles ne répondent pas à ces exigences pour les extensions in-process. La liste suivante présente des exemples d’extensions qui peuvent être implémentées en tant qu’extensions in-process ou out-of-process :

-   [**IExecuteCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexecutecommand) associé à une entrée **DelegateExecute** inscrite sous une  \\  \\ sous-clé de **commande** de verbe de Shell.
-   [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) associé au CLSID inscrit sous une  \\  \\ sous-clé **dropTarget** de verbe de Shell.
-   [**IExplorerCommandState**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) associé à une entrée **CommandStateHandler** inscrite sous une \\ sous-clé de *verbe* de Shell.

 

 
