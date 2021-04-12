---
title: Comment ADSI intègre les extensions
description: Instructions qui décrivent comment ADSI interagit avec les extensions.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- ADSI des extensions
- ADSI et extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031853"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="29aa8-105">Comment ADSI intègre les extensions</span><span class="sxs-lookup"><span data-stu-id="29aa8-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="29aa8-106">Les instructions suivantes décrivent comment ADSI interagit avec les extensions :</span><span class="sxs-lookup"><span data-stu-id="29aa8-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="29aa8-107">Un objet est lié à un objet d’annuaire ADSI.</span><span class="sxs-lookup"><span data-stu-id="29aa8-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="29aa8-108">Par exemple, « LDAP : analyseur = JeffSmith, OU = Sales, DC = fabrikam, DC = COM ».</span><span class="sxs-lookup"><span data-stu-id="29aa8-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="29aa8-109">ADSI identifie que l’objet se trouve dans la classe **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="29aa8-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="29aa8-110">ADSI effectue une recherche dans le registre et identifie les CLSID d’extension pour l' **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="29aa8-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="29aa8-111">N’oubliez pas que l’interface ADSI met en cache ces données.</span><span class="sxs-lookup"><span data-stu-id="29aa8-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="29aa8-112">Un événement appelle la méthode **QueryInterface** pour IID \_ IMyExtension.</span><span class="sxs-lookup"><span data-stu-id="29aa8-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="29aa8-113">ADSI recherche les interfaces associées à l’objet **utilisateur** , en commençant par ses propres interfaces, puis en examinant les interfaces d’extension.</span><span class="sxs-lookup"><span data-stu-id="29aa8-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="29aa8-114">Si une correspondance est trouvée, ADSI crée une instance du composant qui prend en charge IID \_ IMyExtension et appelle **QueryInterface** pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="29aa8-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="29aa8-115">L’interface résultante est retournée.</span><span class="sxs-lookup"><span data-stu-id="29aa8-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="29aa8-116">L’utilisateur utilise cette interface pour appeler les méthodes d’interface.</span><span class="sxs-lookup"><span data-stu-id="29aa8-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="29aa8-117">Ensuite, le client appelle **QueryInterface** pour IID \_ IYourExtension, qui se trouve dans un autre composant.</span><span class="sxs-lookup"><span data-stu-id="29aa8-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="29aa8-118">Ce composant délègue cet appel **QueryInterface** à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’agrégateur, qui devient ADSI lui-même.</span><span class="sxs-lookup"><span data-stu-id="29aa8-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="29aa8-119">Là encore, ADSI recherche les interfaces et crée l’instance de composant.</span><span class="sxs-lookup"><span data-stu-id="29aa8-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 