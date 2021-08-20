---
title: Créer une table de montage séquentiel et ajouter des transitions
description: Pour créer une animation, une application doit construire une table de montage séquentiel.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- storyboards Windows Animation, création
- storyboards Windows Animation, ajout de transitions
- transitions Windows Animation, création
- transitions Windows Animation, ajouter à la table de montage séquentiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f992ae7720fea692d5e0b813e6cb9c35fab61d4bf2c781c928d9c8fcd08adb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999639"
---
# <a name="create-a-storyboard-and-add-transitions"></a>Créer une table de montage séquentiel et ajouter des transitions

Pour créer une animation, une application doit construire une table de montage séquentiel.

## <a name="overview"></a>Vue d’ensemble

Les étapes générales pour construire une table de montage séquentiel sont les suivantes :

1.  Créer une table de montage séquentiel
2.  Créer une ou plusieurs transitions
3.  Ajouter les transitions à la table de montage séquentiel, en spécifiant les variables qu’elles animent

Une table de montage séquentiel vide peut être créée à l’aide du gestionnaire d’animations. L’application doit remplir chaque Storyboard avec des transitions. Chaque transition spécifie la manière dont une variable d’animation unique change sur un intervalle de temps donné. les transitions peuvent être créées à l’aide du composant de bibliothèque de transition inclus dans Windows Animation. Une application peut également créer ses propres transitions personnalisées ou utiliser une bibliothèque de transition d’un tiers. Lorsque l’application ajoute une transition à une table de montage séquentiel, elle spécifie la variable d’animation que la transition va animer.

Une table de montage séquentiel peut inclure des transitions sur une ou plusieurs variables d’animation. Les storyboards plus complexes peuvent utiliser des images clés pour synchroniser les démarrages ou les terminaisons des transitions, ou pour spécifier des parties de la table de montage séquentiel qui doivent se répéter (un nombre fixe de fois ou indéfiniment).

## <a name="example-code"></a>Exemple de code

l’exemple de code suivant est extrait de MainWindow. cpp dans l’exemple d' [animation pilotée par un](timer-driven-animation-sample.md)exemple d’animation Windows. consultez la méthode CMainWindow :: ChangeColor. Cet exemple crée la table de montage séquentiel (étape 1) à l’aide de la méthode [**IUIAnimationManager :: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , crée les transitions (étape 2) à l’aide de la méthode [**IUIAnimationTransitionLibrary :: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) et ajoute les transitions à la table de montage séquentiel (étape 3) à l’aide de la méthode [**IUIAnimationStoryboard :: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .


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



## <a name="previous-step"></a>Étape précédente

Avant de commencer cette étape, vous devez avoir terminé cette étape : [lire les valeurs de la variable d’animation](updating---application-driven-animation.md).

## <a name="next-step"></a>étape suivante

À l’issue de cette étape, l’étape suivante est : [planifier une table de montage séquentiel](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Vue d’ensemble du storyboard](storyboard-construction.md)
</dt> </dl>

 

 




