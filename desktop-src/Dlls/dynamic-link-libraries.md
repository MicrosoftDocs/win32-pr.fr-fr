---
description: Une bibliothèque de liens dynamiques (DLL) est un module qui contient des fonctions et des données qui peuvent être utilisées par un autre module (application ou DLL).
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: Bibliothèques de Dynamic-Link (bibliothèques de liens dynamiques)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753781"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="cd2ea-103">Bibliothèques de Dynamic-Link (bibliothèques de liens dynamiques)</span><span class="sxs-lookup"><span data-stu-id="cd2ea-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="cd2ea-104">Une *bibliothèque de liens dynamiques* (dll) est un module qui contient des fonctions et des données qui peuvent être utilisées par un autre module (application ou dll).</span><span class="sxs-lookup"><span data-stu-id="cd2ea-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="cd2ea-105">Une DLL peut définir deux types de fonctions : exporté et interne.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="cd2ea-106">Les fonctions exportées sont destinées à être appelées par d’autres modules, ainsi qu’à partir de la DLL dans laquelle elles sont définies.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="cd2ea-107">Les fonctions internes sont généralement destinées à être appelées uniquement à partir de la DLL dans laquelle elles sont définies.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="cd2ea-108">Bien qu’une DLL puisse exporter des données, ses données sont généralement utilisées uniquement par ses fonctions.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="cd2ea-109">Toutefois, rien n’empêche un autre module de lire ou d’écrire cette adresse.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="cd2ea-110">Les dll offrent un moyen de modulariser les applications afin que leurs fonctionnalités puissent être mises à jour et réutilisées plus facilement.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="cd2ea-111">Les dll permettent également de réduire la surcharge de mémoire lorsque plusieurs applications utilisent la même fonctionnalité en même temps, car même si chaque application reçoit sa propre copie des données DLL, les applications partagent le code DLL.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="cd2ea-112">L’interface de programmation d’applications (API) Windows est implémentée sous la forme d’un ensemble de dll, de sorte que tout processus qui utilise l’API Windows utilise la liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="cd2ea-113">À propos des bibliothèques Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="cd2ea-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="cd2ea-114">Utilisation des bibliothèques de Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="cd2ea-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="cd2ea-115">Référence de bibliothèque de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="cd2ea-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="cd2ea-116">Si vous êtes un utilisateur rencontrant des difficultés avec une DLL sur votre ordinateur, vous devez contacter le support technique de l’éditeur du logiciel qui publie la DLL.</span><span class="sxs-lookup"><span data-stu-id="cd2ea-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="cd2ea-117">Si vous pensez que vous avez besoin de la prise en charge d’un produit Microsoft (y compris Windows), accédez à notre site de support technique à l’adresse [support.Microsoft.com](https://support.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="cd2ea-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cd2ea-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd2ea-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd2ea-119">Dll (Visual C++)</span><span class="sxs-lookup"><span data-stu-id="cd2ea-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
