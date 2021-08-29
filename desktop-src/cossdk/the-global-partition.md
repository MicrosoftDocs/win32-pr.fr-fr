---
description: Partition globale
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: Partition globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63fd66e8bb4401465a604b187d8638b60993b45c130d18ab2c4c5d054d9686d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636789"
---
# <a name="the-global-partition"></a>Partition globale

Outre les partitions définies par l’administrateur et les jeux de partitions, il existe une partition spéciale sur chaque ordinateur, appelée *partition globale*. Une partition globale est créée automatiquement lors de l’installation de COM+. La partition globale est conçue pour contenir des applications à l’échelle du système qui doivent être accessibles à tous les utilisateurs sur un serveur ou dans le domaine. L’installation d’une application dans la partition globale supprime la nécessité d’installer une copie de l’application dans le jeu de partitions de chaque utilisateur individuel.

Si le jeu de partitions d’un utilisateur n’inclut pas une application spécifique à laquelle l’utilisateur tente d’accéder, mais que cette application est installée dans la partition globale, l’application est activée à partir de la partition globale. Dans ce cas, toutefois, tous les composants de l’application installée dans la partition globale doivent être marqués comme des composants publics, et non privés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Partitions par défaut](default-partitions.md)
</dt> <dt>

[Partitions locales](local-partitions.md)
</dt> <dt>

[Propriétés de partition](partition-properties.md)
</dt> <dt>

[Partitions et Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



