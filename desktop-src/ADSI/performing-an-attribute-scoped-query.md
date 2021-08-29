---
title: Exécution d’une requête d’étendue d’attribut
description: La requête d’étendue d’attribut est une préférence de recherche qui permet de rechercher les attributs de nom unique d’un objet à effectuer.
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- Exécution d’une requête d’étendue d’attribut ADSI
- ADSI, recherche, IDirectorySearch, autres options de recherche, requête d’étendue d’attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40251665f487919ce22b78057c6026324b49e33764545b55c38310265474484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637799"
---
# <a name="performing-an-attribute-scope-query"></a>Exécution d’une requête d’étendue d’attribut

La requête d’étendue d’attribut est une préférence de recherche qui permet de rechercher les attributs de nom unique d’un objet à effectuer. L’attribut à rechercher peut être à valeur unique ou à valeurs multiples, mais il doit être du type de **\_ \_ chaîne DN ADS** . Lorsque la recherche est effectuée, ADSI énumère les valeurs de noms uniques de l’attribut et effectue la recherche sur les objets représentés par les noms uniques. Par exemple, si une recherche étendue à l’attribut est effectuée à partir de l’attribut de [**membre**](/windows/desktop/ADSchema/a-member) d’un objet de groupe, ADSI énumère les noms uniques dans l’attribut de **membre** et recherche chacun des membres du groupe pour les critères de recherche spécifiés.

Si une requête de portée d’attribut est exécutée sur un attribut qui n’est pas de type **\_ \_ chaîne DN ADS**, la recherche échoue. La requête d’étendue d’attribut requiert également que la préférence **\_ \_ \_ étendue de recherche SEARCHPREF ADS** soit définie sur la **\_ \_ base étendue ADS**. La préférence de l' **\_ \_ \_ étendue de recherche SEARCHPREF ADS** sera automatiquement définie sur la base de l' **\_ étendue \_ ADS**, mais si la préférence de l' **\_ \_ \_ étendue de recherche SEARCHPREF ADS** est définie sur une autre valeur, [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) échouera avec un **\_ \_ \_ paramètre incorrect E ADS**.

Les résultats d’une requête d’étendue d’attribut peuvent s’étendre sur plusieurs serveurs et un serveur peut ne pas retourner toutes les données demandées pour toutes les lignes retournées. Si cela se produit, lorsque la dernière ligne est récupérée en appelant [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ou [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI retourne **s \_ ADS \_ ERRORSOCCURRED** au lieu de **s \_ ad \_ \_**.

Pour spécifier une requête d’étendue d’attribut, définissez une option de recherche de **\_ \_ \_ requête d’attribut SEARCHPREF ADS** avec une valeur de **chaîne de \_ cas ADSTYPE \_ \_ ignore** définie sur le lDAPDisplayName de l’attribut à rechercher dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Cette opération est illustrée dans l’exemple de code suivant.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



L’exemple de code suivant montre comment utiliser l’option de recherche de **\_ \_ \_ requête d’attribut SEARCHPREF ADS** .


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



Lorsque cette recherche est exécutée et que les résultats sont énumérés, elle retourne le **nom**, le **numéro de téléphone** et le numéro de **Bureau** de tous les objets utilisateur contenus dans la liste d’attributs de **membre** du groupe.

Gestion des erreurs : les résultats d’une requête d’étendue d’attribut peuvent s’étendre sur plusieurs serveurs et un serveur peut ne pas retourner toutes les données demandées pour toutes les lignes retournées. Si cela se produit, lorsque la dernière ligne est récupérée en appelant [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ou [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI retourne **s \_ ADS \_ ERRORSOCCURRED**, au lieu de **s de \_ publicités \_ \_**.

 

 