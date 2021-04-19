---
description: Moteur de rendu intelligent
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Moteur de rendu intelligent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544555"
---
# <a name="smart-render-engine"></a>Moteur de rendu intelligent

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’objet de moteur de rendu intelligent restitue la sortie compressée à partir d’une chronologie. Pour créer cet objet, appelez **CoCreateInstance**. Pour la sortie non compressée, utilisez le moteur de rendu de base. L’identificateur de classe est CLSID \_ SmartRenderEngine.

Le moteur de rendu intelligent expose les interfaces suivantes :

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un projet](rendering-a-project.md)
</dt> <dt>

[Moteur de rendu de base](basic-render-engine.md)
</dt> </dl>

 

 



