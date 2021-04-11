---
description: Les applications clientes spéciales peuvent appeler des opérations privilégiées.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Exécution d’opérations privilégiées à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318942"
---
# <a name="executing-privileged-operations-using-c"></a><span data-ttu-id="b1e36-103">Exécution d’opérations privilégiées à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="b1e36-103">Executing Privileged Operations Using C++</span></span>

<span data-ttu-id="b1e36-104">Les applications clientes spéciales peuvent appeler des opérations privilégiées.</span><span class="sxs-lookup"><span data-stu-id="b1e36-104">Special client applications might invoke privileged operations.</span></span> <span data-ttu-id="b1e36-105">Par exemple, une application peut permettre à un gestionnaire de redémarrer un ordinateur Office qui ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="b1e36-105">For example, an application could allow a manager to reboot an unresponsive office computer.</span></span> <span data-ttu-id="b1e36-106">À l’aide de Windows Management Instrumentation (WMI), vous pouvez exécuter une opération privilégiée en appelant le fournisseur WMI pour l’opération privilégiée.</span><span class="sxs-lookup"><span data-stu-id="b1e36-106">By using Windows Management Instrumentation (WMI), you can execute a privileged operation by calling the WMI provider for the privileged operation.</span></span>

<span data-ttu-id="b1e36-107">La procédure suivante décrit comment appeler un fournisseur pour une opération privilégiée.</span><span class="sxs-lookup"><span data-stu-id="b1e36-107">The following procedure describes how to call a provider for a privileged operation.</span></span>

<span data-ttu-id="b1e36-108">**Pour appeler un fournisseur pour une opération privilégiée**</span><span class="sxs-lookup"><span data-stu-id="b1e36-108">**To call a provider for a privileged operation**</span></span>

1.  <span data-ttu-id="b1e36-109">Obtenez des autorisations pour que le processus client exécute l’opération privilégiée.</span><span class="sxs-lookup"><span data-stu-id="b1e36-109">Obtain permissions for the client process to execute the privileged operation.</span></span>

    <span data-ttu-id="b1e36-110">En règle générale, un administrateur définit les autorisations à l’aide des outils d’administration système, avant d’exécuter le processus.</span><span class="sxs-lookup"><span data-stu-id="b1e36-110">Typically, an administrator sets the permissions using system administrative tools—prior to running the process.</span></span>

2.  <span data-ttu-id="b1e36-111">Obtenez l’autorisation pour le processus du fournisseur afin d’activer l’opération privilégiée.</span><span class="sxs-lookup"><span data-stu-id="b1e36-111">Obtain permission for the provider process to enable the privileged operation.</span></span>

    <span data-ttu-id="b1e36-112">En règle générale, vous pouvez définir des autorisations de fournisseur avec un appel à la fonction [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="b1e36-112">Typically, you can set provider permissions with a call to the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>

3.  <span data-ttu-id="b1e36-113">Obtenez l’autorisation pour le processus client pour activer l’opération privilégiée.</span><span class="sxs-lookup"><span data-stu-id="b1e36-113">Obtain permission for the client process to enable the privileged operation.</span></span>

    <span data-ttu-id="b1e36-114">Cette étape est nécessaire uniquement si le fournisseur est local pour le client.</span><span class="sxs-lookup"><span data-stu-id="b1e36-114">This step is necessary only if the provider is local to the client.</span></span> <span data-ttu-id="b1e36-115">Si le client et le fournisseur existent sur le même ordinateur, le client doit activer spécifiquement l’opération privilégiée à l’aide de l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1e36-115">If the client and provider exist on the same computer, the client must specifically enable the privileged operation by using one of the following techniques:</span></span>

    -   <span data-ttu-id="b1e36-116">Si le client possède le processus, le client peut utiliser [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour ajuster le jeton de processus avant d’appeler WMI.</span><span class="sxs-lookup"><span data-stu-id="b1e36-116">If the client owns the process, the client can use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to adjust the process token before calling WMI.</span></span> <span data-ttu-id="b1e36-117">Dans ce cas, vous n’avez pas besoin de coder davantage.</span><span class="sxs-lookup"><span data-stu-id="b1e36-117">In this case, you do not need to code any further.</span></span>
    -   <span data-ttu-id="b1e36-118">Si le client ne peut pas accéder au jeton client, le client peut utiliser la procédure suivante pour créer un jeton de thread et utiliser [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sur ce jeton.</span><span class="sxs-lookup"><span data-stu-id="b1e36-118">If the client cannot access the client token, the client can use the following procedure to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="b1e36-119">La procédure suivante décrit comment créer un jeton de thread et utiliser [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sur ce jeton.</span><span class="sxs-lookup"><span data-stu-id="b1e36-119">The following procedure describes how to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="b1e36-120">**Pour créer un jeton de thread et utiliser AdjustTokenPrivileges sur ce jeton**</span><span class="sxs-lookup"><span data-stu-id="b1e36-120">**To create a thread token and use AdjustTokenPrivileges on that token**</span></span>

1.  <span data-ttu-id="b1e36-121">Créez une copie du jeton de processus en appelant [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span><span class="sxs-lookup"><span data-stu-id="b1e36-121">Create a copy of the process token by calling [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span></span>
2.  <span data-ttu-id="b1e36-122">Récupérez le jeton de thread nouvellement créé en appelant [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span><span class="sxs-lookup"><span data-stu-id="b1e36-122">Retrieve the newly created thread token by calling [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span></span>
3.  <span data-ttu-id="b1e36-123">Activez l’opération privilégiée avec un appel à [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sur le nouveau jeton.</span><span class="sxs-lookup"><span data-stu-id="b1e36-123">Enable the privileged operation with a call to [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on the new token.</span></span>
4.  <span data-ttu-id="b1e36-124">Obtient un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="b1e36-124">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>
5.  <span data-ttu-id="b1e36-125">Voilez le pointeur sur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) avec un appel à [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="b1e36-125">Cloak the pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>
6.  <span data-ttu-id="b1e36-126">Répétez les étapes 1 à 5 lors de chaque appel à WMI.</span><span class="sxs-lookup"><span data-stu-id="b1e36-126">Repeat steps 1 through 5 on each call to WMI.</span></span>

    > [!Note]  
    > <span data-ttu-id="b1e36-127">Vous devez répéter les étapes, car COM met en cache les jetons de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="b1e36-127">You must repeat the steps because COM caches tokens incorrectly.</span></span>

     

<span data-ttu-id="b1e36-128">L’exemple de code de cette rubrique requiert l' \# instruction include suivante pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="b1e36-128">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="b1e36-129">L’exemple de code suivant montre comment activer des privilèges sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="b1e36-129">The following code example shows how to enable privileges on a local machine.</span></span>


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
