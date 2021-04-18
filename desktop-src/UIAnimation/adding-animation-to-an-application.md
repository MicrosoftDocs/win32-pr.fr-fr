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
# <a name="create-the-main-animation-objects"></a>Créer les objets d’animation principaux

Pour utiliser l’animation Windows dans votre application, la première étape consiste à créer un petit ensemble d’objets d’animation principaux.

## <a name="overview"></a>Vue d’ensemble

Utilisez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le gestionnaire d’animations, le minuteur d’animation et les objets de bibliothèque de transition.

Ces objets seront nécessaires pour créer et afficher les animations. ils ne doivent donc pas être libérés tant que l’application n’est pas arrêtée. S’il n’y a aucun risque que des rappels enregistrés aient créé un cycle de référence, la libération des objets suffit pour un nettoyage approprié. Dans le cas contraire, l’application peut se nettoyer en effaçant les rappels (en transmettant la **valeur null** à la place de chacune) ou en appelant la méthode [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) du gestionnaire d’animations.

## <a name="example-code"></a>Exemple de code

L’exemple de code suivant est extrait de MainWindow. cpp dans les exemples d’animation Windows. consultez la méthode CMainWindow :: InitializeAnimation.


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



Notez les définitions suivantes de MainWindow. h.


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



## <a name="next-step"></a>étape suivante

À l’issue de cette étape, l’étape suivante est : [créer des variables d’animation](create-animation-variables.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Vue d’ensemble des animations Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 