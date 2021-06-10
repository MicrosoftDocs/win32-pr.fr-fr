---
description: D3DX est une bibliothèque d’outils conçue pour fournir des fonctionnalités graphiques supplémentaires par-dessus Direct3D. D3DX est fourni sous la forme d’une bibliothèque de liens dynamiques (DLL).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a2164349b761cd7ff2ccca5e2158abc22bd64
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910248"
---
# <a name="d3dx-direct3d-9"></a><span data-ttu-id="504f3-104">D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="504f3-104">D3DX (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="504f3-105">La bibliothèque D3DX est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="504f3-105">The D3DX library is deprecated.</span></span> <span data-ttu-id="504f3-106">Si vous n’avez pas la possibilité de procéder à une mise à niveau vers une version plus récente de Direct3D et du code de l’utilitaire associé, vous pouvez utiliser le package NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) au lieu de vous appuyer sur le SDK DirectX hérité ou DirectSetup.</span><span class="sxs-lookup"><span data-stu-id="504f3-106">If upgrading to a newer version of Direct3D and associated utility code is not an option, you can make use of the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package rather than relying on the legacy DirectX SDK or DirectSetup.</span></span>

<span data-ttu-id="504f3-107">D3DX est une bibliothèque d’outils conçue pour fournir des fonctionnalités graphiques supplémentaires par-dessus Direct3D.</span><span class="sxs-lookup"><span data-stu-id="504f3-107">D3DX is a library of tools designed to provide additional graphics functionality on top of Direct3D.</span></span> <span data-ttu-id="504f3-108">D3DX est fourni sous la forme d’une bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="504f3-108">D3DX is provided as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="504f3-109">Une seule version de D3DX est fournie dans cette version du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="504f3-109">Only one version of D3DX is provided in this release of the DirectX SDK.</span></span> <span data-ttu-id="504f3-110">La DLL de la version commerciale D3DX est incluse dans le redistribuable fourni dans le kit de développement logiciel (SDK) et est automatiquement installée dans le cadre de l' **installation de DirectX avec DirectSetup**.</span><span class="sxs-lookup"><span data-stu-id="504f3-110">The retail D3DX DLL is included in the redistributable provided in the SDK, and is automatically installed as part of **Installing DirectX with DirectSetup**.</span></span> <span data-ttu-id="504f3-111">La bibliothèque D3DX incluse dans cette version dépend des runtimes Direct3D fournis avec ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="504f3-111">The D3DX library included in this release is dependent on the Direct3D runtimes that shipped with this SDK.</span></span> <span data-ttu-id="504f3-112">Les applications qui sont liées à la version de D3DX dans cette version doivent également redistribuer le runtime à partir de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="504f3-112">Applications linking against the version of D3DX in this release must also redistribute the runtime from this SDK.</span></span>

<span data-ttu-id="504f3-113">Plusieurs versions de D3DX peuvent résider indépendamment sur un même système simultanément.</span><span class="sxs-lookup"><span data-stu-id="504f3-113">Multiple releases of D3DX can reside independently on a single system simultaneously.</span></span> <span data-ttu-id="504f3-114">En liant de manière statique une application à D3dx9. lib, l’application est liée de manière dynamique à la DLL de la version commerciale D3DX correspondante au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="504f3-114">By statically linking an application to D3dx9.lib, the application dynamically links to the corresponding retail D3DX DLL at run-time.</span></span> <span data-ttu-id="504f3-115">Cette DLL correspond aux en-têtes D3DX avec lesquels l’application est compilée (nommée avec la \_ constante de version du kit de développement logiciel D3DX \_ dans D3dx9core. h).</span><span class="sxs-lookup"><span data-stu-id="504f3-115">This DLL corresponds to the D3DX headers the application is compiled against (named with the D3DX\_SDK\_VERSION constant in D3dx9core.h).</span></span> <span data-ttu-id="504f3-116">À mesure que de nouvelles versions de D3DX sont fournies dans les futures versions du SDK DirectX, les applications qui sont liées à des bibliothèques D3DX antérieures ne seront pas affectées.</span><span class="sxs-lookup"><span data-stu-id="504f3-116">As new versions of D3DX are shipped in future releases of the DirectX SDK, applications linking to earlier D3DX libraries will remain unaffected.</span></span>

<span data-ttu-id="504f3-117">La bibliothèque D3DX résout ces problèmes généraux de fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="504f3-117">The D3DX library addresses these general areas of functionality:</span></span>

-   [<span data-ttu-id="504f3-118">Prise en charge des dessins en ligne dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="504f3-118">Line Drawing Support in D3DX (Direct3D 9)</span></span>](line-drawing-support-in-d3dx.md)
-   [<span data-ttu-id="504f3-119">Prise en charge des maillages dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="504f3-119">Mesh Support in D3DX (Direct3D 9)</span></span>](mesh-support-in-d3dx.md)
-   [<span data-ttu-id="504f3-120">Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="504f3-120">Math Function Support in D3DX (Direct3D 9)</span></span>](math-function-support-in-d3dx.md)
-   [<span data-ttu-id="504f3-121">Prise en charge de la texture dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="504f3-121">Texture Support in D3DX (Direct3D 9)</span></span>](texture-support-in-d3dx.md)

## <a name="related-topics"></a><span data-ttu-id="504f3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="504f3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="504f3-123">Prise en main</span><span class="sxs-lookup"><span data-stu-id="504f3-123">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



