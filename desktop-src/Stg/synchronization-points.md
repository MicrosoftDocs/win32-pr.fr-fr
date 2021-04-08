---
title: Points de synchronisation
description: Lorsque les jeux de propriétés sont pris en charge sur le même objet que IStorage, il est important de connaître les points de synchronisation entre le stockage de base et le stockage des propriétés.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa156efbb1573b2954c1f7da07a58ed663c71781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675910"
---
# <a name="synchronization-points"></a>Points de synchronisation

Lorsque les jeux de propriétés sont pris en charge sur le même objet que [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), il est important de connaître les points de synchronisation entre le stockage de base et le stockage des propriétés.

Le stockage de jeux de propriétés contient le flux de jeu de propriétés dans une mémoire tampon interne jusqu’à ce que cette mémoire tampon soit validée par le biais de la méthode [**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) . Cela est vrai si [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) a été ouvert en mode traité ou en mode direct.

 

 




