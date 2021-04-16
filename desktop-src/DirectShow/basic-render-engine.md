---
description: Moteur de rendu de base
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Moteur de rendu de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522220"
---
# <a name="basic-render-engine"></a>Moteur de rendu de base

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’objet de moteur de rendu de base restitue la sortie non compressée d’une chronologie. Pour créer cet objet, appelez **CoCreateInstance**. Pour la sortie compressée, utilisez le moteur de rendu intelligent. L’identificateur de classe est CLSID \_ RenderEngine.

Le moteur de rendu de base expose les interfaces suivantes :

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un projet](rendering-a-project.md)
</dt> <dt>

[Moteur de rendu intelligent](smart-render-engine.md)
</dt> </dl>

 

 



