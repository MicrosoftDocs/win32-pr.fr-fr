---
description: Durée
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Durée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857422"
---
# <a name="timeline"></a>Durée

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

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

 

 



