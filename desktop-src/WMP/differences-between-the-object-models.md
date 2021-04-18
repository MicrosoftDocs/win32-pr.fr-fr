---
title: Différences entre les modèles objet
description: Différences entre les modèles objet
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Lecteur Windows Media, modèle objet
- Modèle d’objet du lecteur Windows Media, différences entre les versions
- modèle objet, différences de version
- Contrôle ActiveX du lecteur Windows Media, différences entre les versions
- Contrôle ActiveX, différences de version
- Windows Media Player Mobile contrôle ActiveX, différences de version
- Windows Media Player Mobile, modèle objet
- Guide de migration, différences de version
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512678"
---
# <a name="differences-between-the-object-models"></a>Différences entre les modèles objet

Il existe deux principales différences entre le modèle d’objet Windows Media Player 6,4 et le modèle objet Windows Media Player 7 ou version ultérieure.

-   **CLSID** Le modèle objet Windows Media Player 7 ou version ultérieure est un départ complet du modèle objet version 6,4. La spécification COM (Component Object Model) requiert que toutes les interfaces existantes continuent de fonctionner dans les nouvelles versions d’un composant COM. Cela signifie que de nouvelles interfaces peuvent être ajoutées à un composant COM, mais que les interfaces existantes ne doivent jamais être modifiées, ce qui garantit que le code client plus ancien fonctionnera toujours avec le composant spécifique qu’il a été conçu pour être utilisé. Par conséquent, le contrôle ActiveX Windows Media Player 7 ou version ultérieure a un nouvel ID de classe : 6BF52A52-394A-11D3-B153-00C04F79FAA6. Si vous souhaitez tirer parti de la nouvelle fonctionnalité du contrôle pour cette version, vous devez modifier votre CLSID.
-   **Modèle d’objet hiérarchique** Si vous avez utilisé le contrôle ActiveX du lecteur Windows Media 6,4, vous avez peut-être remarqué que toutes les propriétés, méthodes et événements sont accessibles par le biais du même objet : l’objet **Player** . En revanche, le modèle objet Windows Media Player 7 ou version ultérieure est organisé comme une hiérarchie d’objets. L’objet **Player** est toujours l’objet racine, mais les fonctions sont désormais accessibles par le biais de divers objets enfants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> </dl>

 

 




