---
title: Liaison avec ADsOpenObject et IADsOpenDSObject OpenDSObject
description: La fonction ADsOpenObject et la méthode OpenDSObject IADsOpenDSObject sont utilisées pour lier des objets de service d’annuaire lorsque d’autres informations d’identification doivent être spécifiées et lorsque le chiffrement des données est requis.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Liaison avec ADsOpenObject et IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI, utilisation de, liaison avec ADsOpenObject et IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031850"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Liaison avec ADsOpenObject et IADsOpenDSObject :: OpenDSObject

La fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) sont utilisées pour lier des objets de service d’annuaire lorsque d’autres informations d’identification doivent être spécifiées et lorsque le chiffrement des données est requis.

Les informations d’identification du thread appelant doivent être utilisées dans la mesure du possible. Toutefois, si d’autres informations d’identification doivent être utilisées, vous devez utiliser la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . Si d’autres informations d’identification sont utilisées, il est important de ne pas mettre en cache le mot de passe. Plusieurs opérations de liaison peuvent être effectuées en spécifiant le nom d’utilisateur et le mot de passe de la première opération de liaison, puis en spécifiant uniquement le nom d’utilisateur dans les liaisons suivantes. Le système configure une session sur le premier appel et utilise la même session sur les appels de liaison suivants, à condition que les conditions suivantes soient remplies :

-   Le même nom d’utilisateur dans chaque opération de liaison.
-   Implémentez une liaison sans serveur ou établissez une liaison avec le même serveur dans chaque opération de liaison.
-   Maintenez une session ouverte en maintenant la valeur sur une référence d’objet à partir de l’une des opérations de liaison. La session est fermée lorsque la référence du dernier objet est libérée.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) utilisent les [interfaces SSPI (Security Support Provider interfaces)](/windows/desktop/SecAuthN/sspi) de Windows NT pour offrir plus de souplesse dans les options d’authentification. Le principal avantage de l’utilisation de ces interfaces est de fournir différents types d’authentification à Active Directory clients et de chiffrer la session. Actuellement, ADSI ne permet pas de transmettre des certificats. Par conséquent, vous pouvez utiliser SSL pour le chiffrement, puis Kerberos, NTLM ou une authentification simple, selon la façon dont les indicateurs sont définis sur le paramètre *dwReserved* .

Vous ne pouvez pas demander un fournisseur SSPI spécifique dans ADSI, bien que vous obteniez toujours le protocole de préférence le plus élevé. Dans le cas d’une liaison client Windows à un ordinateur exécutant Windows, le protocole est Kerberos. Le fait de ne pas autoriser un certificat pour l’authentification est acceptable dans le cas d’une page Web, car l’authentification se produit avant l’exécution de la page Web.

Bien que les opérations d’ouverture vous permettent de spécifier un utilisateur et un mot de passe, vous ne devez pas le faire. Au lieu de cela, ne spécifiez pas d’informations d’identification et utilisez implicitement les informations d’identification du contexte de sécurité de l’appelant. Pour effectuer une liaison à un objet d’annuaire à l’aide des informations d’identification de l’appelant avec [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), spécifiez **null** pour le nom d’utilisateur et le mot de passe.

Enfin, pour établir une liaison sans authentification, utilisez l’indicateur de **\_ non- \_ authentification ADS** . Aucune authentification n’indique que l’interface ADSI tente de se connecter en tant qu’utilisateur anonyme à l’objet cible et n’effectue aucune authentification. Cela équivaut à demander une liaison anonyme dans LDAP et indique que tous les utilisateurs sont inclus dans le contexte de sécurité.

Si les indicateurs d’authentification ont la valeur zéro, ADSI effectue une liaison simple, envoyée sous forme de texte en clair.

> [!Caution]  
> Si un nom d’utilisateur et un mot de passe sont spécifiés sans spécifier d’indicateurs d’authentification, le nom d’utilisateur et le mot de passe sont transmis sur le réseau en texte clair, ce qui constitue un risque pour la sécurité. Ne spécifiez pas de nom d’utilisateur ni de mot de passe sans spécifier les indicateurs d’authentification.

 

## <a name="examples"></a>Exemples

L’exemple de code Visual Basic suivant montre comment utiliser la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



L’exemple de code C++ suivant montre comment utiliser la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



L’interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) peut également être utilisée en C++, mais elle duplique la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

L’exemple de code C++ suivant montre comment utiliser l’interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) pour effectuer la même opération de liaison que dans l’exemple de code ci-dessus.


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 