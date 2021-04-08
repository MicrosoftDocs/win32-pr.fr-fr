---
description: Suivez ces instructions lors de la création d’un module de fusion 64 bits.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Utilisation des modules de fusion 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757804"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="ccf5a-103">Utilisation des modules de fusion 64 bits</span><span class="sxs-lookup"><span data-stu-id="ccf5a-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="ccf5a-104">Un module de fusion 64 bits présente l’une des caractéristiques identifiées dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="ccf5a-105">Le module de fusion contient au moins un composant qui a été compilé pour les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="ccf5a-106">Le module de fusion ne contient aucun composant 64 bits, mais il est destiné à être utilisé uniquement avec les packages de [Windows Installer 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf5a-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="ccf5a-107">Les modules de fusion peuvent être utilisés comme suit :</span><span class="sxs-lookup"><span data-stu-id="ccf5a-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="ccf5a-108">Un module de fusion 64 bits peut être fusionné dans un package [Windows Installer 64 bits](64-bit-windows-installer-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="ccf5a-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="ccf5a-109">Les propriétés [**Résumé du modèle**](template-summary.md) dans le module de fusion et dans le package Windows Installer doivent être définies sur le même type de processeur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="ccf5a-110">Un module de fusion x64 ne peut être fusionné que dans des packages x64 et un module de fusion Intel64 ne peut être fusionné que dans des packages Intel64.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="ccf5a-111">Un module de fusion 32 bits peut être fusionné dans des packages de Windows Installer 32 bits ou [64](64-bit-windows-installer-packages.md) bits.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="ccf5a-112">Un module de fusion 64 bits peut être fusionné dans un package 64 bits sur un système d’exploitation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="ccf5a-113">Respectez les points suivants lors de la création d’un module de fusion 64 bits :</span><span class="sxs-lookup"><span data-stu-id="ccf5a-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="ccf5a-114">Utilisez la même procédure générale que lors de la création de modules de fusion bits 32.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="ccf5a-115">Pour plus d’informations, consultez [à propos des modules de fusion](about-merge-modules.md) et [création de modules de fusion](authoring-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ccf5a-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="ccf5a-116">Si vous exécutez un système Intel64, vous devez définir la propriété [**Résumé du modèle**](template-summary.md) avec la valeur Intel64.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="ccf5a-117">Vous devez définir la propriété **Résumé du modèle** avec la valeur x64 si vous exécutez un système x64.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="ccf5a-118">Pour plus d’informations, consultez [Référence du flux des informations résumées du module de fusion](merge-module-summary-information-stream-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ccf5a-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="ccf5a-119">Lorsque les deux modules de fusion 32 bits et 64 bits existent pour le même composant, il est recommandé que les modules aient des signatures différentes.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="ccf5a-120">Cela permet à un package de contenir les deux versions du composant.</span><span class="sxs-lookup"><span data-stu-id="ccf5a-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="ccf5a-121">Pour plus d’informations, consultez [Windows Installer sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md).</span><span class="sxs-lookup"><span data-stu-id="ccf5a-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



