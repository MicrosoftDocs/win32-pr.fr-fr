---
title: Exemples de code Win32 pour ordinateur de bureau
description: À propos des exemples de pensions pour Win32 et comment y effectuer des recherches.
ms.topic: article
ms.date: 03/19/2021
ms.openlocfilehash: 5a4083697d444f36b31c553a2d6159d4370565d4
ms.sourcegitcommit: 46e75903326c49a6c5cc576ee2b4f67f64a6d5ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106539486"
---
# <a name="desktop-win32-code-samples"></a><span data-ttu-id="39a30-103">Exemples de code Win32 pour ordinateur de bureau</span><span class="sxs-lookup"><span data-stu-id="39a30-103">Desktop Win32 code samples</span></span>

<span data-ttu-id="39a30-104">Consultez également [exemples de code](https://developer.microsoft.com/windows/samples/).</span><span class="sxs-lookup"><span data-stu-id="39a30-104">Also see [Code samples](https://developer.microsoft.com/windows/samples/).</span></span>

## <a name="find-a-sample-for-the-api-youre-interested-in"></a><span data-ttu-id="39a30-105">Trouver un exemple pour l’API qui vous intéresse</span><span class="sxs-lookup"><span data-stu-id="39a30-105">Find a sample for the API you're interested in</span></span>

<span data-ttu-id="39a30-106">Vous pouvez utiliser Microsoft Visual Studio pour rechercher le code source d’un référentiel entier afin de déterminer si l’utilisation d’une API Windows particulière est démontrée.</span><span class="sxs-lookup"><span data-stu-id="39a30-106">You can use Microsoft Visual Studio to search an entire repo's source code to see whether the usage of a particular Windows API is being demonstrated.</span></span>

* <span data-ttu-id="39a30-107">Clonez les dépôts figurant dans les sections ci-dessous (ou téléchargez le fichier ZIP) dans votre système de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="39a30-107">Clone any of the repos listed in the sections below (or download the ZIP) to your local file system.</span></span>
* <span data-ttu-id="39a30-108">**Recherchez ensuite dans les fichiers** dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="39a30-108">Then **Find in Files** in Visual Studio.</span></span> <span data-ttu-id="39a30-109">Définissez **regarder dans** le dossier dans lequel vous avez cloné ou téléchargé, puis recherchez le nom de l’API qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="39a30-109">Set **Look in** to the folder you cloned or downloaded into, and search for the name of the API you're interested in.</span></span> <span data-ttu-id="39a30-110">La vérification de la correspondance de la **casse** donne de meilleurs résultats.</span><span class="sxs-lookup"><span data-stu-id="39a30-110">Checking **Match case** gives best results.</span></span>
* <span data-ttu-id="39a30-111">Veillez à vérifier le **mot entier** si l’API peut être appelée sous différentes formes &mdash; , par exemple **CreateMutex**, **CreateMutexA** et **CreateMutexW**.</span><span class="sxs-lookup"><span data-stu-id="39a30-111">Be careful of checking **Match whole word** if the API can be called in various forms&mdash;for example, **CreateMutex**, **CreateMutexA**, and **CreateMutexW**.</span></span> <span data-ttu-id="39a30-112">Dans ce cas, recherchez **CreateMutex** avec l’option **mot entier** désactivé.</span><span class="sxs-lookup"><span data-stu-id="39a30-112">In that case, search for **CreateMutex** with **Match whole word** unchecked.</span></span>

> [!NOTE]
> <span data-ttu-id="39a30-113">Vous pouvez installer [Visual Studio](https://visualstudio.microsoft.com/downloads/) sans dépense.</span><span class="sxs-lookup"><span data-stu-id="39a30-113">You can install [Visual Studio](https://visualstudio.microsoft.com/downloads/) without expense.</span></span> <span data-ttu-id="39a30-114">Une édition Community est disponible et gratuite pour les étudiants, les contributeurs open source et les particuliers.</span><span class="sxs-lookup"><span data-stu-id="39a30-114">A Community edition is available&mdash;it's free for students, open-source contributors, and individuals.</span></span> <span data-ttu-id="39a30-115">Bien sûr, vous pouvez faire la même chose avec n’importe quel exemple de référentiel.</span><span class="sxs-lookup"><span data-stu-id="39a30-115">Of course you can do the same thing with any samples repo.</span></span>

## <a name="the-windows-classic-samples-repo"></a><span data-ttu-id="39a30-116">Exemples Windows classiques référentiel</span><span class="sxs-lookup"><span data-stu-id="39a30-116">The Windows classic samples repo</span></span>

<span data-ttu-id="39a30-117">Le référentiel principal qui contient des exemples d’applications Windows à l’aide de l’API Win32 est le référentiel d' [exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples) .</span><span class="sxs-lookup"><span data-stu-id="39a30-117">The main repo containing sample Windows apps using the Win32 API is the [Windows classic samples](https://github.com/Microsoft/Windows-classic-samples) repo.</span></span>

## <a name="directx-samples"></a><span data-ttu-id="39a30-118">Exemples DirectX</span><span class="sxs-lookup"><span data-stu-id="39a30-118">DirectX samples</span></span>

<span data-ttu-id="39a30-119">Consultez les exemples de graphiques [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) référentiel pour DirectX 12 qui illustrent comment créer des applications nécessitant beaucoup de ressources graphiques pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="39a30-119">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="39a30-120">Consultez également [exemples DirectX](/windows/uwp/gaming/directx-samples).</span><span class="sxs-lookup"><span data-stu-id="39a30-120">Also see [DirectX samples](/windows/uwp/gaming/directx-samples).</span></span>

## <a name="older-samples"></a><span data-ttu-id="39a30-121">Exemples plus anciens</span><span class="sxs-lookup"><span data-stu-id="39a30-121">Older samples</span></span>

<span data-ttu-id="39a30-122">Des exemples d’applications Win32 plus anciens sont disponibles dans [MSDN Code Gallery Microsoft Samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) référentiel.</span><span class="sxs-lookup"><span data-stu-id="39a30-122">You can find some older Win32 sample apps in the [MSDN Code Gallery Microsoft samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) repo.</span></span>

## <a name="see-also"></a><span data-ttu-id="39a30-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39a30-123">See also</span></span>

* [<span data-ttu-id="39a30-124">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="39a30-124">Code samples</span></span>](https://developer.microsoft.com/windows/samples/)
* [<span data-ttu-id="39a30-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="39a30-125">Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="39a30-126">Exemples classiques Windows</span><span class="sxs-lookup"><span data-stu-id="39a30-126">Windows classic samples</span></span>](https://github.com/Microsoft/Windows-classic-samples)
* [<span data-ttu-id="39a30-127">DirectX-Graphics-Samples</span><span class="sxs-lookup"><span data-stu-id="39a30-127">DirectX-Graphics-Samples</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples)
* [<span data-ttu-id="39a30-128">Exemples DirectX</span><span class="sxs-lookup"><span data-stu-id="39a30-128">DirectX samples</span></span>](/windows/uwp/gaming/directx-samples)
* [<span data-ttu-id="39a30-129">Exemples Microsoft de la Galerie de code MSDN</span><span class="sxs-lookup"><span data-stu-id="39a30-129">MSDN Code Gallery Microsoft samples</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft)
