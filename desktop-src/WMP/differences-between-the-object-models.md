---
title: Différences entre les modèles objet
description: Différences entre les modèles objet
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Lecteur Windows Media, modèle objet
- Lecteur Windows Media modèle objet, différences de version
- modèle objet, différences de version
- contrôle de ActiveX Lecteur Windows Media, différences de version
- contrôle de ActiveX, différences de version
- Lecteur Windows Media contrôle de ActiveX Mobile, différences de version
- Lecteur Windows Media Mobile, modèle objet
- Guide de migration, différences de version
- versions de Lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008464"
---
# <a name="differences-between-the-object-models"></a>Différences entre les modèles objet

il existe deux principales différences entre le modèle objet Lecteur Windows Media 6,4 et le modèle objet Lecteur Windows Media 7 ou version ultérieure.

-   **CLSID** le modèle objet Lecteur Windows Media 7 ou version ultérieure est un départ complet du modèle objet version 6,4. La spécification COM (Component Object Model) requiert que toutes les interfaces existantes continuent de fonctionner dans les nouvelles versions d’un composant COM. Cela signifie que de nouvelles interfaces peuvent être ajoutées à un composant COM, mais que les interfaces existantes ne doivent jamais être modifiées, ce qui garantit que le code client plus ancien fonctionnera toujours avec le composant spécifique qu’il a été conçu pour être utilisé. par conséquent, la Lecteur Windows Media 7 ou une version ultérieure ActiveX contrôle a un nouvel ID de classe : 6BF52A52-394A-11D3-B153-00C04F79FAA6. Si vous souhaitez tirer parti de la nouvelle fonctionnalité du contrôle pour cette version, vous devez modifier votre CLSID.
-   **Modèle d’objet hiérarchique** si vous avez utilisé le contrôle Lecteur Windows Media 6,4 ActiveX, vous avez peut-être remarqué que toutes les propriétés, méthodes et événements sont accessibles par le biais du même objet : l’objet **Player** . en revanche, le modèle objet Lecteur Windows Media 7 ou version ultérieure est organisé comme une hiérarchie d’objets. L’objet **Player** est toujours l’objet racine, mais les fonctions sont désormais accessibles par le biais de divers objets enfants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> </dl>

 

 




