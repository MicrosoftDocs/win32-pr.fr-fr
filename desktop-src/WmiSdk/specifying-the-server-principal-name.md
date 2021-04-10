---
description: Le service d’authentification Kerberos spécifie le nom principal du serveur pour garantir l’identité de l’ordinateur auquel il se connecte.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Spécification du nom du principal du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114887"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="37d00-103">Spécification du nom du principal du serveur</span><span class="sxs-lookup"><span data-stu-id="37d00-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="37d00-104">Le service d’authentification Kerberos spécifie le nom principal du serveur pour garantir l’identité de l’ordinateur auquel il se connecte.</span><span class="sxs-lookup"><span data-stu-id="37d00-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="37d00-105">Spécifiez le nom principal du serveur dans l’appel à la méthode de script [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) en indiquant le nom de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="37d00-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="37d00-106">En C++, spécifiez le nom principal du serveur dans le paramètre *pServerPrincName* lors de l’appel de [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) pour le proxy.</span><span class="sxs-lookup"><span data-stu-id="37d00-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="37d00-107">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="37d00-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="37d00-108">Ce paramètre est requis pour que Kerberos prenne en charge l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="37d00-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="37d00-109">Toutefois, l’utilisation du nom principal du serveur par défaut n’autorise pas l’authentification mutuelle.</span><span class="sxs-lookup"><span data-stu-id="37d00-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="37d00-110">Les clients pour lesquels l’authentification mutuelle est critique doivent spécifier un nom de principal du serveur qui correspond à l’identité du serveur que le service WMI utilise.</span><span class="sxs-lookup"><span data-stu-id="37d00-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="37d00-111">Pour plus d’informations sur la définition de la sécurité du proxy et un exemple C++ indiquant comment définir le nom principal du serveur, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="37d00-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="37d00-112">Pour plus d’informations sur la définition du nom principal du serveur dans script et Visual Basic, consultez [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) et [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="37d00-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="37d00-113">Contrairement à la plupart des protocoles de sécurité pour Windows Management Instrumentation (WMI) et COM (Component Object Model), vous ne pouvez pas définir le principal du serveur dans un appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="37d00-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="37d00-114">Toutefois, vous pouvez définir le principal du serveur avec le paramètre *bstrAuthority* pour [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)ou le paramètre *pServerPrincName* pour [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="37d00-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="37d00-115">L’exemple de code de cette rubrique requiert l' \# instruction include suivante pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="37d00-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="37d00-116">L’exemple de code suivant montre comment définir le nom principal du serveur avec [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="37d00-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="37d00-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37d00-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37d00-118">Définition du service d’authentification à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="37d00-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="37d00-119">Définition de l’authentification à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="37d00-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="37d00-120">Définition de la sécurité sur IWbemServices et d’autres proxies</span><span class="sxs-lookup"><span data-stu-id="37d00-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
