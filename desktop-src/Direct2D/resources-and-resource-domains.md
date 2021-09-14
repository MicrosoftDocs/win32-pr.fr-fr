---
title: Vue d’ensemble des ressources
description: Décrit les ressources Direct2D et comment elles peuvent être partagées.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, ressources
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bf4eb807a25b592e32a2d83436532af17462d70c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112558"
---
# <a name="resources-overview"></a>Vue d’ensemble des ressources

Une ressource Direct2D est un objet utilisé pour le dessin et est représenté par une interface Direct2D, telle que [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) ou [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Cette rubrique décrit les types de ressources Direct2D et comment elles peuvent être partagées.

Cette rubrique contient les sections suivantes :

-   [À propos des ressources Direct2D](#about-direct2d-resources)
-   [Ressources indépendantes du périphérique](#device-independent-resources)
-   [Ressources dépendantes de l’appareil](#device-dependent-resources)
-   [Partage des ressources de la fabrique](#sharing-factory-resources)
-   [Partage des ressources de la cible de rendu](#sharing-render-target-resources)
    -   [Cibles de rendu matériel](#hardware-render-targets)
    -   [Cibles de rendu de surface DXGI](#dxgi-surface-render-targets)
    -   [Cibles de rendu compatibles et bitmaps partagées](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>À propos des ressources Direct2D

De nombreuses API 2D à accélération matérielle sont conçues autour d’un modèle de ressource centré sur l’UC et d’un ensemble d’opérations de rendu qui fonctionnent bien sur les processeurs. ensuite, une partie de l’API est accélérée par le matériel. L’implémentation de ces API requiert un gestionnaire de ressources pour le mappage des ressources de processeur aux ressources sur le GPU. En raison des limitations du GPU, certaines opérations peuvent ne pas être accélérées dans toutes les circonstances. Dans ce cas, le gestionnaire des ressources doit communiquer entre le processeur et le GPU (ce qui est onéreux) afin qu’il puisse passer au rendu de l’UC. Dans certains cas, il est possible qu’il force le rendu de manière imprévisible sur le processeur. En outre, les opérations de rendu qui apparaissent simples peuvent nécessiter des étapes de rendu provisoires temporaires qui ne sont pas exposées dans l’API et qui nécessitent des ressources GPU supplémentaires.

Direct2D fournit un mappage plus direct pour tirer pleinement parti du GPU. Il fournit deux catégories de ressources : indépendantes du périphérique et dépendant du périphérique.

-   Les ressources indépendantes du périphérique, telles que [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), sont conservées sur le processeur.
-   Les ressources dépendantes de l’appareil, telles que [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), sont mappées directement aux ressources sur le GPU (lorsque l’accélération matérielle est disponible). Les appels de rendu sont effectués en combinant les informations de vertex et de couverture d’une géométrie avec les informations de texturation produites par les ressources dépendantes de l’appareil.

Lorsque vous créez des ressources dépendantes de l’appareil, les ressources système (le GPU, s’il est disponible ou le processeur) sont allouées lorsque l’appareil est créé et ne changent pas d’une opération de rendu à une autre. Cette situation élimine le besoin d’un gestionnaire de ressources. Outre les améliorations de performances générales fournies par l’élimination d’un gestionnaire de ressources, ce modèle vous permet de contrôler directement n’importe quel rendu intermédiaire.

Étant donné que Direct2D offre un contrôle très important sur les ressources, vous devez comprendre les différents types de ressources et le moment où ils peuvent être utilisés ensemble.

## <a name="device-independent-resources"></a>Ressources Device-Independent

Comme décrit dans la section précédente, les ressources indépendantes du périphérique résident toujours sur le processeur et ne sont jamais associées à un périphérique de rendu matériel. Les ressources indépendantes du périphérique sont les suivantes :

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) et les interfaces qui héritent de celui-ci.
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) et [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Utilisez un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), lui-même une ressource indépendante du périphérique, pour créer des ressources indépendantes du périphérique. (Pour créer une fabrique, utilisez la fonction [**CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .)

À l’exception des cibles de rendu, toutes les ressources créées par une fabrique sont indépendantes du périphérique. Une cible de rendu est une ressource dépendante de l’appareil.

## <a name="device-dependent-resources"></a>Ressources Device-Dependent

Toute ressource qui n’est pas nommée dans la liste précédente est une ressource dépendante de l’appareil. Les ressources dépendantes de l’appareil sont associées à un appareil de rendu particulier. Lorsque l’accélération matérielle est disponible, cet appareil est le GPU. Dans d’autres cas, il s’agit de l’UC.

Pour créer la plupart des ressources dépendantes de l’appareil, utilisez une cible de rendu. Dans la plupart des cas, utilisez une fabrique pour créer une cible de rendu.

Voici des exemples de ressources dépendantes de l’appareil :

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) et les interfaces qui héritent de celui-ci. Utilisez une cible de rendu pour créer des pinceaux.
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer). Utilisez une cible de rendu pour créer des couches.
-   [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et les interfaces qui héritent de celui-ci. Pour créer une cible de rendu, utilisez une fabrique ou une autre cible de rendu.

> [!Note]  
> à partir de Windows 8, de nouvelles interfaces créent des ressources dépendantes de l’appareil. Un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) et un [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) peuvent partager une ressource si le contexte de périphérique et la ressource sont créés à partir du même **ID2D1Device**.

 

Les ressources dépendantes de l’appareil deviennent inutilisables lorsque les appareils de rendu associés deviennent indisponibles. Cela signifie que lorsque vous recevez l’erreur de recréation de la cible de [**\_ \_ recréation D2DERR**](direct2d-error-codes.md) pour une cible de rendu, vous devez recréer la cible de rendu et toutes ses ressources.

## <a name="sharing-factory-resources"></a>Partage des ressources de la fabrique

Vous pouvez partager toutes les ressources indépendantes des appareils créées par une fabrique avec toutes les autres ressources (indépendantes du périphérique ou de l’appareil) créées par la même fabrique. Par exemple, vous pouvez utiliser deux objets [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) pour dessiner le même [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) si ces deux objets **ID2D1RenderTarget** ont été créés par la même fabrique.

Les interfaces du récepteur ([**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink), [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)et [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) peuvent être partagées avec les ressources créées par toute fabrique. Contrairement à d’autres interfaces dans Direct2D, toute implémentation d’une interface de récepteur peut être utilisée. Par exemple, vous pouvez utiliser votre propre implémentation de **ID2D1SimplifiedGeometrySink**.

## <a name="sharing-render-target-resources"></a>Partage des ressources de la cible de rendu

Votre capacité à partager des ressources créées par une cible de rendu dépend du type de cible de rendu. Quand vous créez une cible de rendu de type [**d2d1 de \_ cible de rendu \_ \_ \_ par défaut**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type), les ressources créées par cette cible de rendu peuvent uniquement être utilisées par cette cible de rendu (sauf si la cible de rendu s’ajuste à l’une des catégories décrites dans les sections suivantes). Cela est dû au fait que vous ne savez pas quel appareil la cible de rendu finit par utiliser : elle peut finir le rendu sur le matériel local, le logiciel ou le matériel d’un client distant. Par exemple, vous pouvez écrire un programme qui cesse de fonctionner lorsqu’il est affiché à distance ou lorsque la taille de la cible de rendu augmente au-delà de la taille maximale prise en charge par le matériel de rendu.

Les sections suivantes décrivent les circonstances dans lesquelles une ressource créée par une cible de rendu peut être partagée avec une autre cible de rendu.

### <a name="hardware-render-targets"></a>Cibles de rendu matériel

Vous pouvez partager des ressources entre n’importe quelle cible de rendu qui utilise explicitement le matériel, tant que le mode de communication à distance est compatible. La compatibilité du mode de communication à distance n’est garantie que lorsque les deux cibles de rendu utilisent l’indicateur d’utilisation **\_ \_ \_ \_ \_ compatible** de l’utilisation de la [**\_ \_ cible \_ \_ \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) de rendu d2d1 ou de l’utilisation de la cible de rendu d2d1, ou si aucun indicateur n’est spécifié. Ces paramètres garantissent que les ressources seront toujours situées sur le même ordinateur. Pour spécifier un mode d’utilisation, définissez le champ **utilisation** de la structure des propriétés de la [**\_ \_ cible \_ de rendu d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que vous avez utilisée pour créer la cible de rendu avec un ou plusieurs indicateurs d’utilisation de la **\_ \_ cible \_ de rendu d2d1** .

Pour créer une cible de rendu qui utilise explicitement le rendu matériel, définissez le champ **type** de la structure des propriétés de la [**\_ cible de rendu \_ \_ d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) que vous avez utilisée pour créer la cible de rendu sur le matériel du type de [**cible de \_ rendu \_ \_ \_ d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).

### <a name="dxgi-surface-render-targets"></a>Cibles de rendu de surface DXGI

Vous pouvez partager des ressources créées par une cible de rendu de surface DXGI avec toute autre cible de rendu de surface DXGI qui utilise le même appareil Direct3D sous-jacent.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Cibles de rendu compatibles et bitmaps partagées

Vous pouvez partager des ressources entre une cible de rendu et des cibles de rendu compatibles qui sont créées par cette cible de rendu. Pour créer une cible de rendu compatible, utilisez la méthode [**ID2D1RenderTarget :: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .

Vous pouvez utiliser la méthode [**ID2D1RenderTarget :: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) pour créer un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) qui peut être partagé entre les deux cibles de rendu spécifiées dans l’appel de méthode, si la méthode est réussie. Cette méthode fonctionnera tant que les deux cibles de rendu utilisent le même appareil sous-jacent pour le rendu.

 

 
