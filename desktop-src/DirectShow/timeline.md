---
description: Durée
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Durée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651251"
---
# <a name="timeline"></a>Durée

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

L’objet Timeline gère tous les objets d’un projet de montage vidéo. Pour créer cet objet, appelez **CoCreateInstance**. L’identificateur de classe est CLSID \_ AMTimeline.

pour lire Windows fichiers de™ multimédia, l’application doit fournir un certificat logiciel, également appelé clé. Inscrivez l’application en tant que fournisseur de clé via l’interface **IObjectWithSite** de la chronologie. pour plus d’informations, consultez [déverrouillage du kit de développement logiciel (SDK) Windows Media Format](unlocking-the-windows-media-format-sdk.md).

L’objet Timeline expose les interfaces suivantes :

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle de chronologie](the-timeline-model.md)
</dt> <dt>

[Construction d’une chronologie](constructing-a-timeline.md)
</dt> </dl>

 

 



