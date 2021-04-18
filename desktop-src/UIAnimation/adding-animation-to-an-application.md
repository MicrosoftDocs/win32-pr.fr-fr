---
title: Créer les objets d’animation principaux
description: Pour utiliser l’animation Windows dans votre application, la première étape consiste à créer un petit ensemble d’objets d’animation principaux.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- objets du gestionnaire d’animations Windows animation, création
- objets de minuteur d’animation Windows animation, création
- objets de bibliothèque de transition Windows animation, création
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382426"
---
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="b3e0d-106">Créer les objets d’animation principaux</span><span class="sxs-lookup"><span data-stu-id="b3e0d-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="b3e0d-107">Pour utiliser l’animation Windows dans votre application, la première étape consiste à créer un petit ensemble d’objets d’animation principaux.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="b3e0d-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b3e0d-108">Overview</span></span>

<span data-ttu-id="b3e0d-109">Utilisez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le gestionnaire d’animations, le minuteur d’animation et les objets de bibliothèque de transition.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="b3e0d-110">Ces objets seront nécessaires pour créer et afficher les animations. ils ne doivent donc pas être libérés tant que l’application n’est pas arrêtée.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="b3e0d-111">S’il n’y a aucun risque que des rappels enregistrés aient créé un cycle de référence, la libération des objets suffit pour un nettoyage approprié.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="b3e0d-112">Dans le cas contraire, l’application peut se nettoyer en effaçant les rappels (en transmettant la **valeur null** à la place de chacune) ou en appelant la méthode [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) du gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="b3e0d-113">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b3e0d-113">Example Code</span></span>

<span data-ttu-id="b3e0d-114">L’exemple de code suivant est extrait de MainWindow. cpp dans les exemples d’animation Windows. consultez la méthode CMainWindow :: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



<span data-ttu-id="b3e0d-115">Notez les définitions suivantes de MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="b3e0d-115">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a><span data-ttu-id="b3e0d-116">étape suivante</span><span class="sxs-lookup"><span data-stu-id="b3e0d-116">Next Step</span></span>

<span data-ttu-id="b3e0d-117">À l’issue de cette étape, l’étape suivante est : [créer des variables d’animation](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="b3e0d-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3e0d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3e0d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3e0d-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b3e0d-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="b3e0d-120">**IUIAnimationManager**</span><span class="sxs-lookup"><span data-stu-id="b3e0d-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="b3e0d-121">**IUIAnimationTimer**</span><span class="sxs-lookup"><span data-stu-id="b3e0d-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="b3e0d-122">**IUIAnimationTransitionLibrary**</span><span class="sxs-lookup"><span data-stu-id="b3e0d-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="b3e0d-123">Vue d’ensemble des animations Windows</span><span class="sxs-lookup"><span data-stu-id="b3e0d-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 