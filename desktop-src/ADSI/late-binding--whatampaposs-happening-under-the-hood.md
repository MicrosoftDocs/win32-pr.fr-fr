---
title: Liaison tardive ce qui se passe en coulisses
description: Cette rubrique décrit le fonctionnement de la liaison tardive dans ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- extensions ADSI, liaison tardive, ce qui se passe en coulisses
- liaison Active Directory, liaison tardive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463699"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="ae208-105">Liaison tardive : que se passe-t-il en coulisse ?</span><span class="sxs-lookup"><span data-stu-id="ae208-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="ae208-106">La liste suivante décrit le processus général pour effectuer une liaison tardive :</span><span class="sxs-lookup"><span data-stu-id="ae208-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="ae208-107">Un objet est lié à un objet d’annuaire ADSI.</span><span class="sxs-lookup"><span data-stu-id="ae208-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="ae208-108">Par exemple, « LDAP : converti = JeffSmith, OU = Sales, DC = fabrikam, DC = COM » est lié à l’aide de la liaison tardive COM.</span><span class="sxs-lookup"><span data-stu-id="ae208-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="ae208-109">ADSI appelle alors la méthode [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur l’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="ae208-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="ae208-110">ADSI recherche un objet dans la classe utilisateur et crée un objet qui prend en charge les interfaces appropriées, telles que [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span><span class="sxs-lookup"><span data-stu-id="ae208-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="ae208-111">ADSI effectue une recherche dans le registre et trouve des CLSID d’extension pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae208-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="ae208-112">N’oubliez pas que l’interface ADSI met en cache ces données.</span><span class="sxs-lookup"><span data-stu-id="ae208-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="ae208-113">Un événement effectue un appel à la méthode **MyNewMethod** .</span><span class="sxs-lookup"><span data-stu-id="ae208-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="ae208-114">ADSI recherche son ID de dispatch et les ID de dispatch pour d’autres extensions ADSI.</span><span class="sxs-lookup"><span data-stu-id="ae208-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="ae208-115">ADSI recherche ensuite l’extension qui sert cet appel et appelle l’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour cette extension.</span><span class="sxs-lookup"><span data-stu-id="ae208-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="ae208-116">L’extension exécute la fonction.</span><span class="sxs-lookup"><span data-stu-id="ae208-116">The extension executes the function.</span></span>
-   <span data-ttu-id="ae208-117">À présent, le writer client appelle la méthode **YourNewMethod** à l’aide de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pour l’extension actuelle.</span><span class="sxs-lookup"><span data-stu-id="ae208-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="ae208-118">L’implémentation **IDispatch** de l’extension délègue à **IDispatch** pour ADSI.</span><span class="sxs-lookup"><span data-stu-id="ae208-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="ae208-119">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pour ADSI recherche à nouveau l’extension appropriée, ou elle-même, puis appelle l’extension appropriée à l’aide de l’interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) pour cette extension.</span><span class="sxs-lookup"><span data-stu-id="ae208-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 