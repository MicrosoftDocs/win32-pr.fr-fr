---
description: Les identificateurs spécifient les noms des colonnes (parfois appelées propriétés), les catalogues et les alias.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112423"
---
# <a name="identifiers"></a>Identificateurs

Les identificateurs spécifient les noms des colonnes (parfois appelées propriétés), les catalogues et les alias. Par exemple, System. ItemName et System. DateCreated sont les identificateurs de deux colonnes de propriété définies par le système. En revanche, les littéraux spécifient des valeurs numériques et de chaîne.


Vous pouvez créer des identificateurs d’une longueur maximale de 128 caractères, et dans l’un des deux types, distingués par les caractères utilisés dans le nom de l’identificateur :

-   Les **identificateurs réguliers** contiennent uniquement les caractères a-z, a-z, 0-9, le trait de soulignement () et le \_ point (.), et ils commencent par une lettre. Vous n’avez pas besoin de placer les identificateurs réguliers entre guillemets doubles ("").
-   Les **identificateurs délimités** peuvent contenir n’importe quel caractère Unicode valide et doivent être placés entre guillemets doubles.

> [!Note]  
> Dans les clauses FREETEXT et CONTAINs, vous pouvez utiliser l’astérisque ( \* ) comme identificateur de colonne spécial lorsque vous souhaitez spécifier que la recherche Windows inclut toutes les propriétés indexées dans la requête. Bien qu’il ne s’agisse pas d’un identificateur régulier, il ne requiert pas de guillemets doubles.

 

 

 



