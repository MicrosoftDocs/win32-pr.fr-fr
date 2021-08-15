---
description: Remplissage des collections COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Remplissage des collections COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256c246a4f5d176e6b706515d02c0dd5cf68f7ae5a9aff7f89949da14510636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990669"
---
# <a name="populating-com-collections"></a>Remplissage des collections COM+

Une fois que vous avez récupéré une collection et que vous pouvez travailler directement avec les éléments qu’elle contient, vous devez remplir la collection à l’aide de la méthode [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Cette instruction extrait des données pour le contenu de la collection à partir du catalogue COM+.

Il est important de comprendre que chaque fois que vous utilisez des objets comadmin pour manipuler des éléments ou des données dans des collections, vous travaillez vraiment sur des données mises en cache de façon temporaire ; vous ne travaillez pas directement avec le catalogue persistant. Rien ne fait que vous utilisez une collection ou l’un de ses éléments est reflété sur le catalogue tant que vous n’avez pas appelé [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur la collection. Pour plus d’informations, consultez [enregistrement ou rejet des modifications](saving-or-discarding-changes.md).

Tout appel ultérieur à [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), avant d’appeler [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), a pour effet d’ignorer les modifications en attente de tous les éléments de la collection. Le **remplissage** remplit toujours le cache dans lequel vous travaillez, quelles que soient les données qui sont conservées dans le magasin de données de catalogue sous-jacent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Navigation dans la hiérarchie de regroupement COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Interrogation des collections associées disponibles](querying-for-available-related-collections.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



