---
title: Appel de WDS à partir de pages Web
description: Vous pouvez appeler Microsoft Windows Desktop Search (WDS) à partir de n’importe quelle page Web que vous créez ou gérez à l’aide de l’objet d’assistance du navigateur (BHO) et de Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "104030912"
---
# <a name="calling-wds-from-web-pages"></a><span data-ttu-id="af366-103">Appel de WDS à partir de pages Web</span><span class="sxs-lookup"><span data-stu-id="af366-103">Calling WDS from Web Pages</span></span>

> [!NOTE]
> <span data-ttu-id="af366-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="af366-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="af366-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="af366-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="af366-106">Vous pouvez appeler Microsoft Windows Desktop Search (WDS) à partir de n’importe quelle page Web que vous créez ou gérez à l’aide de l’objet d’assistance du navigateur (BHO) et de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="af366-106">You can call Microsoft Windows Desktop Search (WDS) from any webpage you create or maintain using the Browser Helper Object (BHO) and Windows Internet Explorer.</span></span> <span data-ttu-id="af366-107">Vous pouvez voir comment cela fonctionne sur la page Web MSN.</span><span class="sxs-lookup"><span data-stu-id="af366-107">You can see how this works on the MSN webpage.</span></span> <span data-ttu-id="af366-108">Au-dessus de la zone de recherche de https://www.msn.com se trouvent plusieurs types de recherche : Web, Actualités, images, Desktop, Encarta et local.</span><span class="sxs-lookup"><span data-stu-id="af366-108">Above the search box on https://www.msn.com are several search types: Web, News, Images, Desktop, Encarta, and Local.</span></span> <span data-ttu-id="af366-109">Si vous cliquez sur bureau, les paramètres de recherche sont transmis à Windows Desktop Search, qui effectue une recherche dans le catalogue et affiche les résultats dans l’interface utilisateur WDS.</span><span class="sxs-lookup"><span data-stu-id="af366-109">If you click Desktop, the search parameters are passed to Windows Desktop Search, which searches the catalog and displays results in the WDS user interface.</span></span> <span data-ttu-id="af366-110">Pour que les utilisateurs puissent démarrer une recherche sur le Bureau à partir de vos pages Web, WDSBHO doit être installé et activé sur leurs systèmes, vos pages Web doivent être inscrites auprès de WDS en tant qu’URL autorisée, et vous devez créer un lien pour transmettre la requête enetered utilisateur à WDS.</span><span class="sxs-lookup"><span data-stu-id="af366-110">For users to start a desktop search from your webpage(s), the WDSBHO must be installed and enabled on their systems, your webpage(s) must be registered with WDS as an allowed URL, and you must create a link to pass the user-enetered query to WDS.</span></span>

## <a name="enabling-the-wds-browser-help-object"></a><span data-ttu-id="af366-111">Activation de l’objet d’aide du navigateur WDS</span><span class="sxs-lookup"><span data-stu-id="af366-111">Enabling the WDS Browser Help Object</span></span>

<span data-ttu-id="af366-112">L’BHO est installé et activé par défaut dans Internet Explorer lorsque vous installez WDS, mais vous pouvez facilement vérifier qu’il n’a pas été désactivé ou désinstallé.</span><span class="sxs-lookup"><span data-stu-id="af366-112">The BHO is installed and enabled within Internet Explorer by default when you install WDS, but you can easily verify that it hasn't been disabled or uninstalled.</span></span> <span data-ttu-id="af366-113">Sur le système d’un utilisateur, ouvrez Internet Explorer, sélectionnez **Options Internet** dans le menu **Outils** , cliquez sur l’onglet **programmes** , puis sur **gérer les modules complémentaires**.</span><span class="sxs-lookup"><span data-stu-id="af366-113">On a user's system, open Internet Explorer , select **Internet Options** from the **Tools** menu, click the **Programs** tab, and then click **Manage Add-Ons**.</span></span> <span data-ttu-id="af366-114">Dans la liste des modules complémentaires, recherchez la classe dsWebAllowBHO et assurez-vous qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="af366-114">In your list of add-ons, look for the dsWebAllowBHO Class and make sure it is enabled.</span></span> <span data-ttu-id="af366-115">Lorsque l’BHO est désactivé, WDS continue de fonctionner normalement. Toutefois, vous ne pourrez pas effectuer de recherches sur le Bureau à partir d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="af366-115">When the BHO is disabled, WDS will continue to work normally; however, you will not be able to search the desktop from a webpage.</span></span>

<span data-ttu-id="af366-116">Les deux options suivantes pour autoriser une recherche sur le bureau exécutent la recherche localement avec l’application de recherche inscrite.</span><span class="sxs-lookup"><span data-stu-id="af366-116">Both of the following options for allowing a desktop search will execute the search locally with the registered search application.</span></span>

## <a name="registering-web-page-urls"></a><span data-ttu-id="af366-117">Inscription des URL de page Web</span><span class="sxs-lookup"><span data-stu-id="af366-117">Registering Web Page URLs</span></span>

<span data-ttu-id="af366-118">Le registre contient une liste d’URL de domaine « autorisées » à partir desquelles WDS peut être appelé.</span><span class="sxs-lookup"><span data-stu-id="af366-118">The Registry includes a list of "allowed" domain URLs from which WDS can be called.</span></span> <span data-ttu-id="af366-119">Pour inclure vos pages Web, vous devez répertorier votre ou vos URL de domaine en tant que REG \_ SZ dans le registre comme suit :</span><span class="sxs-lookup"><span data-stu-id="af366-119">To include your webpage(s), you need to list your domain URL(s) as REG\_SZ in the Registry as follows:</span></span>

<span data-ttu-id="af366-120">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **autorisé**\\*<number>* = <domainURL></span><span class="sxs-lookup"><span data-stu-id="af366-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows Desktop Search**\\**DSW**\\**Allowed**\\*<number>* = <domainURL></span></span>

<span data-ttu-id="af366-121">Où **<number>** est numéroté de manière séquentielle et **<domainURL>** est l’URL de la page Web à partir de laquelle vous souhaitez autoriser les recherches WDS.</span><span class="sxs-lookup"><span data-stu-id="af366-121">Where **<number>** is sequentially numbered, and **<domainURL>** is the URL of the Web Page you want to allow WDS searches from.</span></span> <span data-ttu-id="af366-122">Cette chaîne d’URL peut inclure l’astérisque générique \* au début ou à la fin de l’URL.</span><span class="sxs-lookup"><span data-stu-id="af366-122">This URL string can include the wildcard asterisk \* at the beginning or end of the URL.</span></span> <span data-ttu-id="af366-123">Par exemple, si la chaîne est « \* . mydomain.com », vous pouvez démarrer une recherche WDS à partir de https://www.mydomain.com et de https://mydomain.com .</span><span class="sxs-lookup"><span data-stu-id="af366-123">For example, if the string is "\*.mydomain.com", then you can start a WDS search from both https://www.mydomain.com and https://mydomain.com.</span></span>

## <a name="enabling-desktop-search-by-url"></a><span data-ttu-id="af366-124">Activation de Desktop Search by URL</span><span class="sxs-lookup"><span data-stu-id="af366-124">Enabling Desktop Search by URL</span></span>

<span data-ttu-id="af366-125">Une autre option qui ne nécessite pas l’accès au registre consiste à utiliser l’URL suivante sur vos pages Web :</span><span class="sxs-lookup"><span data-stu-id="af366-125">Another option that does not require access to the Registry is to use the following URL on your webpage(s):</span></span>

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

<span data-ttu-id="af366-126">où **requête** est la chaîne encodée URL sur laquelle l’utilisateur recherche, y compris les termes de la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md) .</span><span class="sxs-lookup"><span data-stu-id="af366-126">where **QUERY** is the URL-encoded string the user is searching on, including any [Advanced Query Syntax](-search-2x-wds-aqsreference.md) terms.</span></span>

 

 




