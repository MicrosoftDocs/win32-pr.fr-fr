---
description: Lorsque vous accédez à un serveur Windows Management Instrumentation (WMI) à l’aide d’un script, vous pouvez choisir entre les protocoles d’authentification NTLM (NT LAN Manager) ou Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Définition du service d’authentification à l’aide de VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545119"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="214d7-103">Définition du service d’authentification à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="214d7-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="214d7-104">Lorsque vous accédez à un serveur Windows Management Instrumentation (WMI) à l’aide d’un script, vous pouvez choisir entre les protocoles d’authentification NTLM (NT LAN Manager) ou Kerberos.</span><span class="sxs-lookup"><span data-stu-id="214d7-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="214d7-105">La spécification de Kerberos n’est pas requise, sauf lors de l’utilisation de la délégation.</span><span class="sxs-lookup"><span data-stu-id="214d7-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="214d7-106">Pour plus d’informations, consultez [connexion à un troisième ordinateur-délégation](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="214d7-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="214d7-107">Étant donné que les versions de système d’exploitation diffèrent dans le service d’authentification qu’elles utilisent, il est recommandé de ne pas spécifier de valeur pour le champ autorité lors de la connexion à un système distant.</span><span class="sxs-lookup"><span data-stu-id="214d7-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="214d7-108">Au lieu de cela, autorisez le système d’exploitation et la version distribuée du modèle COM (Component Object Model) à sélectionner NTLM ou Kerberos.</span><span class="sxs-lookup"><span data-stu-id="214d7-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="214d7-109">Si un service d’authentification est spécifié, la syntaxe requiert le nom principal du serveur, qui est le nom de l’ordinateur cible plutôt que le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="214d7-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="214d7-110">Vous pouvez utiliser le paramètre Authority uniquement avec les connexions aux serveurs WMI distants.</span><span class="sxs-lookup"><span data-stu-id="214d7-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="214d7-111">La tentative de connexion échoue si vous tentez de définir des niveaux d’autorisation dans le cadre d’un moniker ou d’un appel à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) pour une connexion locale.</span><span class="sxs-lookup"><span data-stu-id="214d7-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="214d7-112">Procédez comme suit pour spécifier le service d’authentification que vous souhaitez utiliser dans le paramètre *strAuthority* de la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou de la connexion de chaîne [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="214d7-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="214d7-113">**Pour spécifier l’authentification NTLM ou Kerberos avec l’API de script pour WMI**</span><span class="sxs-lookup"><span data-stu-id="214d7-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="214d7-114">Si le paramètre *strAuthority* commence par la chaîne « Kerberos : », WMI suppose que la chaîne fait référence à un nom de principal Kerberos et que l’authentification Kerberos est utilisée.</span><span class="sxs-lookup"><span data-stu-id="214d7-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="214d7-115">Si le paramètre *strAuthority* commence par la chaîne « ntlmdomain : », WMI utilise l’authentification NTLM à la place.</span><span class="sxs-lookup"><span data-stu-id="214d7-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="214d7-116">Vous pouvez également utiliser la partie autorité d’un moniker pour spécifier le type d’authentification utilisé pour la connexion à WMI.</span><span class="sxs-lookup"><span data-stu-id="214d7-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="214d7-117">Pour utiliser l’authentification Kerberos lors de l’utilisation d’un moniker, incluez la chaîne « Authority = Kerberos : » suivie du nom principal.</span><span class="sxs-lookup"><span data-stu-id="214d7-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="214d7-118">Pour utiliser l’authentification NTLM, incluez la chaîne « Authority = ntlmdomain : » suivie du nom de domaine NTLM.</span><span class="sxs-lookup"><span data-stu-id="214d7-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="214d7-119">L’exemple suivant montre un moniker qui demande l’authentification Kerberos à l’aide de l’entité « MyDomain \\ Server ».</span><span class="sxs-lookup"><span data-stu-id="214d7-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="214d7-120">En revanche, l’exemple suivant montre un moniker qui demande l’authentification NTLM à l’aide du domaine « mydomain ».</span><span class="sxs-lookup"><span data-stu-id="214d7-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



