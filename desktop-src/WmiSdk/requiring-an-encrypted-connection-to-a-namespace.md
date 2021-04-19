---
description: Vous pouvez exiger que les applications et les scripts clients établissent une connexion chiffrée pour l’authentification en ajoutant le qualificateur RequiresEncryption au fichier format MOF (MOF). MOF qui crée l’espace de noms.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Exiger une connexion chiffrée à un espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518919"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="b0e4c-103">Exiger une connexion chiffrée à un espace de noms</span><span class="sxs-lookup"><span data-stu-id="b0e4c-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="b0e4c-104">Vous pouvez exiger que les applications et les scripts clients établissent une connexion chiffrée pour l’authentification en ajoutant le qualificateur **RequiresEncryption** au fichier format MOF (MOF). MOF qui crée l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="b0e4c-105">Une connexion chiffrée à un espace de noms WMI spécifie la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C** (ou **PktPrivacy** dans un script) pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="b0e4c-106">Le qualificateur **RequiresEncryption** fait en sorte que WMI rejette toutes les demandes de données entrantes, sauf s’il utilise explicitement l’authentification chiffrée.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="b0e4c-107">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md) ou définition de l' [authentification à l’aide de C++](setting-authentication-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="b0e4c-108">Vous pouvez également modifier un espace de noms existant en ajoutant cet attribut, puis compiler à nouveau le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="b0e4c-109">**RequiresEncryption** est utilisé dans [*MOF*](gloss-m.md) avec l’instruction de préprocesseur d' [espace de noms pragma](pragma-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e4c-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="b0e4c-110">La procédure suivante définit l’espace de noms pour exiger une connexion chiffrée.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="b0e4c-111">**Pour définir le chiffrement requis**</span><span class="sxs-lookup"><span data-stu-id="b0e4c-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="b0e4c-112">Créez un fichier format MOF (MOF) ou modifiez votre fichier MOF existant qui définit l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="b0e4c-113">L’exemple de code suivant montre que l’espace de noms qui sera modifié est le *\\ MyNamespace racine* et le fichier est nommé *MyNamespace \_ Security. mof*.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="b0e4c-114">**RequiresEncryption** a un type de données booléen. il doit donc être défini sur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="b0e4c-115">Exécutez [**mofcomp.exe**](mofcomp.md) pour compiler le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="b0e4c-116">**c : \\ mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="b0e4c-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="b0e4c-117">En C++, utilisez les méthodes [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="b0e4c-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="b0e4c-118">WMI rejette un client qui utilise le niveau d’authentification par défaut, car DCOM négocie la sécurité au niveau requis par le processus SVCHOST dans lequel le service WMI est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="b0e4c-119">Pour plus d’informations sur les hôtes de service, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="b0e4c-120">Pour plus d’informations sur la définition des niveaux d’authentification lors de la connexion à des espaces de noms WMI, consultez [définition du niveau de sécurité de processus par défaut à l’aide de c++](setting-the-default-process-security-level-using-c-.md), définition de l' [authentification à l’aide de C++](setting-authentication-using-c-.md), ou [définition du niveau de sécurité de processus par défaut en VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="b0e4c-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="b0e4c-121">Lors du retour de données sur une connexion de rappel asynchrone, WMI retourne un message d’accès refusé à l’ordinateur demandeur.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="b0e4c-122">WMI crée également une entrée de journal dans le journal des événements NT de l’ordinateur avec l’espace de noms chiffré, indiquant qu’une connexion sécurisée ne peut pas être établie au client.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="b0e4c-123">À compter de Windows Vista, le fichier WbemCore. log n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="b0e4c-124">Vous pouvez consulter le journal des événements NT pour rechercher des entrées indiquant les demandes de données entrantes rejetées à des espaces de noms qui requièrent un chiffrement.</span><span class="sxs-lookup"><span data-stu-id="b0e4c-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0e4c-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0e4c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e4c-126">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="b0e4c-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="b0e4c-127">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="b0e4c-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="b0e4c-128">Sécurisation d’une connexion WMI à distance</span><span class="sxs-lookup"><span data-stu-id="b0e4c-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



