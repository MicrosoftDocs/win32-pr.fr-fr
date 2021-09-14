---
title: Magasins en ligne privés
description: Magasins en ligne privés
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Lecteur Windows Media les magasins en ligne, privés
- magasins en ligne, privés
- tapez 1 magasins en ligne, privés
- tapez 2 magasins en ligne, privés
- magasins en ligne privés
- Registre, magasins en ligne privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292890"
---
# <a name="private-online-stores"></a>Magasins en ligne privés

Lecteur Windows Media 10 ou version ultérieure prend en charge les magasins en ligne privés ; autrement dit, les magasins qui sont visibles uniquement pour certains utilisateurs. Pour qu’un magasin en ligne privé soit visible par l’utilisateur actuel, il doit y avoir une entrée qui représente la Banque en ligne privée sous la clé de Registre suivante.

HKEY \_ \_ logiciel utilisateur \\ actuel \\ Microsoft \\ MediaPlayer \\ PrivateServices

L’entrée de registre requise doit avoir le format suivant.



| Nom                                                         | Type           | Valeur                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Tout nom choisi par la personne qui crée l’entrée de Registre | **\_valeur DWORD reg** | Nombre, fourni par Microsoft, qui identifie le magasin en ligne privé |



 

le contrôle Lecteur Windows Media 10 ActiveX prend en charge les magasins en ligne privés uniquement si le contrôle s’exécute en mode distant. le contrôle Lecteur Windows Media 11 ActiveX prend en charge les magasins en ligne privés, que le contrôle s’exécute en mode distant ou non.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




