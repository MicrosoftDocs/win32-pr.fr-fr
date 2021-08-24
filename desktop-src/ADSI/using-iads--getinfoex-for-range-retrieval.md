---
title: Utilisation d’IADs GetInfoEx pour la récupération de plages
description: La méthode IADs. GetInfoEx peut être utilisée pour récupérer une plage de valeurs d’attribut. La plage de valeurs à récupérer est spécifiée dans le tableau de noms d’attributs passé à la méthode.
ms.assetid: 2098862f-e5ec-4912-a941-8faceade22ee
ms.tgt_platform: multiple
keywords:
- Utilisation d’IADs GetInfoEx pour l’ADSI de récupération de plages
- IADs GetInfoEx ADSI, utilisation pour la récupération de plage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218f6cf8c0b0346a5b5554f870f5729bd55f8b221a3ebe0e425305333ee00cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082193"
---
# <a name="using-iadsgetinfoex-for-range-retrieval"></a>Utilisation de IADs :: GetInfoEx pour la récupération de plages

La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) peut être utilisée pour récupérer une plage de valeurs d’attribut. La plage de valeurs à récupérer est spécifiée dans le tableau de noms d’attributs passé à la méthode.

Les spécificateurs de plage pour une requête de propriété requièrent la forme suivante :


```C++
<property name>;range=<low range>-<high range>
```



où « &lt; nom &gt; de la propriété » est le **ldapDisplayName** de l’attribut, « &lt; la plage basse &gt; » est l’index de base zéro de la première valeur d’attribut à récupérer et « &lt; la plage supérieure &gt; » est l’index de base zéro de la dernière valeur d’attribut à récupérer. La valeur zéro est utilisée pour &lt; la « plage inférieure &gt; » pour spécifier la première entrée. Le caractère générique ( \* ) peut être utilisé pour la « &lt; plage supérieure &gt; » afin de spécifier toutes les entrées restantes.

L’exemple de code suivant contient une fonction qui montre comment utiliser la récupération de plages avec [**IADs :: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pour énumérer les membres d’un groupe.


```C++
HRESULT EnumGroupWithGetInfoEx(LPCWSTR pwszGroupDN, 
                               LPCWSTR pwszUsername, 
                               LPCWSTR pwszPassword)
{
    if(NULL == pwszGroupDN)
    {
        return E_POINTER;
    }
    
    HRESULT hr;
    IADs *pads;

    hr = ADsOpenObject( pwszGroupDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        const DWORD dwStep = 1000;
        DWORD dwLowRange;
        DWORD dwHighRange;
        WCHAR wszAttr[MAX_PATH];
        LPWSTR rgAttrs[1];

        rgAttrs[0] = wszAttr;

        dwLowRange = 0;
        dwHighRange = dwLowRange + (dwStep - 1);

        do
        {
            VARIANT var;

            // Perform this query with the "range=<lowRange>-<highRange>" range.
            swprintf_s(wszAttr, L"member;range=%d-%d", dwLowRange, dwHighRange);
    
            hr = ADsBuildVarArrayStr(rgAttrs, 1, &var);
            if(SUCCEEDED(hr))
            {
                hr = pads->GetInfoEx(var, 0);
                
                VariantClear(&var);

                if(SUCCEEDED(hr))
                {
                    hr = pads->Get(CComBSTR("member"), &var);
                    if(SUCCEEDED(hr))
                    {
                        if(var.vt == (VT_VARIANT | VT_ARRAY))
                        {
                            VARIANT *pVar;
                            long lLBound, lUBound;

                            // Get the array of VARIANTs.
                            hr = SafeArrayAccessData((SAFEARRAY*)(var.pparray), (void HUGEP* FAR*)&pVar);
                            if(SUCCEEDED(hr))
                            {
                                // Get the bounds for the array.
                                hr = SafeArrayGetLBound((SAFEARRAY*)(var.pparray), 1, &lLBound);
                                hr = SafeArrayGetUBound((SAFEARRAY*)(var.pparray), 1, &lUBound);

                                // Get the number of elements.
                                long cElements = lUBound - lLBound + 1;

                                // Enumerate the elements.
                                for(long i = 0; i < cElements; i++)
                                {
                                    switch(pVar[i].vt)
                                    {
                                    case VT_BSTR:
                                        wprintf(pVar[i].bstrVal); 
                                        wprintf(L"\n"); 
                                        break;
                                    }
                                }

                                // Release the array.
                                SafeArrayUnaccessData((SAFEARRAY*)(var.pparray));
                            }
                        }
                        // This occurs only if one element is retrieved.
                        else if (var.vt == VT_BSTR)
                        {
                            wprintf(var.bstrVal); 
                            wprintf(L"\n"); 
                        }

                        VariantClear(&var);
                    }

                    // Increment the high and low ranges to query for the next block of objects.
                    dwLowRange = dwHighRange + 1;
                    dwHighRange = dwLowRange + (dwStep - 1);
                }
            }
        }while(SUCCEEDED(hr));

        pads->Release();
    }

    return hr;
}
```



L’exemple de code suivant contient une fonction qui montre comment utiliser la récupération de plages avec [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) pour énumérer les membres d’un groupe.


```VB
Private Sub EnumGroupMembersWithGetInfoEx(strGroupDN As String, strUsername As String, strPassword As String)
    Dim oGroup As IADs
    Dim dso As IADsOpenDSObject
    
    On Error GoTo quit
        
    strPath = "LDAP://" & strGroupDN
    
    If "" <> strUsername Then
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oGroup = dso.OpenDSObject(strPath, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oGroup = GetObject(strPath)
    End If
    
    ' For compatibility with all operating systems, the number of objects
    ' retrieved by each query should not exceed 999. The number of objects
    ' to retrieve should be as close as possible to 999 to reduce the number
    ' of round trips to the server necessary to retrieve the objects.
    rangeStep = 999
    lowRange = 0
    highRange = lowRange + rangeStep
    
    Do
        ' Use the "member;range=<lowRange>-<highRange>" syntax.
        strCommandText = "member;range=" & lowRange & "-" & highRange
        Debug.Print "Current search command: " & strCommandText
        
        ' Load the specified range of members into the local cache. This will
        ' throw an error if the range exceeds the properties contained in the
        ' object. The "On Error GoTo quit" error handler will cause the loop
        ' to terminate when this happens.
        On Error GoTo quit
        oGroup.GetInfoEx Array(strCommandText), 0
        
        ' Enumerate the retrieved members.
        oMembers = oGroup.Get("member")
        If vbArray And VarType(oMembers) Then
            For Each oMember In oMembers
                ' Add the member.
                Debug.Print oMember
                nRetrieved = nRetrieved + 1
            Next
        Else
            ' oGroup.Get returned only one member, so add it to the list.
            Debug.Print oMembers
            nRetrieved = nRetrieved + 1
        End If
        
        ' Increment the high and low ranges to query for the next block of objects.
        lowRange = highRange + 1
        highRange = lowRange + rangeStep
    Loop While True
    
quit:
End Sub
```



 

 




