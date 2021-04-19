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
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513742"
---
# <a name="performing-an-attribute-scope-query"></a><span data-ttu-id="b152e-105">Exécution d’une requête d’étendue d’attribut</span><span class="sxs-lookup"><span data-stu-id="b152e-105">Performing an Attribute Scope Query</span></span>

<span data-ttu-id="b152e-106">La requête d’étendue d’attribut est une préférence de recherche qui permet de rechercher les attributs de nom unique d’un objet à effectuer.</span><span class="sxs-lookup"><span data-stu-id="b152e-106">The attribute scope query is a search preference that enables a search of an object's distinguished name valued attributes to be performed.</span></span> <span data-ttu-id="b152e-107">L’attribut à rechercher peut être à valeur unique ou à valeurs multiples, mais il doit être du type de **\_ \_ chaîne DN ADS** .</span><span class="sxs-lookup"><span data-stu-id="b152e-107">The attribute to search can be either single or multi-valued, but must be of the **ADS\_DN\_STRING** type.</span></span> <span data-ttu-id="b152e-108">Lorsque la recherche est effectuée, ADSI énumère les valeurs de noms uniques de l’attribut et effectue la recherche sur les objets représentés par les noms uniques.</span><span class="sxs-lookup"><span data-stu-id="b152e-108">When the search is performed, ADSI will enumerate the distinguished name values of the attribute and perform the search on the objects represented by the distinguished names.</span></span> <span data-ttu-id="b152e-109">Par exemple, si une recherche étendue à l’attribut est effectuée à partir de l’attribut de [**membre**](/windows/desktop/ADSchema/a-member) d’un objet de groupe, ADSI énumère les noms uniques dans l’attribut de **membre** et recherche chacun des membres du groupe pour les critères de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b152e-109">For example, if an attribute scoped search is performed of the [**member**](/windows/desktop/ADSchema/a-member) attribute of a group object, ADSI will enumerate the distinguished names in the **member** attribute and search each of the members of the group for the specified search criteria.</span></span>

<span data-ttu-id="b152e-110">Si une requête de portée d’attribut est exécutée sur un attribut qui n’est pas de type **\_ \_ chaîne DN ADS**, la recherche échoue.</span><span class="sxs-lookup"><span data-stu-id="b152e-110">If an attribute scoped query is performed on an attribute that is not of type **ADS\_DN\_STRING**, the search will fail.</span></span> <span data-ttu-id="b152e-111">La requête d’étendue d’attribut requiert également que la préférence **\_ \_ \_ étendue de recherche SEARCHPREF ADS** soit définie sur la **\_ \_ base étendue ADS**.</span><span class="sxs-lookup"><span data-stu-id="b152e-111">The attribute scoped query also requires that the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference be set to **ADS\_SCOPE\_BASE**.</span></span> <span data-ttu-id="b152e-112">La préférence de l' **\_ \_ \_ étendue de recherche SEARCHPREF ADS** sera automatiquement définie sur la base de l' **\_ étendue \_ ADS**, mais si la préférence de l' **\_ \_ \_ étendue de recherche SEARCHPREF ADS** est définie sur une autre valeur, [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) échouera avec un **\_ \_ \_ paramètre incorrect E ADS**.</span><span class="sxs-lookup"><span data-stu-id="b152e-112">The **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference will automatically be set to **ADS\_SCOPE\_BASE**, but if the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** preference is set to any other value, [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) will fail with **E\_ADS\_BAD\_PARAMETER**.</span></span>

<span data-ttu-id="b152e-113">Les résultats d’une requête d’étendue d’attribut peuvent s’étendre sur plusieurs serveurs et un serveur peut ne pas retourner toutes les données demandées pour toutes les lignes retournées.</span><span class="sxs-lookup"><span data-stu-id="b152e-113">The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="b152e-114">Si cela se produit, lorsque la dernière ligne est récupérée en appelant [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ou [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI retourne **s \_ ADS \_ ERRORSOCCURRED** au lieu de **s \_ ad \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="b152e-114">If this occurs, when the last row is retrieved by calling [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED** instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

<span data-ttu-id="b152e-115">Pour spécifier une requête d’étendue d’attribut, définissez une option de recherche de **\_ \_ \_ requête d’attribut SEARCHPREF ADS** avec une valeur de **chaîne de \_ cas ADSTYPE \_ \_ ignore** définie sur le lDAPDisplayName de l’attribut à rechercher dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="b152e-115">To specify an attribute scope query, set an **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option with an **ADSTYPE\_CASE\_IGNORE\_STRING** value set to the lDAPDisplayName of the attribute to search in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="b152e-116">Cette opération est illustrée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b152e-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



<span data-ttu-id="b152e-117">L’exemple de code suivant montre comment utiliser l’option de recherche de **\_ \_ \_ requête d’attribut SEARCHPREF ADS** .</span><span class="sxs-lookup"><span data-stu-id="b152e-117">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBUTE\_QUERY** search option.</span></span>


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



<span data-ttu-id="b152e-118">Lorsque cette recherche est exécutée et que les résultats sont énumérés, elle retourne le **nom**, le **numéro de téléphone** et le numéro de **Bureau** de tous les objets utilisateur contenus dans la liste d’attributs de **membre** du groupe.</span><span class="sxs-lookup"><span data-stu-id="b152e-118">When this search is executed and the results are enumerated, it would return the **name**, **telephone number**, and **office number** of all of the user objects contained in the group's **member** attribute list.</span></span>

<span data-ttu-id="b152e-119">Gestion des erreurs : les résultats d’une requête d’étendue d’attribut peuvent s’étendre sur plusieurs serveurs et un serveur peut ne pas retourner toutes les données demandées pour toutes les lignes retournées.</span><span class="sxs-lookup"><span data-stu-id="b152e-119">Error handling: The results of an attribute-scope query may span multiple servers and a server may not return all the data requested for the all the rows returned.</span></span> <span data-ttu-id="b152e-120">Si cela se produit, lorsque la dernière ligne est récupérée en appelant [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ou [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI retourne **s \_ ADS \_ ERRORSOCCURRED**, au lieu de **s de \_ publicités \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="b152e-120">If this occurs, when the last row is retrieved by calling [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) or [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow), ADSI will return **S\_ADS\_ERRORSOCCURRED**, instead of **S\_ADS\_NOMORE\_ROWS**.</span></span>

 

 