---
title: Créer une table de montage séquentiel et ajouter des transitions
description: Pour créer une animation, une application doit construire une table de montage séquentiel.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- Animations de storyboards Windows, création
- Animations de storyboards Windows, ajout de transitions
- transitions Windows animation, création
- transitions Windows animation, ajouter à la table de montage séquentiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310865"
---
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="d6548-107">Créer une table de montage séquentiel et ajouter des transitions</span><span class="sxs-lookup"><span data-stu-id="d6548-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="d6548-108">Pour créer une animation, une application doit construire une table de montage séquentiel.</span><span class="sxs-lookup"><span data-stu-id="d6548-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="d6548-109">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="d6548-109">Overview</span></span>

<span data-ttu-id="d6548-110">Les étapes générales pour construire une table de montage séquentiel sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6548-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="d6548-111">Créer une table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="d6548-111">Create a storyboard</span></span>
2.  <span data-ttu-id="d6548-112">Créer une ou plusieurs transitions</span><span class="sxs-lookup"><span data-stu-id="d6548-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="d6548-113">Ajouter les transitions à la table de montage séquentiel, en spécifiant les variables qu’elles animent</span><span class="sxs-lookup"><span data-stu-id="d6548-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="d6548-114">Une table de montage séquentiel vide peut être créée à l’aide du gestionnaire d’animations.</span><span class="sxs-lookup"><span data-stu-id="d6548-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="d6548-115">L’application doit remplir chaque Storyboard avec des transitions.</span><span class="sxs-lookup"><span data-stu-id="d6548-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="d6548-116">Chaque transition spécifie la manière dont une variable d’animation unique change sur un intervalle de temps donné.</span><span class="sxs-lookup"><span data-stu-id="d6548-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="d6548-117">Les transitions peuvent être créées à l’aide du composant de bibliothèque de transition inclus dans l’animation Windows.</span><span class="sxs-lookup"><span data-stu-id="d6548-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="d6548-118">Une application peut également créer ses propres transitions personnalisées ou utiliser une bibliothèque de transition d’un tiers.</span><span class="sxs-lookup"><span data-stu-id="d6548-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="d6548-119">Lorsque l’application ajoute une transition à une table de montage séquentiel, elle spécifie la variable d’animation que la transition va animer.</span><span class="sxs-lookup"><span data-stu-id="d6548-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="d6548-120">Une table de montage séquentiel peut inclure des transitions sur une ou plusieurs variables d’animation.</span><span class="sxs-lookup"><span data-stu-id="d6548-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="d6548-121">Les storyboards plus complexes peuvent utiliser des images clés pour synchroniser les démarrages ou les terminaisons des transitions, ou pour spécifier des parties de la table de montage séquentiel qui doivent se répéter (un nombre fixe de fois ou indéfiniment).</span><span class="sxs-lookup"><span data-stu-id="d6548-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="d6548-122">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="d6548-122">Example Code</span></span>

<span data-ttu-id="d6548-123">L’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par une](timer-driven-animation-sample.md)Animation Windows. consultez la méthode CMainWindow :: ChangeColor.</span><span class="sxs-lookup"><span data-stu-id="d6548-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="d6548-124">Cet exemple crée la table de montage séquentiel (étape 1) à l’aide de la méthode [**IUIAnimationManager :: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , crée les transitions (étape 2) à l’aide de la méthode [**IUIAnimationTransitionLibrary :: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) et ajoute les transitions à la table de montage séquentiel (étape 3) à l’aide de la méthode [**IUIAnimationStoryboard :: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .</span><span class="sxs-lookup"><span data-stu-id="d6548-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a><span data-ttu-id="d6548-125">Étape précédente</span><span class="sxs-lookup"><span data-stu-id="d6548-125">Previous Step</span></span>

<span data-ttu-id="d6548-126">Avant de commencer cette étape, vous devez avoir terminé cette étape : [lire les valeurs de la variable d’animation](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="d6548-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="d6548-127">étape suivante</span><span class="sxs-lookup"><span data-stu-id="d6548-127">Next Step</span></span>

<span data-ttu-id="d6548-128">À l’issue de cette étape, l’étape suivante est : [planifier une table de montage séquentiel](scheduling-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="d6548-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6548-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6548-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6548-130">**IUIAnimationManager::CreateStoryboard**</span><span class="sxs-lookup"><span data-stu-id="d6548-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="d6548-131">**IUIAnimationStoryboard::AddTransition**</span><span class="sxs-lookup"><span data-stu-id="d6548-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="d6548-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span><span class="sxs-lookup"><span data-stu-id="d6548-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="d6548-133">Vue d’ensemble du storyboard</span><span class="sxs-lookup"><span data-stu-id="d6548-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




