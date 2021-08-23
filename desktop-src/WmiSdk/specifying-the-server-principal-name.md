---
description: Le service d’authentification Kerberos spécifie le nom principal du serveur pour garantir l’identité de l’ordinateur auquel il se connecte.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Spécification du nom du principal du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b3d05d6933653a7d2a1737d36f00f6ca65c39bd7739e5f2e9f4232eb507f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816422"
---
# <a name="specifying-the-server-principal-name"></a>Spécification du nom du principal du serveur

Le service d’authentification Kerberos spécifie le nom principal du serveur pour garantir l’identité de l’ordinateur auquel il se connecte. Spécifiez le nom principal du serveur dans l’appel à la méthode de script [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) en indiquant le nom de l’ordinateur distant. En C++, spécifiez le nom principal du serveur dans le paramètre *pServerPrincName* lors de l’appel de [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour le proxy. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

Ce paramètre est requis pour que Kerberos prenne en charge l’authentification mutuelle. Toutefois, l’utilisation du nom principal du serveur par défaut n’autorise pas l’authentification mutuelle. Les clients pour lesquels l’authentification mutuelle est critique doivent spécifier un nom de principal du serveur qui correspond à l’identité du serveur que le service WMI utilise. Pour plus d’informations sur la définition de la sécurité du proxy et un exemple C++ indiquant comment définir le nom principal du serveur, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

pour plus d’informations sur la définition du nom principal du serveur dans script et Visual Basic, consultez [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) et [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

contrairement à la plupart des protocoles de sécurité pour Windows Management Instrumentation (WMI) et COM (component Object Model), vous ne pouvez pas définir le principal du serveur dans un appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Toutefois, vous pouvez définir le principal du serveur avec le paramètre *bstrAuthority* pour [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)ou le paramètre *pServerPrincName* pour [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

L’exemple de code de cette rubrique requiert l' \# instruction include suivante pour compiler correctement.


```C++
#include <wbemidl.h>
```



L’exemple de code suivant montre comment définir le nom principal du serveur avec [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition du service d’authentification à l’aide de VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Définition de l’authentification à l’aide de C++](setting-authentication-using-c-.md)
</dt> <dt>

[Définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
