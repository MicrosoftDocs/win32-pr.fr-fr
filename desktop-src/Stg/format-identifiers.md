---
title: Identificateurs de format
description: Les valeurs de jeu de propriétés sont stockées dans une section marquée avec un FMTID unique.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificateurs de format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309813"
---
# <a name="format-identifiers"></a>Identificateurs de format

Les valeurs de jeu de propriétés sont stockées dans une section marquée avec un FMTID unique. Par exemple, le FMTID pour la propriété informations résumées COM définie est **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Pour définir un FMTID pour le jeu de propriétés d’informations de synthèse, utilisez la macro **définir le \_ GUID** dans un fichier include pour le code qui manipule le jeu de propriétés.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Tout code qui requiert FMTID pour le jeu de propriétés d’informations de synthèse peut y accéder via la variable *fmtid \_ SummaryInformation* .

Lors du stockage de jeux de propriétés dans des instances de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , convertissez le fmtid en un nom de chaîne pour l’objet de stockage.

 

 




