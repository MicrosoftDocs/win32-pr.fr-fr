---
title: Comment effectuer une recherche à l’aide de VLV
description: Active Directory prend en charge les recherches de listes virtuelles (VLV, Virtual List View). Ce style de recherche est spécifiquement conçu pour les grands jeux de résultats et permet à une application d’afficher un sous-ensemble de milliers d’entrées sans avoir à récupérer chaque entrée.
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- Comment effectuer une recherche à l’aide de VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a24250c8e54ccb7917f86b193152c62810b93
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941369"
---
# <a name="how-to-search-using-vlv"></a>Comment effectuer une recherche à l’aide de VLV

Active Directory prend en charge les recherches de listes virtuelles (VLV, Virtual List View). Ce style de recherche est spécifiquement conçu pour les grands jeux de résultats et permet à une application d’afficher un sous-ensemble de milliers d’entrées sans avoir à récupérer chaque entrée.

Une recherche VLV peut être utilisée de deux façons distinctes. La première consiste à récupérer les attributs pour des entrées particulières en fonction d’un décalage numérique. Cette méthode est utile lors de la récupération des résultats de la recherche en réponse à une opération de défilement.

La deuxième façon d’utiliser les recherches VLV consiste à rechercher tout ou partie d’un attribut textuel et à afficher uniquement les résultats de la recherche. Voici un exemple d’utilisation de ce carnet d’adresses. Si l’utilisateur tape un « s », l’application peut utiliser une recherche VLV pour rechercher les entrées dont le nom commun commence par « s ». Si l’utilisateur ajoute ensuite un « m » à la « s », l’application peut utiliser une autre recherche VLV pour rechercher les entrées dont le nom commun commence par « SM ».

Pour effectuer une recherche VLV, demandez à ADSI d’utiliser le contrôle VLV. Pour ce faire, appelez la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) avec une option de recherche **\_ \_ VLV ADS SEARCHPREF** avec une valeur de **\_ preuve \_ spécifique ADSTYPE** . La **valeur \_ \_ spécifique de la preuve ADSTYPE** est un pointeur vers une structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) qui contient les données relatives à la recherche. La fonction exemple [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) montre comment définir ces deux préférences de recherche.

Toutes les recherches VLV doivent utiliser le tri des résultats côté serveur, qui est effectué en définissant le **\_ \_ Tri SEARCHPREF des publicités \_ sur** la préférence de recherche. Pour plus d’informations sur les préférences de recherche **\_ SEARCHPREF \_ \_ des publicités** , consultez [Tri des résultats de recherche avec IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).

Lorsqu’une recherche VLV est effectuée, une certaine quantité de métadonnées sur la recherche est retournée dans une colonne qui est extraite en appelant [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) avec l’identificateur de **\_ \_ réponse VLV ADS** . Ces données sont contenues dans une structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Les membres **dwContentCount** et **lpContextID** sont particulièrement importants. Le membre **dwContentCount** contient le nombre de résultats qui répondent aux critères de recherche VLV. Cette valeur peut être utilisée comme une estimation du nombre total d’éléments qui seraient renvoyés pour une recherche de ce type. Le membre **lpContextID** contient une valeur définie par le serveur qui peut être transmise à la recherche suivante pour identifier la recherche. L’utilisation de **lpContextID** peut améliorer les performances de recherche. Sachez que le **lpContextID** est une valeur définie par le serveur et que sa longueur est contenue dans le membre **dwContextIDLength** . Cette mémoire tampon est libérée quand la méthode [**IDirectorySearch :: FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) est appelée, de sorte que l’appelant doit allouer une mémoire tampon de la taille appropriée et copier et enregistrer le contenu de la mémoire tampon entre les recherches.

Pour plus d’informations sur le contrôle VLV LDAP, consultez [recherche à l’aide du contrôle VLV LDAP](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control).

Pour plus d’informations, consultez :

-   Obtention du nombre d’éléments
-   Recherche par décalage
-   Recherche par chaîne
-   [Exemple de code pour l’utilisation d’une recherche VLV](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>Obtention du nombre d’éléments

**Pour obtenir une estimation du nombre d’éléments qui seront retournés pour une recherche particulière, procédez comme suit.**

1.  Remplir une [**structure \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) avec toutes les valeurs zéro ou **null** .
2.  Remplissez les [**\_ \_ informations de SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) avec les valeurs suivantes.

    -   Définissez le membre **dwSearchPref** sur **ADS \_ SEARCHPREF \_ VLV**.
    -   Définissez le membre **vValue. dwType** sur **ADSTYPE \_ \_ specific**.
    -   Définissez le membre **vValue. providerspecific. dwLength** sur la taille de la [**structure \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
    -   Définissez le membre **vValue. providerspecific. lpValue** sur l’adresse de la [**structure \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) de l’étape 1.

3.  Remplissez une [**structure \_ SortKey ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) comme indiqué dans [Tri des résultats de recherche avec IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md) pour effectuer un tri sur l’attribut souhaité.
4.  Remplissez d' [**autres \_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pour ajouter la structure de valeurs de tri [**ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) aux préférences de recherche, comme indiqué dans [Tri des résultats de recherche avec IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).
5.  Ajoutez les autres préférences de recherche souhaitées et appelez [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) pour définir les préférences de recherche.
6.  Effectuez la recherche avec [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
7.  Récupérez la première ligne de résultats en appelant [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
8.  Appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) avec **la \_ \_ réponse VLV ADS** pour obtenir les métadonnées de recherche VLV.
9.  Cast du **pADsValues->providerspecific. lpValue** de la structure de [**\_ \_ colonne de recherche ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) en pointeur de structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Le membre **dwContentCount** de cette **structure \_ VLV ADS** contient le nombre approximatif d’éléments qui seraient renvoyés par une recherche de ce type.
10. Si d’autres recherches VLV du même type sont effectuées, effectuez une copie des données **lpContextID** et conservez-les pour la recherche VLV suivante.

La fonction exemple [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) montre comment procéder.

## <a name="searching-by-offset"></a>Recherche par décalage

Une chose qui effectue des recherches de VLV si rapide est qu’il est possible de rechercher un résultat spécifique à l’aide d’un décalage numérique. Par exemple, si une recherche se traduirait par 10 000 éléments retournés, une recherche VLV permet d’obtenir les informations d’environ l’élément 4072nd sans avoir à récupérer tous les éléments avant l’élément en question.

Les décalages sont spécifiés sous la forme d’un rapport entre le décalage et le nombre de contenu. Les ratios sont utiles, car le serveur n’a peut-être pas une estimation précise du nombre d’entrées qui existent dans la liste ou la taille de la liste peut être modifiée au moment où l’utilisateur la parcourt. Étant donné que vous devez indiquer le début et la fin de la liste, vous pouvez utiliser une valeur estimée pour le nombre de contenu dans la première demande de recherche, ainsi qu’une valeur de décalage. Le serveur utilise ces données pour calculer les décalages correspondants dans la liste, en fonction de son idée du nombre de contenu, qui est envoyé dans sa réponse au client via le membre **dwContentCount** de la [**structure \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Par exemple, si vous estimez que la taille de la liste est de 3000, et que vous souhaitez que le décalage soit la liste d’entrée 1500, vous devez définir **dwContentCount** sur 3000 et **dwOffset** sur 1500. Si le serveur estime que la taille réelle de la liste est de 4500, il recalcule le décalage à 2250 et retourne les nouvelles estimations dans **dwContentCount** et **dwOffset**.

> [!Note]
>
> Toutes les valeurs numériques d’une recherche VLV sont des approximations et ne doivent pas être utilisées pour les valeurs absolues. Par exemple, si vous émettez une recherche VLV pour le 50e élément dans un ratio de 100, il n’est pas garanti que vous obteniez l’élément intermédiaire exact.
>
> **Pour rechercher un élément particulier par décalage, procédez comme suit.**
>
> 1.  Remplissez une [**structure \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) avec les valeurs suivantes. Les membres supplémentaires de la structure doivent être définis sur zéro ou **null**.
>
>     -   Définissez le membre **dwContentCount** sur la valeur maximale du rapport des éléments à récupérer.
>     -   Affectez au membre **dwOffset** le ratio, par rapport à **dwContentCount**, de l’élément ou des éléments à récupérer.
>     -   Définissez le membre **lpContextID** sur l’adresse de la copie de la mémoire tampon de l’ID de contexte et **dwContextIDLength** sur la longueur, en octets, de la mémoire tampon de l’ID de contexte. Si aucun ID de contexte n’a été enregistré, les deux membres doivent avoir la valeur zéro ou avoir la **valeur null**.
>
> 2.  Définissez les préférences de recherche comme indiqué dans les étapes 2 à 5 de la procédure obtention du nombre d’éléments.
> 3.  Effectuez la recherche avec [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
> 4.  Récupérez la première ligne de résultats en appelant [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
> 5.  Appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) avec le nom de l’attribut à récupérer pour obtenir les données réelles de l’élément demandé.
> 6.  Appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) avec **la \_ \_ réponse VLV ADS** pour obtenir les métadonnées de recherche VLV.
> 7.  Cast du **pADsValues->providerspecific. lpValue** de la structure de [**\_ \_ colonne de recherche ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) en pointeur de structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
> 8.  Effectuez une copie des données **lpContextID** et conservez-les pour la prochaine recherche VLV.

 

La fonction exemple [**GetVLVItemText**](example-code-for-using-a-vlv-search.md) montre comment procéder.

Il est également possible de récupérer plusieurs lignes de données à l’aide d’un seul appel de recherche. Cette opération est effectuée à l’étape 1 en définissant les membres **dwBeforeCount** et **dwAfterCount** de la structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) de manière appropriée. Le membre **dwBeforeCount** contient le nombre d’éléments qui apparaissent dans la liste avant l’élément en question et le membre **dwAfterCount** contient le nombre d’éléments qui s’affichent dans la liste après à l’élément en question. Ces deux comptes excluent l’élément lui-même. par conséquent, la définition de **dwBeforeCount** sur 10 et **dwAfterCount** sur 10 entraîne un total de 21 éléments retournés. Cette option permet de mettre en cache les résultats de la recherche côté client.

## <a name="searching-by-string"></a>Recherche par chaîne

Il est également possible d’utiliser une recherche VLV pour rechercher des éléments qui ont un attribut de chaîne dont la valeur correspond à tout ou partie d’une chaîne sans avoir à récupérer tous les éléments. La correspondance de chaînes est exécutée par rapport à l’attribut spécifié dans [**la structure de \_ Tri des publicités de**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) la préférence de recherche **\_ SEARCHPREF \_ \_ de publicités** .

**Pour rechercher un élément particulier par chaîne, procédez comme suit.**

1.  Remplissez une [**structure \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) avec les valeurs suivantes. Les membres supplémentaires de la structure doivent être définis sur zéro ou **null**.

    -   Définissez le membre **pszTarget** sur un pointeur désignant une chaîne terminée par le caractère null qui contient la chaîne à rechercher.
    -   Définissez le membre **lpContextID** sur l’adresse de la copie de la mémoire tampon de l’ID de contexte et **dwContextIDLength** sur la longueur, en octets, de la mémoire tampon de l’ID de contexte. Si aucun ID de contexte n’a été enregistré, les deux membres doivent avoir la valeur zéro ou avoir la **valeur null**.

2.  Définissez les préférences de recherche comme indiqué dans les étapes 2 à 5 de la procédure obtention du nombre d’éléments.
3.  Effectuez la recherche avec [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
4.  Récupérez la première ligne de résultats en appelant [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
5.  Appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) avec le nom de l’attribut à récupérer pour obtenir les données réelles de l’élément demandé.
6.  Appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) avec **la \_ \_ réponse VLV ADS** pour obtenir les métadonnées de recherche VLV.
7.  Cast du **pADsValues->providerspecific. lpValue** de la structure de [**\_ \_ colonne de recherche ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) en pointeur de structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
8.  Effectuez une copie des données **lpContextID** et conservez-les pour la prochaine recherche VLV. Si nécessaire, le membre **dwOffset** contient l’index de base un du premier élément dont l’attribut de chaîne commence par la valeur spécifiée dans **pszTarget**.

La fonction exemple [**GetVLVItemsByString**](example-code-for-using-a-vlv-search.md) montre comment procéder.

De même que la recherche par index, il est également possible de récupérer plusieurs lignes de données à l’aide d’un seul appel de recherche. Cela s’effectue de la même manière en définissant les membres **dwBeforeCount** et **dwAfterCount** de la structure [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) de manière appropriée.

 

 