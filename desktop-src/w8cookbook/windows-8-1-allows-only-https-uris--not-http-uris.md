---
title: URI dans Windows 8.1
description: Windows 8.1 autorise uniquement les URI https, pas les URI http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382544"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="7b234-103">Windows 8.1 autorise uniquement les URI https, pas les URI http</span><span class="sxs-lookup"><span data-stu-id="7b234-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="7b234-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="7b234-104">Platforms</span></span>

<dl> <span data-ttu-id="7b234-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7b234-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="7b234-106">Serveurs-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7b234-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="7b234-107">Description</span><span class="sxs-lookup"><span data-stu-id="7b234-107">Description</span></span>

<span data-ttu-id="7b234-108">Alors que les applications générées pour Windows 8 peuvent inclure des URI http et https dans leurs URI de contenu d’application, les applications générées pour Windows 8.1 peuvent inclure uniquement des URI HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7b234-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="7b234-109">La seule exception concerne les ContentUriRules dynamiques spécifiés dans le fichier AppxManifest.xml de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b234-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="7b234-110">Avec les ContentUriRules dynamiques, les applications peuvent accéder à des domaines supplémentaires ou à des ressources réseau fournies par l’administrateur, par exemple des URI stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="7b234-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="7b234-111">Toutefois, les ContentUriRules dynamiques sont uniquement disponibles pour les applications du Windows Store si elles remplissent les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b234-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="7b234-112">Le stratégie de groupe est activé</span><span class="sxs-lookup"><span data-stu-id="7b234-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="7b234-113">Le package a spécifié la fonctionnalité enterpriseAuthentication</span><span class="sxs-lookup"><span data-stu-id="7b234-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="7b234-114">Le OSMaxVersionTested du package est Windows 8.1 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="7b234-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="7b234-115">Les nouvelles restrictions dans Windows 8.1 font partie des restrictions de sécurité renforcée pour renforcer la protection de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="7b234-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="7b234-116">Manifestations</span><span class="sxs-lookup"><span data-stu-id="7b234-116">Manifestations</span></span>

<span data-ttu-id="7b234-117">Lors de l’exécution d’une application conçue pour Windows 8 sur Windows 8.1, l’utilisation d’URI http dans le [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="7b234-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="7b234-118">Corrections</span><span class="sxs-lookup"><span data-stu-id="7b234-118">Mitigations</span></span>

<span data-ttu-id="7b234-119">Nous recommandons que les développeurs WWA basculent de [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) vers le contrôle [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-WebView>).</span><span class="sxs-lookup"><span data-stu-id="7b234-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="7b234-120">Toutefois, si vous avez besoin d’une prise en charge pour AppCache), IndexedDB, la géolocalisation ou l’accès par programmation au Presse-papiers, vous devrez continuer à utiliser</span><span class="sxs-lookup"><span data-stu-id="7b234-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="7b234-121">pour Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7b234-121">for Windows 8.1.</span></span>

<span data-ttu-id="7b234-122">Utilisation continue de</span><span class="sxs-lookup"><span data-stu-id="7b234-122">Continued usage of</span></span> <iframe> <span data-ttu-id="7b234-123">pour le contenu distant, une nouvelle entrée est requise dans le ApplicationContentUriRules de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b234-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="7b234-124">Les applications avec WebView requièrent de nouvelles entrées dans le ApplicationContentUriRules si le contenu Web doit appeler Window. external. notifier pour générer un événement [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="7b234-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="7b234-125">Si vous n’avez pas Visual Studio, vous pouvez mettre à jour le manifeste de l’application en ajoutant le code XML suivant, y compris les caractères génériques pour les sous-domaines (par exemple, https:// \* . Microsoft.com) :</span><span class="sxs-lookup"><span data-stu-id="7b234-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a><span data-ttu-id="7b234-126">Ressources</span><span class="sxs-lookup"><span data-stu-id="7b234-126">Resources</span></span>

-   [<span data-ttu-id="7b234-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="7b234-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="7b234-128"><iframe>\| <iframe> objet élément</span><span class="sxs-lookup"><span data-stu-id="7b234-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="7b234-129">WebView (classe)</span><span class="sxs-lookup"><span data-stu-id="7b234-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="7b234-130">WebView. ScriptNotify, événement</span><span class="sxs-lookup"><span data-stu-id="7b234-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 