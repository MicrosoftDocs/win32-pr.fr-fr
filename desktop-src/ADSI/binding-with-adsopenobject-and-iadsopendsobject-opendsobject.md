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
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="339d9-105">Liaison avec ADsOpenObject et IADsOpenDSObject :: OpenDSObject</span><span class="sxs-lookup"><span data-stu-id="339d9-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="339d9-106">La fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) sont utilisées pour lier des objets de service d’annuaire lorsque d’autres informations d’identification doivent être spécifiées et lorsque le chiffrement des données est requis.</span><span class="sxs-lookup"><span data-stu-id="339d9-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="339d9-107">Les informations d’identification du thread appelant doivent être utilisées dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="339d9-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="339d9-108">Toutefois, si d’autres informations d’identification doivent être utilisées, vous devez utiliser la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="339d9-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="339d9-109">Si d’autres informations d’identification sont utilisées, il est important de ne pas mettre en cache le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="339d9-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="339d9-110">Plusieurs opérations de liaison peuvent être effectuées en spécifiant le nom d’utilisateur et le mot de passe de la première opération de liaison, puis en spécifiant uniquement le nom d’utilisateur dans les liaisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="339d9-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="339d9-111">Le système configure une session sur le premier appel et utilise la même session sur les appels de liaison suivants, à condition que les conditions suivantes soient remplies :</span><span class="sxs-lookup"><span data-stu-id="339d9-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="339d9-112">Le même nom d’utilisateur dans chaque opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="339d9-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="339d9-113">Implémentez une liaison sans serveur ou établissez une liaison avec le même serveur dans chaque opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="339d9-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="339d9-114">Maintenez une session ouverte en maintenant la valeur sur une référence d’objet à partir de l’une des opérations de liaison.</span><span class="sxs-lookup"><span data-stu-id="339d9-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="339d9-115">La session est fermée lorsque la référence du dernier objet est libérée.</span><span class="sxs-lookup"><span data-stu-id="339d9-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="339d9-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) utilisent les [interfaces SSPI (Security Support Provider interfaces)](/windows/desktop/SecAuthN/sspi) de Windows NT pour offrir plus de souplesse dans les options d’authentification.</span><span class="sxs-lookup"><span data-stu-id="339d9-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="339d9-117">Le principal avantage de l’utilisation de ces interfaces est de fournir différents types d’authentification à Active Directory clients et de chiffrer la session.</span><span class="sxs-lookup"><span data-stu-id="339d9-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="339d9-118">Actuellement, ADSI ne permet pas de transmettre des certificats.</span><span class="sxs-lookup"><span data-stu-id="339d9-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="339d9-119">Par conséquent, vous pouvez utiliser SSL pour le chiffrement, puis Kerberos, NTLM ou une authentification simple, selon la façon dont les indicateurs sont définis sur le paramètre *dwReserved* .</span><span class="sxs-lookup"><span data-stu-id="339d9-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="339d9-120">Vous ne pouvez pas demander un fournisseur SSPI spécifique dans ADSI, bien que vous obteniez toujours le protocole de préférence le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="339d9-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="339d9-121">Dans le cas d’une liaison client Windows à un ordinateur exécutant Windows, le protocole est Kerberos.</span><span class="sxs-lookup"><span data-stu-id="339d9-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="339d9-122">Le fait de ne pas autoriser un certificat pour l’authentification est acceptable dans le cas d’une page Web, car l’authentification se produit avant l’exécution de la page Web.</span><span class="sxs-lookup"><span data-stu-id="339d9-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="339d9-123">Bien que les opérations d’ouverture vous permettent de spécifier un utilisateur et un mot de passe, vous ne devez pas le faire.</span><span class="sxs-lookup"><span data-stu-id="339d9-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="339d9-124">Au lieu de cela, ne spécifiez pas d’informations d’identification et utilisez implicitement les informations d’identification du contexte de sécurité de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="339d9-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="339d9-125">Pour effectuer une liaison à un objet d’annuaire à l’aide des informations d’identification de l’appelant avec [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), spécifiez **null** pour le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="339d9-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="339d9-126">Enfin, pour établir une liaison sans authentification, utilisez l’indicateur de **\_ non- \_ authentification ADS** .</span><span class="sxs-lookup"><span data-stu-id="339d9-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="339d9-127">Aucune authentification n’indique que l’interface ADSI tente de se connecter en tant qu’utilisateur anonyme à l’objet cible et n’effectue aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="339d9-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="339d9-128">Cela équivaut à demander une liaison anonyme dans LDAP et indique que tous les utilisateurs sont inclus dans le contexte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="339d9-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="339d9-129">Si les indicateurs d’authentification ont la valeur zéro, ADSI effectue une liaison simple, envoyée sous forme de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="339d9-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="339d9-130">Si un nom d’utilisateur et un mot de passe sont spécifiés sans spécifier d’indicateurs d’authentification, le nom d’utilisateur et le mot de passe sont transmis sur le réseau en texte clair, ce qui constitue un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="339d9-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="339d9-131">Ne spécifiez pas de nom d’utilisateur ni de mot de passe sans spécifier les indicateurs d’authentification.</span><span class="sxs-lookup"><span data-stu-id="339d9-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="339d9-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="339d9-132">Examples</span></span>

<span data-ttu-id="339d9-133">L’exemple de code Visual Basic suivant montre comment utiliser la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="339d9-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="339d9-134">L’exemple de code C++ suivant montre comment utiliser la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="339d9-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


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



<span data-ttu-id="339d9-135">L’interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) peut également être utilisée en C++, mais elle duplique la fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="339d9-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="339d9-136">L’exemple de code C++ suivant montre comment utiliser l’interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) pour effectuer la même opération de liaison que dans l’exemple de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="339d9-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


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



 

 