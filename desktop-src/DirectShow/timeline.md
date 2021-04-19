---
description: Durée
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Durée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539762"
---
# <a name="timeline"></a>Durée

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L’objet Timeline gère tous les objets d’un projet de montage vidéo. Pour créer cet objet, appelez **CoCreateInstance**. L’identificateur de classe est CLSID \_ AMTimeline.

Pour lire des fichiers Windows Media™, l’application doit fournir un certificat logiciel, également appelé clé. Inscrivez l’application en tant que fournisseur de clé via l’interface **IObjectWithSite** de la chronologie. Pour plus d’informations, consultez [déverrouillage du kit de développement logiciel (SDK) de format Windows Media](unlocking-the-windows-media-format-sdk.md).

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

 

 



