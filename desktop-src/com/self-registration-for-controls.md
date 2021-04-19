---
title: Inscription automatique pour les contrôles
description: Inscription automatique pour les contrôles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511715"
---
# <a name="self-registration-for-controls"></a><span data-ttu-id="427e8-103">Inscription automatique pour les contrôles</span><span class="sxs-lookup"><span data-stu-id="427e8-103">Self Registration for Controls</span></span>

<span data-ttu-id="427e8-104">Les contrôles ActiveX doivent prendre en charge l’inscription automatique en implémentant les fonctions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) .</span><span class="sxs-lookup"><span data-stu-id="427e8-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="427e8-105">Les contrôles ActiveX doivent inscrire toutes les entrées de Registre standard pour les objets et les serveurs Automation incorporables.</span><span class="sxs-lookup"><span data-stu-id="427e8-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="427e8-106">Les contrôles ActiveX doivent utiliser l’API des catégories de composants pour s’inscrire en tant que contrôle et enregistrer les catégories de composants qu’un hôte doit prendre en charge et toutes les catégories implémentées par le contrôle, consultez [catégories de composants](component-categories.md).</span><span class="sxs-lookup"><span data-stu-id="427e8-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="427e8-107">Les contrôles ActiveX doivent également inscrire la clé de Registre [ToolboxBitmap32](toolboxbitmap32.md) , bien que cela ne soit pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="427e8-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="427e8-108">La catégorie de composant pouvant être insérée doit être inscrite uniquement si le contrôle peut être utilisé en tant qu’objet de document composé.</span><span class="sxs-lookup"><span data-stu-id="427e8-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="427e8-109">Il est important de noter qu’un objet de document composé doit prendre en charge certaines interfaces au-delà de la valeur de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) minimale requise pour un contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="427e8-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="427e8-110">Bien qu’un contrôle ActiveX puisse être qualifié d’objet de document composé, la documentation du contrôle doit indiquer clairement le comportement à attendre dans ces circonstances.</span><span class="sxs-lookup"><span data-stu-id="427e8-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="427e8-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="427e8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427e8-112">Contrôles</span><span class="sxs-lookup"><span data-stu-id="427e8-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 