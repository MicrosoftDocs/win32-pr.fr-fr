---
description: Les API InkAnalysis fournissent aux développeurs Tablet PC des outils puissants pour examiner l’entrée manuscrite par programmation. L’API classe l’encre dans des catégories significatives, telles que des mots, des lignes, des paragraphes et des dessins.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Présentation de l’analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3056a5e5fbff8be82f6df2de2a34fadd9761e50f451ee2d48c112589d1aff397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718911"
---
# <a name="ink-analysis-overview"></a>Présentation de l’analyse de l’encre

Les API InkAnalysis fournissent aux développeurs Tablet PC des outils puissants pour examiner l’entrée manuscrite par programmation. L’API classe l’encre dans des catégories significatives, telles que des mots, des lignes, des paragraphes et des dessins.

Vous pouvez utiliser chaque classification de plusieurs façons, y compris pour améliorer les résultats de la reconnaissance de l’écriture manuscrite.

## <a name="ink-analysis-basics"></a>Notions de base de l’analyse d’encre

Cette section présente la technologie d’analyse des encres de la plateforme Tablet PC et explique quand et comment l’utiliser.

Les API InkAnalysis combinent efficacement deux technologies distinctes mais complémentaires : la reconnaissance de l’écriture manuscrite et la classification de la disposition. La combinaison de ces deux technologies donne des résultats plus élevés que les parties.

La reconnaissance de l’écriture manuscrite est l’analyse de calcul de l’encre numérique manuscrite pour retourner une interprétation basée sur des caractères dans une langue donnée. Autrement dit, la reconnaissance de l’écriture manuscrite indique comment l’ordinateur lit l’écriture manuscrite d’une personne.

L’analyse de l’encre peut être divisée en une classification de l’encre et une analyse de la disposition. La classification d’encre est la Division de calcul de l’encre en unités sémantiquement significatives, telles que les paragraphes, les lignes, les mots et les dessins. L’analyse de la disposition est l’examen de calcul de l’entrée d’encre pour déterminer la position de l’encre sur la surface d’encrage et la façon dont les traits sont liés l’un à l’autre de manière spatiale et même sémantique. Par exemple, l’analyse de la disposition peut vous indiquer qu’un élément d’encre particulier est une annotation ou un appel.

### <a name="recognition"></a>Reconnaissance

Un exemple de la façon dont la combinaison de reconnaissance avec l’analyse d’encre dans l’API InkAnalysis permet au développeur d’améliorer les résultats de la reconnaissance. Les moteurs de reconnaissance de l’écriture manuscrite Tablet PC ont été principalement conçus pour reconnaître une seule ligne horizontale d’encre. Toutefois, les gens ont tendance à écrire plusieurs lignes lorsqu’ils prennent des notes, et il n’est pas garanti que ces lignes soient horizontales par rapport à la page. Avec l’API InkAnalysis, l’encre est prétraitée par l’analyseur d’encre avant d’être envoyée au module de reconnaissance. L’encre analysée est transformée en horizontale avant d’être reconnue, ce qui améliore les résultats de la reconnaissance.

Les autres avantages à la reconnaissance sont dérivés en faisant en sorte que l’analyseur d’encre corrige les informations d’ordre de trait incorrectes avant d’envoyer l’encre au module de reconnaissance. En outre, les résultats de la reconnaissance sont à présent disponibles de manière sélective. Autrement dit, le développeur peut rapidement récupérer les résultats de la reconnaissance pour un mot, une ligne ou un paragraphe unique dans un appel.

### <a name="ink-classification"></a>Classification d’encre

Il existe, bien sûr, un grand nombre de scénarios dans lesquels vous pouvez conserver les données d’encre intactes, plutôt que de les convertir immédiatement en texte. L’analyse de l’encre offre également des avantages. Plus précisément, les API InkAnalysis offrent la possibilité de fractionner les traits d’encre selon qu’ils écrivent ou dessinent. Les traits d’encre classés comme écrits sont ceux qui composent un mot ou des caractères. Tous les autres traits sont des dessins. Vous disposez ainsi d’une nouvelle façon d’accéder aux données manuscrites, ce qui permet de créer de nouveaux scénarios utilisateur. Par exemple, vous pouvez implémenter la sélection de sorte qu’elle soit différente selon le type de trait sur lequel l’utilisateur appuie ; Si un utilisateur appuie sur un trait d’écriture, l’application sélectionne tout le jeu de traits qui composent le mot, si l’utilisateur appuie sur un des de dessin, l’application sélectionne uniquement ce trait.

### <a name="layout-analysis"></a>Analyse de la disposition

L’analyse de la disposition utile va bien au-delà de la répartition relativement simple de l’encre en composants d’écriture et de dessin.

L’analyse de l’encre comprend également une décomposition plus détaillée des traits d’écriture et de dessin. À titre d’exemple très simple, prenez un blob d’encre comme indiqué dans l’illustration suivante.

![deux simples lignes d’écriture manuscrite](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Une fois que la plateforme a analysé ces traits, elle retourne une représentation sous forme d’arborescence de ces traits, comme indiqué dans l’illustration suivante. Pour ce cas simple, l’arborescence contient uniquement des informations sur les paragraphes, les lignes et les mots, mais la richesse de cette arborescence augmente à mesure que la complexité du document manuscrit augmente.

![représentation sous forme d’arborescence de la racine, du paragraphe, des lignes et des mots](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Étant donné que ces informations sont maintenant séparées en unités gérables, vous pouvez désormais créer des fonctionnalités plus puissantes. Par exemple, l’application peut étendre la fonctionnalité dans laquelle l’utilisateur appuie pour sélectionner un mot dans une fonctionnalité dans laquelle l’utilisateur appuie une fois pour sélectionner le mot, appuie deux fois pour sélectionner la ligne entière, et appuie trois fois pour sélectionner le paragraphe entier. En tirant parti de la structure arborescente retournée par l’opération d’analyse, l’application peut relier la zone taraudé à un trait dans l’arbre. Une fois que l’application a trouvé un trait, elle peut remonter l’arborescence pour déterminer comment et quels traits voisins sélectionner.

La sélection d’une ligne entière est un exemple simpliste des avantages de l’analyse de l’encre, mais les possibilités deviennent intéressantes quand l’un d’eux prend en compte les différents types de structures hiérarchiques que l’analyseur d’encre peut détecter :

-   Listes triées et non triées
-   Formes
-   Commentaires annotés écrits en ligne avec le texte

Les types de fonctionnalités varient d’une application à l’autres et sont basés sur les exigences et les moteurs d’analyse et de reconnaissance des encres disponibles.

### <a name="key-ink-analysis-features"></a>Fonctionnalités d’analyse de l’encre de clé

Les fonctionnalités clés de l’API InkAnalysis incluent les fonctionnalités suivantes :

-   Analyse incrémentielle
-   Persistance
-   Proxy de données
-   Rapprochement
-   Extensibilité

### <a name="incremental-analysis"></a>Analyse incrémentielle

Lorsque les utilisateurs finaux travaillent avec de l’encre, ils le considèrent généralement comme l’écriture manuscrite. L’encre est continuellement sujette à des opérations de modification telles que l’ajout de nouvelles encres, la suppression de l’encre existante et la modification des propriétés de l’encre, toutes effectuées de la même façon que l’écriture manuscrite est continuellement modifiée. Ces opérations de modification affectent les résultats de l’analyse. Lorsque des modifications se produisent, elles peuvent généralement être isolées dans des sections du document à des moments précis dans le temps. Par exemple, supposons qu’un utilisateur écrive cinq lignes d’encre. La méthode standard utilisée par les applications pour analyser l’encre est d’attendre que l’utilisateur ait fini d’écrire les cinq lignes d’encre, par exemple un paragraphe, puis d’analyser les résultats, de manière synchrone ou asynchrone.

Vous pouvez optimiser le temps total passé à analyser ces cinq lignes en isolant les zones qui sont analysées au fur et à mesure de leur écriture, puis en réanalysant uniquement les parties des résultats qui ont changé. Une fois la première ligne analysée, elle ne sera jamais reconnue à moins qu’elle ne soit modifiée par l’utilisateur final. La reconnaissance de la deuxième ligne est traitée comme une opération de reconnaissance indépendante.

Cette approche incrémentielle fonctionne bien au niveau de la ligne pour les opérations de reconnaissance, mais elle doit fonctionner à un niveau plus élevé pour l’opération d’analyse de l’encre. Étant donné que l’analyseur d’encre peut détecter différentes classifications de niveau supérieur pour ces cinq lignes d’encre (par exemple, il peut s’agir d’un paragraphe standard ou de cinq éléments dans une liste), l’approche incrémentielle de l’analyseur d’encre est qu’il doit analyser ces structures plus élevées. Autrement dit, une fois que l’analyseur d’encre classe la première ligne d’encre comme une ligne, il vérifie qu’il s’agit toujours d’une ligne lorsqu’il classe la deuxième ligne. Toutefois, l’analyseur d’encre isole cette double vérification du paragraphe et ignore le premier paragraphe lors de l’analyse d’un deuxième paragraphe, en traitant le deuxième paragraphe comme une opération d’analyseur d’encre indépendante. Cette approche incrémentielle de l’analyse économise considérablement le temps de traitement lorsque de grandes quantités d’encre existent déjà dans l’application.

### <a name="persistence"></a>Persistance

L’analyse incrémentielle fonctionne bien au sein d’une session ou d’une instance donnée d’un objet [**InkAnalyzer**](inkanalyzer.md) . Toutefois, les API de la plateforme Tablet PC de première génération ne peuvent pas effectuer une analyse incrémentielle une fois que l’encre est conservée sur le disque. L’API InkAnalysis permet d’enregistrer l’encre sur le disque avec une forme persistante des résultats de l’analyse. Les résultats de l’analyse peuvent être chargés lorsque l’encre est chargée et peuvent être injectées dans une nouvelle instance d’un **InkAnalyzer**. Une nouvelle instance de l’objet **InkAnalyzer** a ensuite le même état de résultats qu’auparavant et peut désormais accepter toutes les modifications en tant que modifications incrémentielles apportées à l’état existant, au lieu d’analyser de nouveau tous les éléments.

### <a name="data-proxy"></a>Proxy de données

De nombreuses applications ont déjà une sorte de structure de document existante dans leurs applications. par exemple, un graphique ou une base de données. Le [**InkAnalyzer**](inkanalyzer.md) présente également les résultats sous forme structurée, dans une arborescence d’objets [**ContextNode**](icontextnode.md) . La structure **InkAnalyzer** et la structure existante de l’application doivent interagir dans deux directions : les résultats sont extraits du **InkAnalyzer** dans l’application et l’État fait l’objet d’un push à partir de l’application dans le **InkAnalyzer**.

Si vous extrayez les résultats de [**InkAnalyzer**](inkanalyzer.md) dans la structure de l’application, c’est tout ce qui était nécessaire, c’est relativement simple. Les applications parcourent l’arborescence des résultats et copient (intègrent) tous les éléments des résultats dont ils ont besoin dans leur structure de données existante. Toutefois, étant donné que de nombreuses applications horizontales nécessitent une analyse incrémentielle et une persistance sur le disque, le problème devient bidirectionnel. L’État (résultats passés) doit être extrait de la structure de l’application et envoyé dans le **InkAnalyzer**.

Pour répondre à cette exigence, [**InkAnalyzer**](inkanalyzer.md) contient une série d’événements qu’il déclenche au moment approprié pendant une opération d’analyse afin de permettre aux applications de renvoyer la requête de données à leurs structures existantes. Ces événements sont déclenchés uniquement pour les objets [**ContextNode**](icontextnode.md) requis par l’opération incrémentielle.

### <a name="reconciliation"></a>Rapprochement

La plupart des applications souhaiteront analyser l’encre en arrière-plan pour limiter au minimum les interruptions de l’interface utilisateur. L’analyse de l’encre en arrière-plan provoque des problèmes, toutefois, si l’utilisateur modifie l’encre (ou l’encre voisine) en cours d’analyse. Par exemple, si l’utilisateur supprime l’encre pendant l’opération d’arrière-plan, la structure résultante reflète l’état du document lorsque l’opération d’arrière-plan a démarré, plutôt qu’à la fin.

Pour aider les applications, le [**InkAnalyzer**](inkanalyzer.md) rapproche les différences dans l’état du document entre le début et la fin de l’opération d’analyse. Les modifications apportées par l’utilisateur ou l’application pendant l’exécution de l’analyse en arrière-plan remplacent toujours les résultats calculés en arrière-plan. Après le rapprochement, seules les parties de la structure de résultats qui ne sont pas en conflit avec les modifications de document sont signalées, et les traits conflictuels sont marqués pour une analyse ultérieure. Lors de la prochaine exécution de l’opération d’analyse en arrière-plan, les résultats sont recalculés en fonction du nouvel État.

Le diagramme suivant illustre ce processus. L’heure est exprimée de façon linéaire de haut en bas dans le diagramme.

![processus de rapprochement des modifications de l’état des documents lors de l’opération d’analyse](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  Au moment 1 (T1), l’application collecte de l’encre auprès de l’utilisateur final, y compris tout type de modification de l’encre, comme l’ajout, la suppression ou la modification.
2.  À T2, l’application appelle l’opération d’analyse en arrière-plan. Le [**InkAnalyzer**](inkanalyzer.md) détermine l’encre qui n’a pas de résultats et l’encre qui doit être vérifiée. Il copie les données d’encre nécessaires pour permettre l’exécution indépendante du thread d’arrière-plan.
3.  À T3, [**InkAnalyzer**](inkanalyzer.md) retourne l’exécution du thread d’interface utilisateur à l’application. Le **InkAnalyzer** crée un deuxième thread, le thread d’analyse en arrière-plan, et les moteurs d’analyse et de reconnaissance des entrées manuscrites analysent les données d’encre copiées.
4.  Pendant que l’opération d’analyse se produit sur le deuxième thread d’arrière-plan, l’utilisateur final continue à modifier le document, en ajoutant et en supprimant les données de trait, aux T4 et T5. Ces modifications peuvent être en conflit avec le travail en cours de traitement en arrière-plan.
5.  Sur T6, le thread d’arrière-plan a terminé l’opération d’analyse et les résultats sont prêts. Avant que le [**InkAnalyzer**](inkanalyzer.md) ne communique les résultats à l’application, il exécute un algorithme de réconciliation pour déterminer si les modifications apportées par l’utilisateur lors du calcul de l’opération d’analyse (T4 et T5) sont en conflit avec les résultats. Si des collisions sont détectées, les traits conflictuels sont signalés pour une nouvelle analyse, qui se produit la prochaine fois que l’application appelle l’opération d’analyse en arrière-plan.
6.  Enfin, sur T7, avec toutes les collisions détectées, le [**InkAnalyzer**](inkanalyzer.md) présente les résultats à l’application.

### <a name="extensibility"></a>Extensibilité

Les API InkAnalysis permettent l’utilisation de nouveaux types de moteurs d’analyse par les applications, de manière à empêcher l’application d’avoir à réécrire tous les avantages de l’API InkAnalysis, y compris la réconciliation, le proxy de données, la persistance et l’analyse incrémentielle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 
