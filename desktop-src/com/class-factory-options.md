---
title: Options de fabrique de classes
description: Options de fabrique de classes
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730429"
---
# <a name="class-factory-options"></a><span data-ttu-id="ce8be-103">Options de fabrique de classes</span><span class="sxs-lookup"><span data-stu-id="ce8be-103">Class Factory Options</span></span>

<span data-ttu-id="ce8be-104">Un contrôle ActiveX, en vertu d’un objet COM, doit avoir un code serveur associé qui prend en charge la création de contrôles via [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) au minimum.</span><span class="sxs-lookup"><span data-stu-id="ce8be-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="ce8be-105">Il est facultatif, pas obligatoire, que cet objet de classe prenne également en charge [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) pour la gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="ce8be-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="ce8be-106">Seuls les fournisseurs concernés par les licences doivent prendre en charge le mécanisme de licence de COM.</span><span class="sxs-lookup"><span data-stu-id="ce8be-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="ce8be-107">En d’autres termes, étant donné que **IClassFactory2** est le seul moyen d’obtenir une licence de niveau com, cette interface est requise sur l’objet de classe pour les contrôles qui souhaitent être sous licence.</span><span class="sxs-lookup"><span data-stu-id="ce8be-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce8be-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce8be-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce8be-109">Contrôles</span><span class="sxs-lookup"><span data-stu-id="ce8be-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 