---
description: 'La recherche : le protocole d’application est une convention extensible pour l’appel de l’application Desktop Search sur Windows Vista avec Service Pack 1 (SP1) et versions ultérieures.'
title: Utilisation du protocole de recherche
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991737"
---
# <a name="using-the-search-protocol"></a>Utilisation du protocole de recherche

La **recherche :** le [protocole d’application](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) est une convention extensible pour l’appel de l’application Desktop Search sur Windows Vista avec Service Pack 1 (SP1) et versions ultérieures. Le protocole a été créé dans Windows Vista avec SP1 (pour plus d’informations, consultez l’article [vue d’ensemble de Windows Vista Desktop Search changes in Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) afin de permettre à Windows de déterminer et d’appeler l’application Desktop Search par défaut.

La syntaxe du protocole fournit un certain nombre de paramètres utiles pour effectuer des recherches courantes sur le bureau, telles que des termes de recherche entrés par l’utilisateur ou l’emplacement où la recherche a commencé. Lorsque les utilisateurs recherchent à partir de l’un des deux points d’entrée de recherche disponibles (le menu **Démarrer** ou l’Explorateur Windows), le système d’exploitation utilise le protocole de recherche pour lancer l’application Desktop Search par défaut. Pour ce faire, il ajoute les termes de recherche entrés par l’utilisateur à la syntaxe du protocole de recherche standard et transmet ces informations à l’application inscrite en tant qu’application de recherche par défaut.

Si aucune autre application Desktop Search n’est installée, une recherche entrée dans ces points d’entrée lance l’Explorateur de recherche Windows. Toutefois, les développeurs tiers peuvent créer, installer et inscrire leurs applications pour gérer le protocole de recherche et être l’application de recherche par défaut. De telles applications doivent prendre en charge la syntaxe du protocole de recherche et s’inscrire auprès de la fonctionnalité [programmes par défaut](default-programs.md) pour garantir une expérience transparente avec Windows.

Si vous développez une application destinée à utiliser ou à créer une application de recherche sur le bureau spécifique, vous ne devez pas dépendre exclusivement du protocole **Search :** . Étant donné que de nombreuses applications peuvent posséder le protocole **Search :** , il n’y a aucune garantie que votre application de recherche de bureau ciblée en sera propriétaire à un moment donné. Au lieu de cela, vous devez utiliser un protocole de recherche privé défini par cette application de recherche de bureau ciblée. Cela signifie que les applications Desktop Search destinées à être une plateforme pour les applications tierces doivent prendre en charge le protocole **Search :** et leur propre protocole de recherche propriétaire.

> [!Note]  
> Le protocole **Search :** ne remplace pas la propriété [search-ms :](../search/-search-3x-wds-qryidx-searchms.md) Protocol. Les applications peuvent toujours utiliser le protocole **search-ms :** Protocol pour lancer l’Explorateur de recherche dans la fenêtre ou pour interroger silencieusement l’indexeur de recherche Windows.

 

Cette rubrique couvre les sujets suivants :

-   [Syntaxe](#syntax)
-   [Windows Vista avec SP1 utilisation du protocole Search :](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [Exemples](#examples)
-   [Inscription de l’application qui gère le protocole](#registering-the-application-that-handles-the-protocol)
    -   [Entrées de Registre](#registry-entries)
-   [Rubriques connexes](#related-topics)

## <a name="syntax"></a>Syntaxe

Le protocole de recherche utilise la syntaxe encodée par URL standard suivante :


```C++
search:parameter=value[&parameter=value]&
```



La syntaxe commence par identifier le protocole lui-même (**Search :**). Les paires paramètre/valeur sont des arguments passés au moteur de recherche, comme décrit dans le tableau suivant, qui montre tous les paramètres possibles pour la syntaxe du protocole de recherche.



| Paramètre                                              | Valeur                                                         | Description                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| query                                                  | Texte encodé URL                                              | Texte de la requête entré par l’utilisateur.                                                                                                                                                                                                                                                            |
| [InputLocale](search-protocol-localeidentifiers.md)   | Tout identificateur de code de langue (LCID) valide                     | LCID qui identifie la langue d’entrée de la requête.                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | Tout LCID valide                                                | LCID qui identifie la langue de la version internationale de l’indexeur. La valeur par défaut est 1033 (en-US).                                                                                                                                                                                |
| [navigation](search-protocol-crumb.md)                     | Instruction AQS                                                 | Cet argument restreint l’étendue dans laquelle la recherche est effectuée. Dans Windows Vista, le protocole de recherche prend en charge la AQS complète, ainsi qu’une implémentation spéciale pour un `location` argument. Dans Windows XP, le protocole de recherche prend également en charge la AQS complète, à l’exception d’une implémentation spéciale de `kind` et `store` . |
| [stockéesyntaxe](search-protocol-syntaxargument.md)           | NQS, AQS (ne respecte pas la casse)                                 | Syntaxe de requête à utiliser pour effectuer une recherche dans l’index : syntaxe de requête naturelle ou syntaxe de requête avancée (AQS). AQS est la valeur par défaut et est toujours supposé analysé et pris en charge.                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | Toute propriété valide du système de propriétés                   | Propriété qui spécifie la colonne par laquelle piler les résultats.                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | Un chemin d’accès complètement spécifié pour un fichier de recherche enregistré ( \* . search-ms) | Les résultats de la sous-requête sont utilisés en tant que source de la requête. Autrement dit, les termes de la requête sont recherchés par rapport aux résultats de la sous-requête.                                                                                                                                               |
| displayname                                            | Chaîne encodée URL                                            | Nom de la recherche actuelle.                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Windows Vista avec SP1 utilisation du protocole Search :

Windows Vista avec SP1 possède plusieurs points d’entrée à partir desquels il appelle le protocole **Search :** . Ces points d’entrée sont présentés ci-dessous, ainsi que la syntaxe commune associée à chacun d’entre eux.



| Point d’entrée du protocole de recherche | Emplacement         | Requête appelée                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **Rechercher partout**       | Menu **Démarrer**   | recherche : requête =<*terme de recherche*>                                   |
| **Rechercher partout**       | Explorateur Windows | recherche : requête =<*terme de recherche*>&de navigation = emplacement : *emplacement* du <> |
| Touche Windows + F          | N'importe où         | recherche                                                              |
| Ctrl+F                      | Explorateur Windows | recherche : requête =<*terme de recherche*>&de navigation = emplacement : *emplacement* du <> |
| F3                          | Menu **Démarrer**   | recherche                                                              |
| F3                          | Explorateur Windows | recherche : requête =<*terme de recherche*>&de navigation = emplacement : *emplacement* du <> |



 

Les points d’entrée du protocole de recherche Windows Vista avec SP1 ne tirent pas parti de tous les paramètres possibles dans le protocole de recherche. Les applications qui sont uniquement concernées par le traitement des appels de protocole de recherche à partir de Windows Vista avec SP1 peuvent utiliser le tableau suivant comme guide sur le minimum qu’ils doivent implémenter.



| Paramètre                                              | Utilisé par Windows ? | Comment Windows Vista avec SP1 l’utilise lors de l’appel de Search :                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| query                                                  | Oui              | Texte de la requête entré par l’utilisateur.                                                                                                                                                                                                                                         |
| [navigation](search-protocol-crumb.md)                     | Oui              | la [navigation](search-protocol-crumb.md) utilise l' `location` argument pour spécifier l’origine de la requête.                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Oui              | Les résultats de l’argument de [sous-requête](search-protocol-subquery.md) sont utilisés comme étendue des éléments à rechercher. Cela est généralement utilisé si un utilisateur utilisait un fichier. search-ms pour effectuer une recherche, puis l’a appelé application Desktop Search par défaut à partir de cette recherche. |
| [InputLocale](search-protocol-localeidentifiers.md)   | Non               | Pas utilisé pour l'instant.                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | Non               | Pas utilisé pour l'instant.                                                                                                                                                                                                                                                         |
| [stockéesyntaxe](search-protocol-syntaxargument.md)           | Non               | Pas utilisé pour l'instant.                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | Non               | Pas utilisé pour l'instant.                                                                                                                                                                                                                                                         |
| displayname                                            | Non               | Pas utilisé pour l'instant.                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>Exemples

Si un utilisateur entre « Microsoft » dans le menu **Démarrer** et clique sur **Rechercher partout**, l’appel de protocole de recherche qui en résulte est effectué :


```C++
search:query=microsoft&
```



Si un utilisateur entre « Seattle » dans l’Explorateur Windows dans C : \\ mondossier, puis clique sur **Rechercher partout**, l’appel suivant est effectué, en utilisant des caractères d’échappement pour «  : » et « \\ » :


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>Inscription de l’application qui gère le protocole

Étant donné que plusieurs applications peuvent rivaliser pour le protocole de recherche, vous devez inscrire votre application auprès de la fonctionnalité [programmes par défaut](default-programs.md) pendant l’installation pour permettre à l’utilisateur de configurer plus facilement la valeur par défaut. En plus des procédures d’installation normalement recommandées sous Windows XP, une application Windows Vista doit s’inscrire auprès de la fonctionnalité programmes par défaut afin que l’application et les utilisateurs puissent configurer les valeurs par défaut en toute transparence.

Après l’installation des fichiers binaires nécessaires sur l’ordinateur de l’utilisateur, votre routine d’installation doit effectuer les tâches générales suivantes :

1.  Écrivez les ProgID sur la **\_ \_ machine locale HKEY**, comme décrit ci-dessous. Notez que les applications doivent créer des ProgID spécifiques à l’application pour le protocole de recherche.
2.  Demandez une association de protocole de recherche au niveau de l’ordinateur.
3.  Enregistrez l’application avec les [programmes par défaut](default-programs.md), comme expliqué dans la rubrique [inscription d’une application pour une utilisation avec les programmes par défaut](default-programs.md), en tant que contendeur pour le protocole de recherche.

### <a name="registry-entries"></a>Entrées de Registre

Voici des exemples d’entrées de Registre requises pour une application de recherche de bureau fictive, contoso Search.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe de requête avancée](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[Programmes par défaut](default-programs.md)
</dt> </dl>

 

 
