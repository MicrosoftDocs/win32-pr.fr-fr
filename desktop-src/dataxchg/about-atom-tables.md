---
title: À propos des tables Atom
description: Cette section traite des tables Atom.
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- atomes
- tables Atom
- noms Atom
- Échange dynamique de données (DDE), atomes
- DDE (échange dynamique de données), atomes
- tables Atom globales
- tables Atom locales
- atomes d’entiers
- atomes de chaînes
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 92a8304e1e96c7385ddb11ba6391258acbe62a26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549604"
---
# <a name="about-atom-tables"></a>À propos des tables Atom

Une *table Atom* est une table définie par le système qui stocke des chaînes et des identificateurs correspondants. Une application place une chaîne dans une table Atom et reçoit un entier 16 bits, appelé *Atom*, qui peut être utilisé pour accéder à la chaîne. Une chaîne placée dans une table Atom est appelée un *nom Atom*.

Le système fournit un certain nombre de tables Atom. Chaque table Atom remplit un rôle différent. Par exemple, les applications échange dynamique de données (DDE) utilisent la [table Atom globale](#global-atom-table) pour partager des chaînes nom d’élément et nom de rubrique avec d’autres applications. Au lieu de passer des chaînes réelles, une application DDE transmet des atomes globaux à son application partenaire. Le partenaire utilise les atomes pour obtenir les chaînes de la table Atom.

Les applications peuvent utiliser des tables Atom locales pour stocker leurs propres associations nom-élément.

Le système utilise des tables Atom qui ne sont pas directement accessibles aux applications. Toutefois, l’application utilise ces atomes lors de l’appel d’une variété de fonctions. Par exemple, les formats de presse-papiers inscrits sont stockés dans une table Atom interne utilisée par le système. Une application ajoute des atomes à cette table Atom à l’aide de la fonction [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . En outre, les classes inscrites sont stockées dans une table Atom interne utilisée par le système. Une application ajoute des atomes à cette table Atom à l’aide de la fonction [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) ou [**RegisterClassEx**](/windows/desktop/api/winuser/nf-winuser-registerclassexa) .

Les rubriques suivantes sont présentées dans cette section.

-   [Table Atom globale](#global-atom-table)
-   [Table Atom utilisateur](#user-atom-table)
-   [Tables Atom locales](#local-atom-tables)
-   [Types Atom](#atom-types)
    -   [Atomes de chaînes](#string-atoms)
    -   [Atomes d’entiers](#integer-atoms)
-   [Création et nombre d’utilisations Atom](#atom-creation-and-usage-count)
-   [Requêtes de table Atom](#atom-table-queries)
-   [Formats de chaîne Atom](#atom-string-formats)

## <a name="global-atom-table"></a>Table Atom globale

La table Atom globale est disponible pour toutes les applications. Quand une application place une chaîne dans la table Atom globale, le système génère un Atom qui est unique dans l’ensemble du système. Toute application qui a l’atome peut obtenir la chaîne qu’elle identifie en interrogeant la table Atom globale.

Une application qui définit un format de données DDE privé pour le partage de données avec d’autres applications doit placer le nom de format dans la table Atom globale. Cette technique évite les conflits avec les noms de formats définis par le système ou par d’autres applications, et rend les identificateurs (atomes) des messages ou des formats disponibles pour les autres applications.

## <a name="user-atom-table"></a>Table Atom utilisateur

En plus de la table Atom globale, la table Atom de l’utilisateur est une autre table d’Atoms système qui est également partagée entre tous les processus. La table Atom utilisateur est utilisée pour un petit nombre de scénarios internes à Win32k ; par exemple, les noms de modules Windows, les chaînes connues dans Win32k, les formats OLE, etc. Bien que les applications n’interagissent pas directement avec la table Atom utilisateur, elles appellent plusieurs API, telles que [registerClass](/windows/win32/api/winuser/nf-winuser-registerclassexa), [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)et [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata), qui ajoutent des entrées à la table Atom de l’utilisateur. Les entrées ajoutées par `RegisterClass` peuvent être supprimées par `UnregisterClass` . Toutefois, les entrées ajoutées par `RegisterWindowMessage` et `RegisterClipboardFormat` ne sont pas supprimées tant que la session n’est pas terminée. Si la table Atom de l’utilisateur n’a plus d’espace et que la chaîne passée n’est pas déjà dans la table, l’appel échoue. 

### <a name="atom-table-size"></a>Taille de la table Atom
 
De nombreuses API critiques, y compris [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa), s’appuient sur les atomes utilisateur. Par conséquent, l’épuisement de l’espace dans la table Atom de l’utilisateur entraînera des problèmes graves. par exemple, le lancement de toutes les applications peut échouer. Voici quelques recommandations pour vous assurer que votre application utilise efficacement les tables Atom et préserve la fiabilité et les performances de l’application et du système :  

1. Vous devez limiter l’utilisation de votre application par la table Atom utilisateur. Le stockage de chaînes uniques à l’aide d’API telles que `RegisterClass` , `RegisterWindowMessage` ou `RegisterClipboardFormat` prend de l’espace dans la table Atom utilisateur, qui est utilisé globalement par d’autres applications pour inscrire des classes de fenêtre à l’aide de chaînes. Si possible, vous devez utiliser [AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw) / [DeleteAtom](/windows/desktop/api/Winbase/nf-winbase-deleteatom) pour stocker des chaînes dans une table Atom locale, ou [GlobalAddAtom](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / [GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) si les atomes sont nécessaires entre processus.

1. En cas de problème au niveau de l’application provoquant des problèmes de table Atom utilisateur, vous pouvez examiner la cause racine en connectant le débogueur du noyau et en révisant le processus lors des appels à `UserAddAtomEx` ( `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` ). Recherchez `user32!` sur la pile des appels pour voir l’API appelée. La méthodologie est similaire à la détection globale des problèmes liés aux tables Atom, décrite dans [identification des fuites de tables Atom globales](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks). Pour vider le contenu de la table Atom utilisateur, vous pouvez également appeler [GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) sur la plage d’atomes possibles de 0XC000 à 0xFFFF. Si le nombre total d’atomes augmente régulièrement pendant que l’application est en cours d’exécution ou ne retourne pas à la ligne de base lorsque l’application est fermée, il y a un problème.

## <a name="local-atom-tables"></a>Tables Atom locales

Une application peut utiliser une table Atom locale pour gérer efficacement un grand nombre de chaînes utilisées uniquement dans l’application. Ces chaînes, ainsi que les atomes associés, sont uniquement disponibles pour l’application qui a créé la table.

Une application nécessitant la même chaîne dans plusieurs structures peut réduire l’utilisation de la mémoire à l’aide d’une table Atom locale. Au lieu de copier la chaîne dans chaque structure, l’application peut placer la chaîne dans la table Atom et inclure l’atome résultant dans les structures. De cette façon, une chaîne apparaît une seule fois en mémoire, mais peut être utilisée plusieurs fois dans l’application.

Les applications peuvent également utiliser des tables Atom locales pour gagner du temps lors de la recherche d’une chaîne particulière. Pour effectuer une recherche, une application doit uniquement placer la chaîne de recherche dans la table Atom et comparer l’atome résultant avec les atomes dans les structures pertinentes. La comparaison des atomes est généralement plus rapide que la comparaison de chaînes.

Les tables Atom sont implémentées en tant que tables de hachage. Par défaut, une table Atom locale utilise des compartiments 37 pour sa table de hachage. Toutefois, vous pouvez modifier le nombre de compartiments utilisés en appelant la fonction [**InitAtomTable**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) . Toutefois, si l’application appelle **InitAtomTable**, elle doit le faire avant d’appeler d’autres fonctions de gestion Atom.

## <a name="atom-types"></a>Types Atom

Les applications peuvent créer deux types d’atomes : les atomes de chaînes et les atomes d’entiers. Les valeurs des atomes d’entiers et des atomes de chaînes ne se chevauchent pas. par conséquent, les deux types d’atomes peuvent être utilisés dans le même bloc de code.

Plusieurs fonctions acceptent des chaînes ou des atomes en tant que paramètres. Lors du passage d’un Atom à ces fonctions, une application peut utiliser la macro [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) pour convertir l’atome en un format qui peut être utilisé par la fonction.

Les sections suivantes décrivent les types Atom.

-   [Atomes de chaînes](#string-atoms)
-   [Atomes d’entiers](#integer-atoms)

### <a name="string-atoms"></a>Atomes de chaînes

Lorsque les applications passent des chaînes terminées par un caractère NULL aux fonctions [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)et [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) , elles reçoivent des *atomes de chaînes* (entiers 16 bits) en retour. Les atomes de chaînes ont les propriétés suivantes :

-   Les valeurs des atomes de chaînes se trouvent dans la plage 0xC000 (MAXINTATOM) à 0xFFFF.
-   La casse n’est pas significative dans les recherches d’un nom Atom dans une table Atom. En outre, l’ensemble de la chaîne doit correspondre dans une opération de recherche ; aucune correspondance de sous-chaîne n’est effectuée.
-   La taille de la chaîne associée à un Atom de chaîne ne peut pas dépasser 255 octets. Cette limitation s’applique à toutes les fonctions Atom.
-   Un *nombre de références* est associé à chaque nom Atom. Le nombre est incrémenté chaque fois que le nom Atom est ajouté à la table et décrémenté chaque fois que le nom Atom est supprimé de celui-ci. Cela empêche que différents utilisateurs du même atome de chaîne détruisent les noms Atom de l’autre. Lorsque le nombre de références pour un nom Atom est égal à zéro, le système supprime l’atome et le nom Atom de la table.

### <a name="integer-atoms"></a>Atomes d’entiers

Les atomes d’entiers diffèrent des atomes de chaînes des manières suivantes :

-   Les valeurs des atomes d’entiers se trouvent dans la plage 0x0001 à 0xBFFF (**MAXINTATOM**– 1).
-   La représentation sous forme de chaîne d’un Atom entier est \# *dddd*, où les valeurs représentées par *dddd* sont des chiffres décimaux. Les zéros non significatifs sont ignorés.
-   Aucun nombre de références ou surcharge de stockage n’est associé à un Atom entier.

## <a name="atom-creation-and-usage-count"></a>Création et nombre d’utilisations Atom

Une application crée un Atom local en appelant la fonction [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) ; elle crée un atome global en appelant la fonction [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) . Les deux fonctions requièrent un pointeur vers une chaîne. Le système recherche la chaîne dans la table Atom appropriée et retourne l’atome correspondant à l’application. Dans le cas d’un Atom de chaîne, si la chaîne réside déjà dans la table Atom, le système incrémente le nombre de références pour la chaîne pendant ce processus.

Les appels répétés pour ajouter le même nom Atom retournent le même Atom. Si le nom Atom n’existe pas dans la table quand [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) est appelé, le nom Atom est ajouté à la table et un nouvel atome est retourné. S’il s’agit d’un Atom de chaîne, son décompte de références est également défini sur un.

Une application doit appeler la fonction [**DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) lorsqu’elle n’a plus besoin d’utiliser un Atom local ; elle doit appeler la fonction [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) lorsqu’elle n’a plus besoin d’un atome global. Dans le cas d’un atome de chaîne, l’une de ces fonctions réduit d’une unité le décompte de références de l’atome correspondant. Lorsque le nombre de références atteint zéro, le système supprime le nom Atom de la table.

Le nom Atom d’un Atom de chaîne reste dans la table Atom globale tant que son décompte de références est supérieur à zéro, même après que l’application qui l’a placé dans la table se termine. Une table Atom locale est détruite lorsque l’application associée se termine, quel que soit le nombre de références des atomes de la table.

## <a name="atom-table-queries"></a>Requêtes Atom-Table

Une application peut déterminer si une chaîne particulière figure déjà dans une table Atom à l’aide de la fonction [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) ou [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) . Ces fonctions recherchent dans une table Atom la chaîne spécifiée et, si la chaîne y figure, retournent l’atome correspondant.

Une application peut utiliser la fonction [**GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) ou [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) pour extraire une chaîne de nom Atom d’une table Atom, à condition que l’atome corresponde à la chaîne recherchée. Les deux fonctions copient la chaîne Atom-Name de l’Atom spécifié dans une mémoire tampon et retournent la longueur de la chaîne qui a été copiée. **GetAtomName** récupère une chaîne de nom Atom à partir d’une table Atom locale et **GlobalGetAtomName** récupère une chaîne de nom Atom à partir de la table Atom globale.

## <a name="atom-string-formats"></a>Formats de chaîne Atom

Les fonctions [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw), [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma), [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)et [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) prennent un pointeur vers une chaîne terminée par le caractère null. Une application peut spécifier ce pointeur de l’une des manières suivantes.



|     Format chaîne               |    Description                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*jjjj*           | Entier spécifié comme une chaîne décimale. Utilisé pour créer ou Rechercher un Atom entier.                  |
| *nom Atom de chaîne* | Nom Atom de chaîne. Permet d’ajouter un nom Atom de chaîne à une table Atom et de recevoir un Atom en retour. |



 

 

 
