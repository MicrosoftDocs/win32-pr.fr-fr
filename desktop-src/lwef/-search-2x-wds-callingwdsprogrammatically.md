---
title: Appeler WDS par programmation
description: Microsoft Windows Desktop Search (WDS) 2. x peut être interrogé par programme à l’aide des méthodes ExecuteQuery et ExecuteSQLQuery dans l’interface ISearchDesktop.
ms.assetid: 38426f63-2039-410e-8c70-ebd9fc269d74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8879001bcf284affd03ff472ac9327445b799acd44465b5bae9a8cb2d819b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976899"
---
# <a name="calling-wds-programmatically"></a>Appeler WDS par programmation

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

Microsoft Windows Desktop Search (WDS) 2. x peut être interrogé par programme à l’aide des méthodes **ExecuteQuery** et **ExecuteSQLQuery** dans l’interface [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) . La méthode **ExecuteQuery** retourne un jeu d’enregistrements à partir de l’index en fonction du texte de la requête, des colonnes et des restrictions passées en tant que paramètres. la méthode **ExecuteSQLQuery** retourne également un jeu d’enregistrements de résultats, mais requiert la transmission de la commande exacte langage SQL (SQL). **ExecuteQuery** doit être utilisé dans la plupart des scénarios.

## <a name="regular-queries"></a>Requêtes régulières

Les requêtes régulières sont celles qui sont tapées dans la zone d’entrée WDS par l’utilisateur, y compris la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md). La requête est transmise à **ExecuteQuery** avec les colonnes de [schéma](-search-2x-wds-schematable.md) WDS 2. x à retourner, la colonne et l’ordre de tri des résultats et toutes les clauses pour limiter les résultats par.

La méthode se présente sous la forme :

`HRESULT ExecuteQuery(LPCWSTR lpcwstrQuery, LPCWSTR lpcwstrColumn, LPCWSTR lpcwstrSort, LPCWSTR lpcwstrRestriction, Recordset **ppiRs);`



| Sens | Variable           | Description                                                                                                                                                                                   |
|-----------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dans        | lpcwstrQuery       | Texte de la requête. cette requête est identique à une requête tapée dans la zone de texte rechercher de l’interface utilisateur Windows Desktop search. <br/> Par exemple : `"from:Zara dinner plans"`<br/> |
| Dans        | lpcwstrColumn      | Colonnes à inclure, séparées par des virgules. <br/> Par exemple : `"DocTitle, Url"`<br/>                                                                                            |
| Dans        | lpcwstrSort        | Colonne de remplacement dans laquelle effectuer le tri, suivi de ASC pour l’ordre croissant ou DESC pour l’ordre décroissant. <br/> Par exemple : `"LastAuthor DESC"`<br/>                                                  |
| Dans        | lpcwstrRestriction | Restrictions relatives à l’ajout de clauses where dans le Windows Desktop Search select. <br/> Par exemple : `"Contains(LastAuthor, 'Bill')"`<br/>                                       |
| Sortie       | ppiRs              | Jeu d’enregistrements résultant<br/>                                                                                                                                                           |



 

## <a name="sql-queries"></a>Requêtes SQL

La méthode **ISearchDesktop.ExecuteSQLQuery** est utilisée pour envoyer des requêtes de base de données WDS directes. la syntaxe des requêtes est similaire à celle utilisée pour SharePoint Server, ainsi que la possibilité d’utiliser des clauses de groupe de SQL de style Monarch. La requête est exécutée sur l’index exactement telle qu’elle est transmise sans traitement supplémentaire de la syntaxe de requête avancée comme le fait l’API ExecuteQuery.

https://msdn.microsoft.com/library/default.asp?url=/library/spssdk/html/\_tahoe\_search\_sql\_syntax.asp

La méthode se présente sous la forme :

`HRESULT ExecuteSQLQuery(LPCWSTR lpcwstrSQL, Recordset **ppiRs);`



| Sens | Variable   | Description                                    |
|-----------|------------|------------------------------------------------|
| Dans        | lpcwstrSQL | SQL requête à exécuter sur l’index WDS |
| Sortie       | ppiRs      | Jeu d’enregistrements résultant                       |



 

Ressources :

-   Fichiers de prise en charge pour l’interface ISearchDesktop : https://addins.msn.com/support/WDSSDK.zip
-   Exemple C# ISearchDesktop : https://addins.msn.com/support/WDSSample.zip

## <a name="sample-c-code"></a>Exemple de code C++

> [!Note]
>
> CE CODE ET CES INFORMATIONS SONT FOURNIS « EN L’ÉTAT », SANS GARANTIE D’AUCUNE SORTE, EXPRESSE OU IMPLICITE, Y COMPRIS, MAIS SANS S’Y LIMITER, LES GARANTIES IMPLICITES DE QUALITÉ MARCHANDE ET/OU D’ADÉQUATION À UN USAGE PARTICULIER.
>
> Copyright (C) Microsoft. All rights reserved.

 


```
#include <stdio.h>
#include <wchar.h>
#include <windows.h>
#include <msnldl.h>
#include <adoint.h>
#include <adoguids.h>
 
HRESULT TestExecuteQuery(ISearchDesktop *psd)
{
ADORecordset *prs = NULL;
 
    HRESULT hr;
 
    hr = psd->ExecuteQuery( L"ToName:Moishe", 
                            L"DocTitle,DocFormat", 
                            L"PrimaryDate DESC", 
                            L"Contains('text')", 
                            &prs);
    if (SUCCEEDED(hr))
        prs->Release();
    return hr;
}
 
HRESULT TestExecuteSQLQuery(ISearchDesktop *psd)
{
    ADORecordset *prs = NULL;
    HRESULT hr;

    hr = psd->ExecuteSQLQuery(L"select DocTitle from MyIndex..Scope() where contains('text')", &prs);

    if (SUCCEEDED(hr))
      prs->Release();
    return hr;
}
 
extern "C" int __cdecl wmain( int argc, WCHAR * argv[] )
{
    SCODE sc = CoInitialize(0);
    ISearchDesktop *psd = NULL;
    HRESULT         hr;
     
    if (SUCCEEDED(hr = CoCreateInstance(__uuidof(SearchDesktop), NULL, CLSCTX_INPROC_SERVER, 
                                        __uuidof(ISearchDesktop), (void**)&psd)))
          {
             TestExecuteSQLQuery(psd);
             TestExecuteQuery(psd);
             psd->Release();
          }
          CoUninitialize();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Syntaxe de requête avancée](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Types perçus](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Appel de WDS à partir de pages Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

