---
description: découvrez les concepts courants lorsque vous souhaitez étendre Windows Explorer, qui est l’une des nombreuses options d’extensibilité dans l’interface utilisateur de l’interpréteur de commandes Windows.
title: Concepts communs de l’Explorateur
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78136c36-bd3c-4114-8b69-fef4e307566d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bd0c641e1e265b50180aa6ce4e98eeafbf3f6dc86f4f499dee5267161842e9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050520"
---
# <a name="common-explorer-concepts"></a>Concepts communs de l’Explorateur

L' *espace de noms* Shell organise le système de fichiers et d’autres objets gérés par le shell en une seule hiérarchie structurée en arborescence. Conceptuellement, il s’agit d’une version plus volumineuse et plus inclusive du système de fichiers.

-   [Introduction](#introduction)
-   [Identification des objets d’espace de noms](#identifying-namespace-objects)
    -   [ID d’élément](#item-ids)
    -   [Listes d’ID d’élément](#item-id-lists)
    -   [PIDL](#pidls)
    -   [Allocation de PIDL](#allocating-pidls)

## <a name="introduction"></a>Introduction

L’une des responsabilités principales de l’interpréteur de commandes consiste à gérer et à fournir l’accès à la grande variété d’objets qui composent le système. Les plus nombreux et les plus familiers de ces objets sont les dossiers et les fichiers qui résident sur les lecteurs de disque de l’ordinateur. Toutefois, l’interpréteur de commandes gère également un certain nombre d’objets de système de fichiers ou *virtuels* . Voici quelques exemples :

-   Imprimantes réseau
-   Autres ordinateurs en réseau
-   Applications du panneau de configuration
-   La corbeille

Certains objets virtuels n’impliquent pas du tout le stockage physique. L’objet Printer, par exemple, contient une collection de liens vers des imprimantes en réseau. D’autres objets virtuels, tels que la corbeille, peuvent contenir des données stockées sur un lecteur de disque, mais doivent être gérées différemment des fichiers normaux. Par exemple, un objet virtuel peut être utilisé pour représenter des données stockées dans une base de données. en termes d’espace de noms, les différents éléments de la base de données peuvent apparaître dans l’explorateur de Windows en tant qu’objets distincts, même s’ils sont tous stockés dans un seul fichier de disque.

Les objets virtuels peuvent même être situés sur des ordinateurs distants. Par exemple, pour faciliter l’itinérance, les fichiers de document d’un utilisateur peuvent être stockés sur un serveur. Pour permettre aux utilisateurs d’accéder à leurs fichiers à partir de plusieurs PC de bureau, le dossier Mes documents sur le PC de bureau qu’ils utilisent actuellement pointe vers le serveur, et non vers le disque dur du PC de bureau. Son chemin d’accès comprend un lecteur réseau mappé ou un nom de chemin d’accès UNC.

À l’instar du système de fichiers, l’espace de noms comprend deux types d’objets : dossiers et fichiers de base. Les objets de dossier sont les *nœuds* de l’arborescence ; Il s’agit de conteneurs pour les objets de fichier et d’autres dossiers. Les objets de fichier sont les *feuilles* de l’arborescence ; Il s’agit soit de fichiers de disque normaux, soit d’objets virtuels, tels que les liens d’imprimante. Les dossiers qui ne font pas partie du système de fichiers sont parfois appelés *dossiers virtuels*.

À l’instar des dossiers du système de fichiers, la collection de dossiers virtuels varie généralement d’un système à l’autres. Il existe trois classes de dossiers virtuels :

-   Les dossiers virtuels standard, tels que la corbeille, qui se trouvent sur tous les systèmes.
-   Dossiers virtuels facultatifs qui ont des noms et des fonctionnalités standard, mais qui peuvent ne pas être présents sur tous les systèmes.
-   Dossiers non standard installés par l’utilisateur.

Contrairement aux dossiers de système de fichiers, les utilisateurs ne peuvent pas créer des dossiers virtuels eux-mêmes. Ils peuvent uniquement installer ceux créés par des développeurs non-Microsoft. Le nombre de dossiers virtuels est donc généralement beaucoup moins élevé que le nombre de dossiers du système de fichiers. Pour plus d’informations sur la façon d’implémenter des dossiers virtuels, consultez [extensions d’espace de noms](nse-works.md).

vous pouvez voir une représentation visuelle de la structure de l’espace de noms dans la barre d’explorateur de l’explorateur de Windows. par exemple, la capture d’écran suivante de Windows Explorer montre un espace de noms relativement simple.

![capture d’écran montrant une vue de l’espace de noms Shell](images/prog1.png)

La racine ultime de la hiérarchie d’espaces de noms est le bureau. Juste en dessous de la racine se trouvent plusieurs dossiers virtuels tels que Poste de travail et la corbeille.

Les systèmes de fichiers des différents lecteurs de disque peuvent être considérés comme des sous-ensembles de la plus grande hiérarchie d’espaces de noms. Les racines de ces systèmes de fichiers sont des sous-dossiers du dossier Poste de travail. Poste de travail comprend également les racines des lecteurs réseau mappés. Les autres nœuds de l’arborescence, tels que mes documents, sont des dossiers virtuels.

## <a name="identifying-namespace-objects"></a>Identification des objets d’espace de noms

Avant de pouvoir utiliser un objet Namespace, vous devez tout d’abord avoir un moyen de l’identifier. Un objet dans le système de fichiers peut avoir un nom tel que MyFile.htm. Étant donné qu’il peut y avoir d’autres fichiers portant ce nom ailleurs dans le système, l’identification unique d’un fichier ou d’un dossier requiert un chemin d’accès complet tel que « C : \\ MyDocs \\MyFile.htm ». Ce chemin d’accès est fondamentalement une liste triée de tous les dossiers dans un chemin d’accès à partir de la racine du système de fichiers, C : \\ , se terminant par le fichier.

Dans le contexte de l’espace de noms, les chemins d’accès sont toujours très utiles pour identifier les objets situés dans la partie du système de fichiers de l’espace de noms. Toutefois, ils ne peuvent pas être utilisés pour des objets virtuels. Au lieu de cela, l’interpréteur de commandes fournit un autre moyen d’identification qui peut être utilisé avec n’importe quel objet d’espace de noms.

### <a name="item-ids"></a>ID d’élément

Dans un dossier, chaque objet a un *ID d’élément*, qui est l’équivalent fonctionnel d’un nom de fichier ou de dossier. L’ID d’élément est en fait une structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) :


```
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Le membre **abID** est l’identificateur de l’objet. La longueur de **abID** n’est pas définie, et sa valeur est déterminée par le dossier qui contient l’objet. Étant donné qu’il n’existe aucune définition standard de la façon dont les valeurs **abID** sont assignées par les dossiers, elles ne sont significatives que pour l’objet Folder associé. Les applications doivent simplement les traiter comme un jeton qui identifie un objet dans un dossier particulier. Étant donné que la longueur de **abID** varie, le membre **CB** contient la taille de la structure [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , en octets.

Étant donné que les ID d’élément ne sont pas utiles à des fins d’affichage, le dossier qui contient l’objet lui assigne normalement un nom complet. il s’agit du nom utilisé par Windows Explorer lorsqu’il affiche le contenu d’un dossier. Pour plus d’informations sur la gestion des noms d’affichage, consultez [obtention d’informations à partir d’un dossier](folder-info.md).

### <a name="item-id-lists"></a>Listes d’ID d’élément

L’ID d’élément est rarement utilisé par lui-même. Normalement, elle fait partie d’une liste d’ID d’élément, qui remplit le même objectif qu’un chemin d’accès de système de fichiers. Toutefois, au lieu de la chaîne de caractères utilisée pour les chemins d’accès, une liste d’ID d’élément est une structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Cette structure est une séquence ordonnée d’un ou plusieurs ID d’élément, se terminant par une **valeur null** de deux octets. Chaque ID d’élément dans la liste d’ID d’élément correspond à un objet d’espace de noms. Leur ordre définit un chemin d’accès dans l’espace de noms, comme un chemin d’accès au système de fichiers.

L’illustration suivante montre une représentation schématique de la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) qui correspond à C : \\ mydocs \\MyFile.htm. Le nom complet de chaque ID d’élément est affiché au-dessus de lui. Les largeurs variables des membres **abID** sont arbitraires ; ils illustrent le fait que la taille de ce membre peut varier.

![Illustration schématique d’un PIDL](images/shell2.png)

### <a name="pidls"></a>PIDL

Pour l’API de l’interpréteur de commandes, les objets d’espace de noms sont généralement identifiés par un pointeur désignant leur structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) ou un pointeur vers une liste d’identificateurs d’éléments (PIDL). Pour plus de commodité, le terme PIDL fait généralement référence à la structure elle-même plutôt qu’au pointeur.

Le PIDL présenté dans l’illustration précédente est appelé PIDL *complet* ou *absolu*. Un PIDL complet démarre à partir du bureau et contient les ID d’élément de tous les dossiers intermédiaires dans le chemin d’accès. Il se termine par l’ID d’élément de l’objet suivi d’une **valeur null** de deux octets de fin. Un PIDL complet est semblable à un chemin d’accès qualifié complet et identifie de façon unique l’objet dans l’espace de noms de l’interpréteur de commandes.

Les PIDL complets sont rarement utilisés. De nombreuses fonctions et méthodes attendent un *PIDL relatif*. La racine d’un PIDL relatif est un dossier, pas le bureau. Comme avec les chemins d’accès relatifs, la série d’ID d’élément qui composent la structure définissent un chemin d’accès dans l’espace de noms entre deux objets. Bien qu’ils n’identifient pas l’objet de manière unique, ils sont généralement plus petits qu’un PIDL complet et suffisants à de nombreuses fins.

Les PIDL relatifs les plus couramment utilisés, *PIDL à un seul niveau*, sont relatifs au dossier parent de l’objet. Elles contiennent uniquement l’ID d’élément de l’objet et une **valeur null** de fin. Les PIDL à plusieurs niveaux sont également utilisés à de nombreuses fins. Ils contiennent au moins deux ID d’élément et définissent généralement un chemin d’accès d’un dossier parent à un objet via une série d’un ou plusieurs sous-dossiers. Notez qu’un PIDL à un seul niveau peut toujours être un PIDL complet. En particulier, les objets de bureau sont des enfants du bureau, donc leur PIDL complet ne contient qu’un seul ID d’élément.

Comme nous l’avons vu dans obtention de l' [ID d’un dossier](folder-id.md), l’API Shell fournit plusieurs façons de récupérer les PIDL d’un objet. Une fois que vous l’avez, vous l’utilisez généralement pour identifier l’objet lorsque vous appelez d’autres fonctions et méthodes de l’API Shell. Dans ce contexte, le contenu interne d’un PIDL est opaque et inutile. Pour les besoins de cette discussion, considérez PIDL comme des jetons qui représentent des objets d’espace de noms particuliers et concentrez-vous sur la façon de les utiliser pour les tâches courantes.

### <a name="allocating-pidls"></a>Allocation de PIDL

Bien que les PIDL aient une certaine similarité avec les chemins d’accès, leur utilisation requiert une approche quelque peu différente. La principale différence réside dans la façon d’allouer et de libérer de la mémoire pour eux.

À l’instar de la chaîne utilisée pour un chemin d’accès, la mémoire doit être allouée à un PIDL. Si une application crée un PIDL, elle doit allouer suffisamment de mémoire pour la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Pour la plupart des cas présentés ici, le shell crée le PIDL et gère l’allocation de mémoire. Indépendamment de ce qui a alloué le PIDL, l’application est généralement chargée de libérer les PIDL lorsqu’elle n’est plus nécessaire.

Utilisez la fonction [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer PIDL et la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour la libérer.

 

 
