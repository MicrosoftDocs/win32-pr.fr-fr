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
# <a name="setting-authentication-using-c"></a>Définition de l’authentification à l’aide de C++

L’une des principales tâches de [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) pour WMI retourne un pointeur vers un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Via le proxy **IWbemServices** , vous pouvez accéder aux fonctionnalités de l’infrastructure WMI. Toutefois, le pointeur vers le proxy **IWbemServices** dispose de l’identité du processus d’application cliente et non de l’identité du processus **IWbemServices** . Par conséquent, si vous tentez d’accéder à **IWbemServices** avec le pointeur, vous pouvez recevoir un code d’accès refusé tel que **E \_ ACCESSDENIED**. Pour éviter l’erreur d’accès refusé, vous devez définir l’identité du nouveau pointeur avec un appel à l’interface [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .

Un fournisseur peut définir la sécurité sur un espace de noms afin qu’aucune donnée ne soit retournée, sauf si vous utilisez la confidentialité des paquets (**PktPrivacy**) dans votre connexion à cet espace de noms. Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau. Si vous essayez de définir un niveau d’authentification inférieur, vous obtiendrez un message d’accès refusé. Pour plus d’informations, consultez [définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md).

Pour plus d’informations sur la définition de l’authentification dans les scripts, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Définition de la sécurité sur une interface IUnknown distante

Dans certains cas, un plus grand nombre d’accès à un serveur qu’un simple pointeur vers un proxy est nécessaire. Dans certains cas, vous devrez peut-être obtenir une connexion sécurisée à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du proxy. À l’aide de **IUnknown**, vous pouvez interroger le système distant à la recherche d’interfaces et d’autres techniques nécessaires.

Lorsqu’un proxy se trouve sur un ordinateur distant, le serveur délègue tous les appels à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) du proxy à l’interface **IUnknown** . Par exemple, si vous appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un proxy et que l’interface demandée ne faisait pas partie du proxy, le proxy envoie l’appel au serveur distant. À son tour, le serveur distant vérifie la prise en charge de l’interface appropriée. Si le serveur prend en charge l’interface, COM marshale un nouveau proxy vers le client afin que l’application puisse utiliser la nouvelle interface.

Des problèmes surviennent si le client n’a pas les autorisations d’accès au serveur distant, mais utilise les informations d’identification d’un utilisateur qui exécute. Dans ce cas, toute tentative d’accès à [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le serveur distant échoue. La version finale du proxy échoue également, car l’utilisateur actuel n’a pas accès au serveur distant. Un symptôme de ce problème est un décalage d’un ou de deux secondes avant que l’application cliente ne fasse échouer la version finale du proxy. L’échec se produit parce que COM a tenté d’accéder au serveur distant à l’aide des paramètres de sécurité par défaut de l’utilisateur actuel, qui n’incluent pas les informations d’identification modifiées qui ont autorisé l’accès au serveur en premier lieu. Pour plus d’informations, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

Pour éviter l’échec de la connexion, utilisez [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour définir explicitement l’authentification de sécurité sur le pointeur retourné par [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). À l’aide de **CoSetProxyBlanket**, vous pouvez vous assurer que le serveur distant reçoit l’identité d’authentification correcte.

L’exemple de code suivant montre comment utiliser [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour accéder à une interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) distante.


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
> Lorsque vous définissez la sécurité sur l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) d’un proxy, com crée une copie du proxy qui ne peut pas être libérée tant que vous n’avez pas appelé [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’authentification dans WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
