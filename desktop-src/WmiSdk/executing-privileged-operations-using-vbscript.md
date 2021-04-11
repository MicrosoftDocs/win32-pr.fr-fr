---
description: Si vous utilisez l’API de script pour WMI, vous pouvez définir des privilèges de sécurité spécifiques.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Exécution d’opérations privilégiées à l’aide de VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115859"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="de14d-103">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="de14d-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="de14d-104">Si vous utilisez l’API de script pour WMI, vous pouvez définir des privilèges de sécurité spécifiques.</span><span class="sxs-lookup"><span data-stu-id="de14d-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="de14d-105">Par exemple, vous pouvez définir les privilèges de sécurité pour demander un arrêt du système d’exploitation ou pour examiner le journal des événements de sécurité.</span><span class="sxs-lookup"><span data-stu-id="de14d-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="de14d-106">Pour plus d’informations, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="de14d-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="de14d-107">Vous devez uniquement définir des privilèges lorsque vous accédez à WMI sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="de14d-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="de14d-108">Lorsque vous accédez à un hôte distant, COM RPC définit automatiquement les privilèges.</span><span class="sxs-lookup"><span data-stu-id="de14d-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="de14d-109">Pour déterminer tous les privilèges requis, consultez la documentation relative aux classes WMI spécifiques auxquelles vous souhaitez accéder, telles que [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="de14d-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="de14d-110">Pour plus d’informations, consultez [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="de14d-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="de14d-111">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="de14d-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="de14d-112">Définition d’un privilège à partir de l’objet de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="de14d-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="de14d-113">Définition d’un privilège dans le cadre d’un moniker</span><span class="sxs-lookup"><span data-stu-id="de14d-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="de14d-114">Révocation et réinitialisation des privilèges</span><span class="sxs-lookup"><span data-stu-id="de14d-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="de14d-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de14d-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="de14d-116">Définition d’un privilège à partir de l’objet de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="de14d-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="de14d-117">Utilisez la procédure suivante pour définir des privilèges de sécurité dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="de14d-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="de14d-118">**Pour définir des privilèges dans Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="de14d-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="de14d-119">Créez un objet de type [**SWbemLocator**](swbemlocator.md).</span><span class="sxs-lookup"><span data-stu-id="de14d-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="de14d-120">Ajoutez le nouveau privilège à l’objet [**SWbemLocator. \_ Security**](swbemlocator-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="de14d-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="de14d-121">L’objet de [**sécurité \_**](swbemlocator-security-.md) contient une collection [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="de14d-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="de14d-122">Les objets du jeu sont des objets [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="de14d-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="de14d-123">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="de14d-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="de14d-124">Connectez-vous à WMI et récupérez un objet [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="de14d-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="de14d-125">L’objet [**SWbemServices**](swbemservices.md) hérite du privilège défini à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="de14d-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="de14d-126">Vous pouvez également définir un privilège à l’aide de la méthode [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="de14d-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="de14d-127">Définition d’un privilège dans le cadre d’un moniker</span><span class="sxs-lookup"><span data-stu-id="de14d-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="de14d-128">Vous pouvez définir un privilège dans le cadre d’un moniker.</span><span class="sxs-lookup"><span data-stu-id="de14d-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="de14d-129">L’exemple suivant montre comment ajouter un privilège de débogage à un moniker.</span><span class="sxs-lookup"><span data-stu-id="de14d-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="de14d-130">Révocation et réinitialisation des privilèges</span><span class="sxs-lookup"><span data-stu-id="de14d-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="de14d-131">L’exemple suivant montre comment définir le privilège **SeDebugPrivilege** et révoquer le privilège **SeRemoteShutdownPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="de14d-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="de14d-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de14d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de14d-133">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="de14d-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="de14d-134">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="de14d-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
