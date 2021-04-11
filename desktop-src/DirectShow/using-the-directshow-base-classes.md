---
description: Utilisation des classes de base DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Utilisation des classes de base DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203621"
---
# <a name="using-the-directshow-base-classes"></a><span data-ttu-id="ab3ce-103">Utilisation des classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab3ce-103">Using the DirectShow Base Classes</span></span>

<span data-ttu-id="ab3ce-104">Pour utiliser les classes de base dans DirectShow, vous devez générer et lier la bibliothèque de classes de base.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-104">To use the base classes in DirectShow, you must build and link the base class library.</span></span>

<span data-ttu-id="ab3ce-105">La bibliothèque de classes de base est fournie en tant qu’exemple SDK dans le kit de développement logiciel (SDK) Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="ab3ce-105">The base class library is provided as a SDK sample in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span> <span data-ttu-id="ab3ce-106">L’emplacement exact dépend de la version du kit de développement logiciel (SDK) que vous avez installée, mais le chemin d’accès relatif est le suivant :</span><span class="sxs-lookup"><span data-stu-id="ab3ce-106">The exact location depends on the version of the SDK that you have installed, but the relative path is:</span></span>

<span data-ttu-id="ab3ce-107">*(Racine des exemples du kit de développement logiciel)* \\ \\BaseClasses DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab3ce-107">*(SDK samples root)*\\DirectShow\\BaseClasses</span></span>

<span data-ttu-id="ab3ce-108">En-tête : streams. h</span><span class="sxs-lookup"><span data-stu-id="ab3ce-108">Header: Streams.h</span></span>

<span data-ttu-id="ab3ce-109">Bibliothèque : l’exemple génère des versions commerciales et de débogage de la bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="ab3ce-109">Library: The sample builds retail and debug versions of the library:</span></span>

-   <span data-ttu-id="ab3ce-110">Version commerciale : Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="ab3ce-110">Retail version: Strmbase.lib</span></span>
-   <span data-ttu-id="ab3ce-111">Version de débogage : Strmbasd. lib.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-111">Debug version: Strmbasd.lib.</span></span>

<span data-ttu-id="ab3ce-112">Pour plus d’informations sur la configuration de votre environnement de génération, consultez [configuration de l’environnement de génération](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ce-112">For more information on setting up your build environment, see [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

## <a name="preprocessor-symbols"></a><span data-ttu-id="ab3ce-113">Symboles du préprocesseur</span><span class="sxs-lookup"><span data-stu-id="ab3ce-113">Preprocessor Symbols</span></span>

<span data-ttu-id="ab3ce-114">Lorsque vous incluez le fichier d’en-tête streams. h, les symboles de préprocesseur suivants ont une signification particulière :</span><span class="sxs-lookup"><span data-stu-id="ab3ce-114">When you include the header file Streams.h, the following preprocessor symbols have special meaning:</span></span>

-   <span data-ttu-id="ab3ce-115">PERF : réservé.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-115">PERF: Reserved.</span></span> <span data-ttu-id="ab3ce-116">N’utilisez pas ce symbole de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-116">Do not use this preprocessor symbol.</span></span>
-   <span data-ttu-id="ab3ce-117">VFWROBUST : active la validation de pointeur dans Retail.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-117">VFWROBUST: Enables pointer validation in retail.</span></span> <span data-ttu-id="ab3ce-118">Pour plus d’informations, consultez [macros de validation de pointeurs](pointer-validation-macros.md).</span><span class="sxs-lookup"><span data-stu-id="ab3ce-118">For more information, see [Pointer Validation Macros](pointer-validation-macros.md).</span></span> <span data-ttu-id="ab3ce-119">Dans les versions Debug, il n’est pas nécessaire de définir VFWROBUST.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-119">In debug builds, it is not necessary to define VFWROBUST.</span></span>

> [!Note]  
> <span data-ttu-id="ab3ce-120">Dans Windows Vista et versions ultérieures, les macros de validation du pointeur sont vides.</span><span class="sxs-lookup"><span data-stu-id="ab3ce-120">In Windows Vista and later, the pointer validation macros are empty.</span></span>

 

 

 



