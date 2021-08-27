---
title: Vue d’ensemble de la couche de débogage Direct2D
description: Vue d’ensemble de la couche de débogage Direct2D
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad960c50cd125ec8c335d836949457bb05ef65aba4b2edaff1dfbbd3a9cf6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087769"
---
# <a name="direct2d-debug-layer-overview"></a>Vue d’ensemble de la couche de débogage Direct2D

La couche de débogage Direct2D fournit des messages de débogage au moment du design pour réduire l’échec de l’application Runtime. Cette vue d’ensemble décrit les principes fondamentaux de la couche de débogage Direct2D. Il part du principe que vous êtes familiarisé avec la création d’applications Direct2D de base.

Cette vue d’ensemble contient les sections suivantes.

-   [Qu’est-ce que la couche de débogage Direct2D ?](#what-is-the-direct2d-debug-layer)
-   [Installation de la couche de débogage Direct2D](#installing-the-direct2d-debug-layer)
-   [Activation de la couche de débogage](#enabling-the-debug-layer)
-   [Niveaux de débogage](#debug-levels)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>Qu’est-ce que la couche de débogage Direct2D ?

La couche de débogage Direct2D, implémentée séparément de Direct2D dans sa propre DLL nommée d2d1debug.dll, fournit des messages de débogage pour vous permettre d’utiliser avec précision les fonctions Direct2D. Les messages de débogage résultent souvent de violations de contrat d’API telles que les paramètres non valides (qui peuvent être liés à Direct3D), de ressources non valides, de violations de thread et de problèmes de performances, tels que l’utilisation d’une couche quand un clip suffit. Pour spécifier la quantité d’informations qui est tracée par la couche de débogage, vous pouvez spécifier l’un des trois niveaux de débogage : information, avertissement et erreur. et un message d’erreur de niveau déclenche le point d’arrêt pour vous aider à effectuer le débogage.

## <a name="installing-the-direct2d-debug-layer"></a>Installation de la couche de débogage Direct2D

Pour obtenir des instructions sur l’installation de la couche de débogage, consultez [installation de la couche de débogage Direct2D](installing-the-direct2d-debug-layer.md).

## <a name="enabling-the-debug-layer"></a>Activation de la couche de débogage

Pour activer la couche de débogage dans votre application, spécifiez une valeur de [**\_ \_ niveau de débogage d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) autre que le niveau de débogage **d2d1 \_ \_ \_ aucun** lorsque vous créez une fabrique avec la fonction [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .

> [!Note]  
> Si la couche de débogage Direct2D est activée, l’effet de gestion des couleurs Direct2D (CLSID \_ D2D1ColorManagement) peut entraîner une violation d’accès lors de la définition d’un contexte de couleur. La solution de contournement consiste à désactiver la couche de débogage lors de l’utilisation de l’effet de gestion des couleurs

 

L’activation de la couche de débogage pour une fabrique active également les informations de débogage pour tout objet créé par cette fabrique.

L’exemple suivant active la couche de débogage pour une fabrique lorsque l’application est compilée pour la configuration de build DEBUG.


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> Si aucune option de fabrique n’est spécifiée ou si un niveau de débogage de « None » est spécifié, la couche de débogage n’est pas appelée. La couche de débogage ne doit jamais être active dans la version Release d’une application.

 

La section suivante décrit les différents niveaux de débogage définis par l’énumération de [**\_ \_ niveau de débogage d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .

## <a name="debug-levels"></a>Niveaux de débogage

L’énumération de [**\_ \_ niveau de débogage d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) spécifie trois niveaux de débogage : erreur de niveau de débogage d2d1 \_ \_ \_ (erreur), d2d1 \_ avertissement de niveau de débogage \_ \_ (avertissement) et \_ informations de niveau de débogage d2d1 \_ \_ (informations). Ces niveaux sont interprétés comme suit :

-   **Erreur :** Direct2D envoie des messages d’erreur graves à la couche de débogage. Par exemple, l’interruption d’une contrainte de thread génère une erreur grave.

-   **Avertissement :** Direct2D envoie des messages d’erreur et des avertissements à la couche de débogage pour vous permettre de traiter l’un de ces messages.

-   **Informations :** Direct2D envoie des messages d’erreur, des avertissements et des informations de diagnostic supplémentaires à la couche de débogage. Par exemple, les messages d’amélioration des performances seront envoyés à ce niveau de débogage.

La valeur D2D1 \_ niveau de débogage \_ \_ aucun (aucune) indique que Direct2D ne fournit pas de sortie de débogage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Messages de débogage](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




