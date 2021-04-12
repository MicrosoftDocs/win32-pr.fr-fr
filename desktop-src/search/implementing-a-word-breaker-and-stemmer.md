---
description: Microsoft fournit des analyseurs lexicaux et des générateurs de formes dérivées pour un certain nombre de langages. Cette rubrique décrit comment implémenter et utiliser des analyseurs lexicaux et des générateurs de formes dérivées personnalisés pour les langues, et les paramètres régionaux au-delà de ceux fournis par Microsoft.
ms.assetid: 47768691-7071-440e-bfbf-975713880c00
title: Implémentation d’un analyseur lexical et du générateur de formes dérivées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd4f4e3210e7f4e17bb035115fd694656cc6e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033878"
---
# <a name="implementing-a-word-breaker-and-stemmer"></a>Implémentation d’un analyseur lexical et du générateur de formes dérivées

Microsoft fournit des analyseurs lexicaux et des générateurs de formes dérivées pour un certain nombre de langages. Cette rubrique décrit comment implémenter et utiliser des analyseurs lexicaux et des générateurs de formes dérivées personnalisés pour les langues, et les paramètres régionaux au-delà de ceux fournis par Microsoft.

> [!Note]
> Depuis le 2018 juillet, une modification de sécurité a été apportée à Windows Server 2019, qui empêche les dll sans signature Microsoft d’être chargées par SearchIndexer.exe. Par conséquent, Windows Server 2019 ne prend plus en charge les analyseurs lexicaux personnalisés non signés par Microsoft. 

Cette rubrique est organisée comme suit :

-   [Inscription d’une DLL de ressource de langue](#registering-a-language-resource-dll)
-   [Inscription d’une langue](#registering-a-language-resource-dll)
-   [Implémentation d’un bécher de mot](#implementing-a-word-beaker)
    -   [WordSink et PhraseSink](#wordsink-and-phrasesink)
    -   [Sauts](#breaks)
    -   [Évolutivité, Performancy et sécurité](#scalability-performancy-and-security)
-   [Implémentation d’un générateur de formes dérivées](#implementing-a-stemmer)
    -   [Évolutivité, Performancy et sécurité](#scalability-performancy-and-security)
-   [Rubriques connexes](#related-topics)

## <a name="registering-a-language-resource-dll"></a>Inscription d’une DLL de ressource de langue

Chaque DLL de ressource de langue doit implémenter et exporter les points d’entrée suivants. La DLL peut être inscrite dans n’importe quel dossier.

-   DllMain est le point d’entrée standard de la DLL.
-   DllRegisterServer inscrit la DLL dans le registre, par exemple `regsvr32.exe %SystemRoot%\MyFolder\wordbreaker.dll`
-   DllCanUnloadNow permet aux clients d’appeler ce point d’entrée par le biais du modèle COM (Component Object Model) pour déterminer s’il est possible de décharger la DLL de ressources de langue.
-   DllUnRegisterServer supprime la DLL du Registre.

## <a name="registering-a-language"></a>Inscription d’une langue

Le registre contient des entrées spécifiques à la langue pour la langue en cours d’indexation, et ces entrées contrôlent les parties des processus d’indexation et de requête qui sont spécifiques à la langue. Ces entrées de Registre se trouvent sous la clé de Registre suivante.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         ContentIndex
            Control
               Language
                  
```

## <a name="implementing-a-word-beaker"></a>Implémentation d’un bécher de mot

Les analyseurs lexicaux implémentent [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker). La méthode [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) effectue toutes les opérations de traitement et d’analyse de texte. Pour implémenter un composant analyseur lexical, vous devez disposer de l’heuristique de langue pour votre langage. Cela comprend des informations sur la syntaxe et la morphologie. Vous pouvez également avoir besoin d’une liste de mots à exclure ou inclure. Vous générez le fichier de mots parasites pour vos paramètres régionaux de langue à partir de la liste des mots exclus. Pour plus d’informations sur les considérations linguistiques et sur la façon dont ces considérations affectent les implémentations de l’analyseur lexical, consultez [Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md).

L’objectif principal de [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) est de traiter le texte en continu à partir de la [**\_ source de texte**](/windows/win32/api/indexsrv/ns-indexsrv-text_source) jusqu’à ce que tout le texte soit traité ou jusqu’à ce que l’analyseur lexical rencontre une erreur. Dans cette boucle de traitement des données, **IWordBreaker :: BreakText** appelle l’analyse et les méthodes utilitaires qui effectuent des tâches spécifiques pour ce processus. Par exemple, l’analyseur lexical allemand peut gérer les mots composés, tandis que l’analyseur lexical français peut traiter les [signes diacritiques](surface-form-normalization.md) ou [clitics](surface-form-normalization.md). Les fonctions spécifiques exécutées par l’analyseur lexical et la stratégie qu’il utilise pour effectuer ces tâches dépendent entièrement des exigences de cette langue.

Lorsque vous scindez du texte, les analyseurs lexicaux identifient les formes « alternatives » pour les mots qui peuvent avoir plusieurs représentations. Aucune relation sémantique n’est implicite entre les mots générés. En fait, le mot d’origine ne peut pas être inclus dans la liste des alternatives. Les autres formulaires sont enregistrés à la même position dans l’index que le mot d’origine pour indiquer qu’ils sont identiques.

Lorsqu’un document est inclus dans l’index, chaque mot reçoit une valeur entière qui représente le décalage, ou la distance entre le mot et le début d’un document. La distance relative entre les mots d’une requête est comparée aux décalages stockés dans l’index de recherche en texte intégral. La requête « where is Kyle document » correspond à n’importe quel document avec « WHERE » au décalage n, « a » à n + 1, « Kyle » à n + 2 et « document » à n + 3. « Où est enregistré le document Kyle dans la base de données ? » est représenté comme suit :



|       |     |                        |          |       |     |     |                               |
|-------|-----|------------------------|----------|-------|-----|-----|-------------------------------|
| Where | is  | Kyle Kyle<br/> | document | classer | in  | le | base de données de base de données<br/> |



 

Dans cet exemple, l’analyseur lexical stocke d’autres formulaires pour « Kyle » (« Kyle ») et « Database » (« base de données ») dans l’index. L’analyseur lexical génère et stocke des mots alternatifs pendant le processus de création d’index dans les conditions suivantes :

-   Si un autre mot est susceptible de s’afficher sous la forme d’un mot unique dans une requête
-   Si un générateur de formes dérivées ne risque pas de dériver le mot d’origine à partir de l’autre

La génération de mots de passe alternatifs augmente le nombre de façons dont les requêtes représentent et correspondent à une phrase, comme indiqué dans les variations suivantes :

1.  Où est archivé le document Kyle dans la base de données
2.  Où est archivé le document Kyle dans la base de données
3.  Où le document Kyle est-il archivé dans la base de données ?
4.  Où est classé le document Kyle dans la base de données

### <a name="wordsink-and-phrasesink"></a>WordSink et PhraseSink

Les analyseurs lexicaux utilisent les objets [**IWordSink**](iwordsink.md) et [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) pour collecter et stocker tous les mots et expressions qu’ils extraient du texte. Un analyseur lexical stocke des mots dans un formulaire le plus proche possible du formulaire Word d’origine dans le document. **IPhraseSink** stocke les expressions au moment de la requête. Les expressions améliorent la pertinence des résultats de la requête, car les séquences de mots plus longues sont plus rares et offrent une plus grande différence par rapport aux expressions plus petites. Lorsque l’indexeur place une expression dans le **IPhraseSink** au moment de la requête, il crée une instance de l’analyseur lexical pour décomposer l’expression en mots. L’indexeur évalue ensuite l’expression en vérifiant si les mots de l’expression apparaissent adjacents l’un à l’autre dans l’index. Par exemple, si « ABCD » se trouve dans l’index aux positions *x*, *x*+ 1, *x*+ 2 et *x*+ 3, la correspondance d’expression se produit si une sous-chaîne adjacente de « abcd » est soumise dans une requête. Cette stratégie est efficace pour les analyseurs lexicaux basés sur des caractères qui fractionnent les expressions et les mots longs pendant la création de l’index et qui génèrent des expressions au moment de la requête.

### <a name="breaks"></a>Sauts

Les sauts sont les espaces entre les mots. Un espace blanc, une ponctuation, une mise en forme ou simplement la nature du langage lui-même peut entraîner des ruptures. L’indexeur utilise quatre types différents de sauts : fin de mot (EOW), fin de phrase (EOS), fin de paragraphe (EOP) et fin de chapitre (EOC). L’arrêt EOW est l’arrêt par défaut. Après chaque jeton, chaque saut indique une distance sémantique différente entre les mots situés de part et d’autre. Les mots séparés par EOW ont le lien sémantique le plus étroit, suivi de EOS, EOP et EOC. Plusieurs appels à [**IWordSink ::P utbreak**](iwordsink-putbreak.md) sont cumulatifs et sont analogues à l’insertion de mots ou de phrases null.

### <a name="scalability-performancy-and-security"></a>Évolutivité, Performancy et sécurité

La manière dont l’analyseur lexical répond aux appels simultanés est en grande partie déterminée par votre choix de modèle de thread. L’indexeur est une application à thread unique. Pour que les analyseurs lexicaux fonctionnent dans un environnement à thread unique, les analyseurs lexicaux doivent être écrits à l’aide d’un modèle de thread « gratuit » ou « les deux ». Les analyseurs lexicaux ne doivent pas s’inscrire auprès de COM à l’aide du modèle de thread « Apartment ».

Nous recommandons que les analyseurs lexicaux évitent les États globaux et stockent les données dans l’instance de l’analyseur lexical. Le seul contenu qui doit être stocké dans l’implémentation de l’analyseur lexical concerne les paramètres *fQuery* et *ulMaxTokenSize*. Les analyseurs lexicaux ne doivent pas être plus de deux fois plus lents que le benchmark établi par l’analyseur lexical anglais. Les performances de l’analyseur lexical doivent également améliorer l’augmentation de la capacité du matériel.

Les analyseurs lexicaux de l’indexeur s’exécutent dans le contexte de sécurité du système local. Elles doivent être écrites pour gérer les mémoires tampons et les empiler correctement. Toutes les copies de chaînes doivent avoir des vérifications explicites pour se protéger contre les dépassements de mémoire tampon. Vous devez toujours vérifier la taille allouée de la mémoire tampon et tester la taille des données en fonction de la taille de la mémoire tampon. Les analyseurs lexicaux ne peuvent pas supposer que le texte transmis à la méthode [**IWordBreaker :: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) est bien formé. Pour plus d’informations sur la résolution des problèmes des analyseurs lexicaux, consultez [Dépannage des ressources et des meilleures pratiques en matière de langage](troubleshooting-language-resources.md).

## <a name="implementing-a-stemmer"></a>Implémentation d’un générateur de formes dérivées

Les générateurs de formes dérivées implémentent l’interface [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) . La méthode [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) génère une liste de formes de mots pour un mot d’entrée particulier. Pour implémenter un composant de générateur de formes dérivées, vous devez disposer de l’heuristique de langue pour votre langage. Cela comprend des informations sur la morphologie. Vous pouvez également avoir besoin d’une liste de mots à exclure ou inclure. Pour plus d’informations sur les considérations linguistiques et sur la façon dont ces considérations affectent les implémentations de générateur de formes dérivées, consultez [Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md).

Nous recommandons que les générateurs de formes dérivées ne doivent pas générer le génitif, ou disposer, de mots. Par exemple, « David » n’est pas généré comme autre formulaire pour « David ». Le séparateur de mots génère « David » et « David » lorsqu’il analyse « David ».

Le générateur de formes dérivées utilise l’objet [IWordFormSink](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) pour recueillir la liste des mots alternatifs. [**IWordFormSink ::P utword**](iwordformsink-putword.md) génère le mot final à partir du générateur de formes dérivées. Dans tous les cas, ce mot final est le même que le mot d’entrée de [**IStemmer :: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms). Par exemple, étant donné le mot « natation », le générateur de formes dérivées génère les mots suivants : « natation », « nageur », « natation », « SWAM » et « SWUM », par le biais des appels à [**IWordFormSink ::P utaltword**](iwordformsink-putphrase.md). Le générateur de formes dérivées génère une « natation » via **IWordFormSink ::P utword**.

### <a name="scalability-performancy-and-security"></a>Évolutivité, Performancy et sécurité

Les générateurs de formes dérivées, tels que les analyseurs lexicaux, doivent utiliser un modèle de thread « gratuit » et s’inscrire auprès de COM avec leur modèle de thread défini sur « gratuit » ou « les deux ». Windows Search appelle des instances distinctes du générateur de formes dérivées à partir de différents threads en même temps. Les générateurs de formes dérivées doivent donc disposer de données d’instance minimales.

La précision de la conjugaison a un impact significatif sur la pertinence des requêtes. Si le générateur de formes dérivées ne génère pas correctement le texte, les requêtes peuvent retourner des résultats imprévisibles et inexacts. Les générateurs de formes dérivées doivent gérer des centaines de requêtes par seconde sans affecter négativement les performances des requêtes. Les performances du générateur de formes dérivées doivent s’améliorer avec une capacité matérielle accrue. Pour plus d’informations sur le dépannage des générateurs de formes dérivées, consultez [Dépannage des ressources linguistiques et des meilleures pratiques](troubleshooting-language-resources.md).

Les générateurs de formes dérivées pour Windows Search s’exécutent dans le contexte de sécurité local. Elles doivent être écrites pour gérer les mémoires tampons et les empiler correctement. Toutes les copies de chaînes doivent avoir des vérifications explicites pour se protéger contre les dépassements de mémoire tampon. Vous devez toujours vérifier la taille allouée de la mémoire tampon et tester la taille des données en fonction de la taille de la mémoire tampon.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extension des ressources linguistiques](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Fonctionnement des composants de ressources linguistiques](understanding-language-resource-components.md)
</dt> <dt>

[Considérations linguistiques et Unicode](linguistic-and-unicode-considerations.md)
</dt> <dt>

[Ressources et meilleures pratiques pour la résolution des problèmes](troubleshooting-language-resources.md)
</dt> </dl>

 

 
