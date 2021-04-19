---
description: 'L’une des principales tâches de IWbemLocator :: ConnectServer pour WMI retourne un pointeur vers un proxy IWbemServices.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Définition de l’authentification à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518777"
---
# <a name="setting-authentication-using-c"></a><span data-ttu-id="413c2-103">Définition de l’authentification à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="413c2-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="413c2-104">L’une des principales tâches de [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) pour WMI retourne un pointeur vers un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="413c2-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="413c2-105">Via le proxy **IWbemServices** , vous pouvez accéder aux fonctionnalités de l’infrastructure WMI.</span><span class="sxs-lookup"><span data-stu-id="413c2-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="413c2-106">Toutefois, le pointeur vers le proxy **IWbemServices** dispose de l’identité du processus d’application cliente et non de l’identité du processus **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="413c2-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="413c2-107">Par conséquent, si vous tentez d’accéder à **IWbemServices** avec le pointeur, vous pouvez recevoir un code d’accès refusé tel que **E \_ ACCESSDENIED**.</span><span class="sxs-lookup"><span data-stu-id="413c2-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="413c2-108">Pour éviter l’erreur d’accès refusé, vous devez définir l’identité du nouveau pointeur avec un appel à l’interface [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="413c2-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="413c2-109">Un fournisseur peut définir la sécurité sur un espace de noms afin qu’aucune donnée ne soit retournée, sauf si vous utilisez la confidentialité des paquets (**PktPrivacy**) dans votre connexion à cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="413c2-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="413c2-110">Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau.</span><span class="sxs-lookup"><span data-stu-id="413c2-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="413c2-111">Si vous essayez de définir un niveau d’authentification inférieur, vous obtiendrez un message d’accès refusé.</span><span class="sxs-lookup"><span data-stu-id="413c2-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="413c2-112">Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="413c2-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="413c2-113">Pour plus d’informations sur la définition de l’authentification dans les scripts, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="413c2-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="413c2-114">Définition de la sécurité sur une interface IUnknown distante</span><span class="sxs-lookup"><span data-stu-id="413c2-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="413c2-115">Dans certains cas, un plus grand nombre d’accès à un serveur qu’un simple pointeur vers un proxy est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="413c2-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="413c2-116">Dans certains cas, vous devrez peut-être obtenir une connexion sécurisée à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du proxy.</span><span class="sxs-lookup"><span data-stu-id="413c2-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="413c2-117">À l’aide de **IUnknown**, vous pouvez interroger le système distant à la recherche d’interfaces et d’autres techniques nécessaires.</span><span class="sxs-lookup"><span data-stu-id="413c2-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="413c2-118">Lorsqu’un proxy se trouve sur un ordinateur distant, le serveur délègue tous les appels à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du proxy à l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="413c2-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="413c2-119">Par exemple, si vous appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un proxy et que l’interface demandée ne faisait pas partie du proxy, le proxy envoie l’appel au serveur distant.</span><span class="sxs-lookup"><span data-stu-id="413c2-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="413c2-120">À son tour, le serveur distant vérifie la prise en charge de l’interface appropriée.</span><span class="sxs-lookup"><span data-stu-id="413c2-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="413c2-121">Si le serveur prend en charge l’interface, COM marshale un nouveau proxy vers le client afin que l’application puisse utiliser la nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="413c2-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="413c2-122">Des problèmes surviennent si le client n’a pas les autorisations d’accès au serveur distant, mais utilise les informations d’identification d’un utilisateur qui exécute.</span><span class="sxs-lookup"><span data-stu-id="413c2-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="413c2-123">Dans ce cas, toute tentative d’accès à [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le serveur distant échoue.</span><span class="sxs-lookup"><span data-stu-id="413c2-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="413c2-124">La version finale du proxy échoue également, car l’utilisateur actuel n’a pas accès au serveur distant.</span><span class="sxs-lookup"><span data-stu-id="413c2-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="413c2-125">Un symptôme de ce problème est un décalage d’un ou de deux secondes avant que l’application cliente ne fasse échouer la version finale du proxy.</span><span class="sxs-lookup"><span data-stu-id="413c2-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="413c2-126">L’échec se produit parce que COM a tenté d’accéder au serveur distant à l’aide des paramètres de sécurité par défaut de l’utilisateur actuel, qui n’incluent pas les informations d’identification modifiées qui ont autorisé l’accès au serveur en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="413c2-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="413c2-127">Pour plus d’informations, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="413c2-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="413c2-128">Pour éviter l’échec de la connexion, utilisez [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour définir explicitement l’authentification de sécurité sur le pointeur retourné par [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="413c2-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="413c2-129">À l’aide de **CoSetProxyBlanket**, vous pouvez vous assurer que le serveur distant reçoit l’identité d’authentification correcte.</span><span class="sxs-lookup"><span data-stu-id="413c2-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="413c2-130">L’exemple de code suivant montre comment utiliser [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour accéder à une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) distante.</span><span class="sxs-lookup"><span data-stu-id="413c2-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> <span data-ttu-id="413c2-131">Lorsque vous définissez la sécurité sur l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) d’un proxy, com crée une copie du proxy qui ne peut pas être libérée tant que vous n’avez pas appelé [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="413c2-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="413c2-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="413c2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="413c2-133">Configuration de l’authentification dans WMI</span><span class="sxs-lookup"><span data-stu-id="413c2-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
