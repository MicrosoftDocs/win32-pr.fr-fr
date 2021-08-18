---
description: Moteur de rendu de base
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Moteur de rendu de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a3e04e1ad32c163db93794e075ff7933f041c3270ab8412cbd5b5a68b4a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955571"
---
# <a name="basic-render-engine"></a>Moteur de rendu de base

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L’objet de moteur de rendu de base restitue la sortie non compressée d’une chronologie. Pour créer cet objet, appelez **CoCreateInstance**. Pour la sortie compressée, utilisez le moteur de rendu intelligent. L’identificateur de classe est CLSID \_ RenderEngine.

Le moteur de rendu de base expose les interfaces suivantes :

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un Project](rendering-a-project.md)
</dt> <dt>

[Moteur de rendu intelligent](smart-render-engine.md)
</dt> </dl>

 

 



