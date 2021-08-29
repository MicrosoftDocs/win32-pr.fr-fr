---
description: Moteur de rendu intelligent
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Moteur de rendu intelligent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3472d096d1c3918a9bf1a45ae788a535fd65bfe4e4084c6b044516db01440d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072553"
---
# <a name="smart-render-engine"></a>Moteur de rendu intelligent

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L’objet de moteur de rendu intelligent restitue la sortie compressée à partir d’une chronologie. Pour créer cet objet, appelez **CoCreateInstance**. Pour la sortie non compressée, utilisez le moteur de rendu de base. L’identificateur de classe est CLSID \_ SmartRenderEngine.

Le moteur de rendu intelligent expose les interfaces suivantes :

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un Project](rendering-a-project.md)
</dt> <dt>

[Moteur de rendu de base](basic-render-engine.md)
</dt> </dl>

 

 



