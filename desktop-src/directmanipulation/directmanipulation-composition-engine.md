---
description: Pour pouvoir générer des mises à jour visuelles, l’application doit utiliser IDirectManipulationCompositor.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Moteur de composition
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: aa4d922893472c1fe235bae60e41a00924d13bba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481600"
---
# <a name="composition-engine"></a>Moteur de composition

Pour pouvoir générer des mises à jour visuelles, l’application doit utiliser [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor). Cet objet est chargé de mettre à jour les éléments visuels basés sur des mises à jour de [manipulation directe](direct-manipulation-portal.md) , de générer des mises à jour par inertie et de fournir des informations de minutage de composition pour la manipulation directe. en outre, une application doit utiliser le [DCompManipulationCompositor](direct-manipulation-guids.md) fourni par la [manipulation directe](direct-manipulation-portal.md), qui gérera toutes les mises à jour visuelles pour le compte de l’application et les mises à jour

Le [DCompManipulationCompositor](direct-manipulation-guids.md) est une implémentation de l’interface [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) qui encapsule [DirectComposition](../directcomp/directcomposition-portal.md). Plutôt que de faire en sorte que l’application applique la sortie, par le biais de cet objet compositeur, la [manipulation directe](direct-manipulation-portal.md) peut appliquer la sortie en définissant les transformations directement sur l’arbre DirectComposition. À l’aide de cette configuration, l’entrée peut être traitée et des transformations de sortie peuvent être appliquées, quelle que soit l’activité sur le thread d’interface utilisateur.

Pour fournir des informations de [manipulation directe](direct-manipulation-portal.md) sur le minutage du moteur de composition, la classe [DCompManipulationCompositor](direct-manipulation-guids.md) implémente l’interface [**IDirectManipulationFrameInfoProvider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) . Lors de la création d’une fenêtre d’affichage, [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) est le pointeur [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) obtenu à partir de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour une instance de **IDirectManipulationFrameInfoProvider**. Le pointeur **IDirectManipulationFrameInfoProvider** est passé à la fonction [**IDirectManipulationManager :: CreateViewport ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) .
