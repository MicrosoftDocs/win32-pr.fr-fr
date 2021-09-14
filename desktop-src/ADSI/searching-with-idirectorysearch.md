---
title: Recherche avec l’interface IDirectorySearch
description: L’interface IDirectorySearch fournit une interface de haut niveau et de faible surcharge pour l’interrogation des données d’un répertoire ou d’un catalogue global.
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- Recherche à l’aide de l’interface ADSI de l’interface IDirectorySearch
- Requêtes ADSI, interfaces de requête, IDirectorySearch
- ADSI ADSI, exemple de code C/C++, recherche dans un répertoire avec IDirectorySearch
- Interface ADSI IDirectorySearch, utilisation de pour rechercher un répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2738e163f672fb0000275e2fb9d885442ae6693
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122094"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>Recherche avec l’interface IDirectorySearch

L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fournit une interface de haut niveau et de faible surcharge pour l’interrogation des données d’un répertoire ou d’un catalogue global. L’interface com **IDirectorySearch** ne peut être utilisée qu’avec un vtable et, par conséquent, n’est pas disponible pour les environnements de développement basés sur Automation.

**Pour effectuer une recherche**

1.  Effectuer une liaison à un objet dans l’annuaire.
2.  Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer le pointeur [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .
3.  Exécutez la recherche à l’aide du pointeur [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Appelez la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) et transmettez un filtre de recherche, les noms d’attributs demandés et d’autres paramètres.

Pour plus d’informations sur la syntaxe de filtre de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).

L’exécution de la requête est spécifique au fournisseur. Avec certains fournisseurs, l’exécution réelle de la requête ne se produit pas tant que [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) n’est pas appelé. L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fonctionne avec les filtres de recherche directement. ni le dialecte SQL ni le dialecte LDAP ne sont requis.

L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fournit des méthodes pour énumérer le jeu de résultats, ligne par ligne. La méthode [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) récupère la première ligne et [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) vous ramène à la ligne suivante de la ligne actuelle. Une fois que vous avez atteint la dernière ligne, l’appel de ces méthodes retourne le code d’erreur S de \_ \_ \_ lignes. À l’inverse, [**IDirectorySearch :: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) vous ramène une ligne à la fois. \_ \_ \_ La valeur renvoyée par des lignes est trop grande pour indiquer que vous avez atteint la première ligne du jeu de résultats. Ces méthodes opèrent sur le jeu de résultats, résidant en mémoire, sur le client. Ainsi, lorsque des recherches paginées et asynchrones sont effectuées et que l' \_ option des résultats du cache \_ est désactivée, le défilement vers l’arrière peut avoir des conséquences inattendues.

Une fois que vous avez localisé la ligne appropriée, appelez [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) pour obtenir des éléments de données, colonne par colonne. Pour chaque appel, vous transmettez le nom de la colonne qui vous intéresse. L’élément de données retourné est un pointeur vers une structure de [**\_ \_ colonne de recherche ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) . **GetColumn** alloue cette structure pour vous, mais vous devez la libérer à l’aide de [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn). Appelez [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) pour terminer l’opération de recherche.

**Pour effectuer une recherche dans les annuaires**

1.  Liaison à un fournisseur LDAP. Il peut s’agir d’un contrôleur de domaine ou d’un fournisseur de catalogue global.
2.  Récupérez l’interface com [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) à l’aide d’un appel à [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)); Cette opération a peut-être été effectuée à l’étape 1 pendant la liaison initiale.

    Si vous le souhaitez, appelez [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) pour sélectionner les options de gestion des résultats de votre recherche.

3.  Appelez [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch). Selon les options définies dans [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) , cela peut ou non commencer à exécuter la requête.
4.  Appelez [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) pour déplacer l’index de ligne (interne vers [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) vers la première ligne.
5.  Lisez les données de la ligne à l’aide de [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn), puis appelez [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) pour libérer la mémoire allouée par **GetColumn**.
6.  Répétez l’étape 5 jusqu’à ce que toutes les données soient récupérées à partir du résultat de la recherche, ou jusqu’à ce que la méthode [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) renvoie des \_ lignes de publicités \_ \_ .
7.  Appelez [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) et [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) lorsque vous avez terminé.

L’exemple de code suivant illustre ce scénario. Pour démarrer la liaison à ADSI, appelez la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



Cela fournit un pointeur vers l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

Maintenant qu’il existe une interface COM pour une instance IDirectoryInterface, appelez [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference).

Générez un tableau de noms d’attributs pour préparer l’appel de la fonction [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . Les noms d’attributs sont définis dans le schéma de Active Directory. Pour plus d’informations sur la définition de schéma, consultez [modèle de schéma ADSI](adsi-schema-model.md). Les noms d’attributs répertoriés sont retournés, s’ils sont pris en charge par l’objet, comme le jeu de résultats de la recherche.


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



À présent, appelez la fonction [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) . La recherche ne s’exécute pas tant que vous n’avez pas appelé la méthode [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



Appelez [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) pour itérer les lignes dans le résultat. Chaque ligne est ensuite interrogée pour obtenir l’attribut « Description ». Si l’attribut est trouvé, il est affiché.


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



Pour mettre fin à la recherche, appelez la méthode [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) .

Sachez que si une taille de page n’est pas définie, la valeur de [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) se bloque jusqu’à ce que le jeu de résultats entier soit renvoyé au client. Si la taille de la page est définie, la valeur de **GetNextRow** se bloque jusqu’à ce que la première page (taille de page = nombre de lignes dans une page) soit retournée. Si la taille de la page est définie et que la requête doit être triée et que vous n’effectuez pas de recherche sur au moins un attribut indexé, la valeur taille de la page est ignorée et le serveur calcule le jeu de résultats entier avant de retourner les données. Cela a pour effet de bloquer la **GetNextRow** jusqu’à la fin de la requête.

> [!Note]  
> Pour modifier cette requête d’une recherche de répertoire à une recherche de catalogue global, l’appel [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) est modifié.

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 