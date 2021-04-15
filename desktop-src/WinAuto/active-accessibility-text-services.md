---
title: Services de texte Active Accessibility
description: Cette section décrit les interfaces des services de texte Active Accessibility.
ms.assetid: 8bbc647f-1687-45b8-8b63-a6ea45a0a721
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9fdb4d9d9972f93db780d274b39e587e51c03b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463391"
---
# <a name="active-accessibility-text-services"></a><span data-ttu-id="c9048-103">Services de texte Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="c9048-103">Active Accessibility Text Services</span></span>

<span data-ttu-id="c9048-104">Cette section décrit les interfaces des services de texte Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="c9048-104">This section discusses the Active Accessibility Text Services interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="c9048-105">Active Accessibility Text services est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="c9048-105">Active Accessibility Text Services is deprecated.</span></span> <span data-ttu-id="c9048-106">Pour plus d’informations sur l’entrée de texte avancée et les technologies de langage naturel, consultez [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="c9048-106">Please see [Microsoft Windows Text Services Framework](../tsf/text-services-framework.md) for more information on advanced text input and natural language technologies.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c9048-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c9048-107">In this section</span></span>

| <span data-ttu-id="c9048-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c9048-108">Topic</span></span>                                                     | <span data-ttu-id="c9048-109">Description</span><span class="sxs-lookup"><span data-stu-id="c9048-109">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9048-110">**IAccServerDocMgr**</span><span class="sxs-lookup"><span data-stu-id="c9048-110">**IAccServerDocMgr**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccserverdocmgr)   | <span data-ttu-id="c9048-111">Expose des méthodes qui rendent des documents accessibles aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="c9048-111">Exposes methods that make documents accessible to client applications.</span></span>                              |
| [<span data-ttu-id="c9048-112">**IAccClientDocMgr**</span><span class="sxs-lookup"><span data-stu-id="c9048-112">**IAccClientDocMgr**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccclientdocmgr)   | <span data-ttu-id="c9048-113">Expose des méthodes pour que les applications clientes récupèrent des documents.</span><span class="sxs-lookup"><span data-stu-id="c9048-113">Exposes methods for client applications to retrieve documents.</span></span>                                      |
| [<span data-ttu-id="c9048-114">**IAccDictionary**</span><span class="sxs-lookup"><span data-stu-id="c9048-114">**IAccDictionary**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)       | <span data-ttu-id="c9048-115">Expose des méthodes pour la manipulation de chaînes.</span><span class="sxs-lookup"><span data-stu-id="c9048-115">Exposes methods for string manipulation.</span></span>                                                            |
| [<span data-ttu-id="c9048-116">**ICoCreateLocally**</span><span class="sxs-lookup"><span data-stu-id="c9048-116">**ICoCreateLocally**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-icocreatelocally)   | <span data-ttu-id="c9048-117">Expose une méthode qui permet à une application cliente de créer un objet d’assistance dans le contexte du serveur.</span><span class="sxs-lookup"><span data-stu-id="c9048-117">Exposes a method that enables a client application to create a helper object in the server context.</span></span> |
| [<span data-ttu-id="c9048-118">**ICoCreatedLocally**</span><span class="sxs-lookup"><span data-stu-id="c9048-118">**ICoCreatedLocally**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-icocreatedlocally) | <span data-ttu-id="c9048-119">Expose une méthode pour retourner des informations sur un objet local.</span><span class="sxs-lookup"><span data-stu-id="c9048-119">Exposes a method to return information about a local object.</span></span>                                        |
| [<span data-ttu-id="c9048-120">**IVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="c9048-120">**IVersionInfo**</span></span>](/windows/desktop/api/msaatext/nn-msaatext-iversioninfo)           | <span data-ttu-id="c9048-121">Expose des méthodes qui fournissent des informations de version pour les éléments accessibles.</span><span class="sxs-lookup"><span data-stu-id="c9048-121">Exposes methods that supply version information for accessible elements.</span></span>                            |

## <a name="related-topics"></a><span data-ttu-id="c9048-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9048-122">Related topics</span></span>

[<span data-ttu-id="c9048-123">Active Accessibility les services d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="c9048-123">Active Accessibility User Interface Services</span></span>](active-accessibility-user-interface-services-dev-guide.md)