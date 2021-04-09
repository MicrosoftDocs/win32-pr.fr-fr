---
description: Interrogation des propriétés disponibles
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Interrogation des propriétés disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111286"
---
# <a name="querying-for-available-properties"></a>Interrogation des propriétés disponibles

Si vous écrivez un outil d’administration à usage général, vous devrez probablement écrire des routines pour définir des propriétés en général. Pour prendre cela en charge, il existe une fonctionnalité qui vous permet de Rechercher dynamiquement les propriétés disponibles pour les éléments d’une collection donnée.

La collection [**PropertyInfo**](propertyinfo.md) est disponible à partir de n’importe quel regroupement que vous êtes susceptible de contenir. La collection **PropertyInfo** contient un élément pour chaque propriété disponible. Vous pouvez énumérer ces éléments pour déterminer si une propriété donnée est disponible.

Vous pouvez obtenir la collection [**PropertyInfo**](propertyinfo.md) à partir de n’importe quelle collection que vous conservez à l’aide de la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , en laissant le deuxième paramètre vide à l’emplacement où vous spécifiez normalement la propriété de clé d’un élément parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention et définition des propriétés](getting-and-setting-properties.md)
</dt> <dt>

[Interdépendances entre les propriétés](interdependencies-between-properties.md)
</dt> <dt>

[Enregistrement ou rejet des modifications](saving-or-discarding-changes.md)
</dt> </dl>

 

 



