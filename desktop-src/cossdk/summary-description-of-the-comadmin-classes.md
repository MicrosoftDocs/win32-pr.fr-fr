---
description: Il existe trois classes fournies par la bibliothèque comadmin (comadmin.dll), chacune implémentant une interface COM double.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Description Résumé des classes comadmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dbcb1ec19b7178b94eae033b1f24d1956e1de373a99ff6545492fabe7b158c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812472"
---
# <a name="summary-description-of-the-comadmin-classes"></a>Description Résumé des classes comadmin

Il existe trois classes fournies par la bibliothèque comadmin (comadmin.dll), chacune implémentant une interface COM double. Vous utilisez des objets créés à partir de ces classes pour accéder au catalogue, pour représenter des collections dans le catalogue et pour représenter les éléments contenus dans des collections.

## <a name="comadmincatalog"></a>COMAdminCatalog

La classe [**COMAdminCatalog**](comadmincatalog.md) représente le catalogue lui-même. Un objet créé à partir de **COMAdminCatalog** est l’objet fondamental que vous utilisez dans l’administration par programme. Outre l’établissement de la connexion de base avec le serveur de catalogue quand vous l’instanciez, **COMAdminCatalog** fournit des méthodes qui vous permettent d’effectuer les opérations suivantes :

-   Obtient des collections sur le catalogue.
-   Connecter au serveur de catalogue sur une machine distante.
-   Installer, exporter, démarrer, arrêter et obtenir des informations sur les applications COM+.
-   Installer des composants dans des applications COM+ et obtenir des informations sur les composants.
-   Démarrez, arrêtez ou actualisez les services s’exécutant sur l’ordinateur.
-   Actualisez, restaurez ou sauvegardez les informations du catalogue.

Dans COM+ 1,0, la classe [**COMAdminCatalog**](comadmincatalog.md) implémente l’interface [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) . Dans COM+ 1,5, la classe **COMAdminCatalog** implémente [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) en tant qu’interface par défaut.

## <a name="comadmincatalogcollection"></a>COMAdminCatalogCollection

La classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) représente n’importe quelle collection dans le catalogue, en fournissant une chaîne nommant la collection particulière au moment de l’instanciation de l’objet. (Les collections de catalogues disponibles sont nommées dans la table dans les [collections d’administration com+](com--administration-collections.md).) Les objets sont créés à partir de cette classe lors de la récupération d’une collection de niveau supérieur en appelant la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) de l’objet [**COMAdminCatalog**](comadmincatalog.md) . Ces objets sont également créés lors de la récupération d’une collection enfant en appelant la méthode **GetCollection** de son objet de collection parent. Les objets **COMAdminCatalogCollection** vous permettent d’effectuer les opérations suivantes :

-   Énumérer les éléments contenus dans la collection.
-   Récupère un élément de la collection.
-   Ajoutez ou supprimez des éléments dans la collection.
-   Enregistrez ou ignorez toutes les modifications en attente apportées à la collection ou aux éléments qu’elle contient.
-   Obtenir une autre collection dans le catalogue.

La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implémente l’interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) représente tout élément contenu dans une collection. Les objets sont créés à partir de cette classe lors de l’obtention d’un élément via la propriété [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) d’un objet de collection de catalogues. Les objets créés à partir de la classe **COMAdminCatalogObject** vous permettent d’effectuer les opérations suivantes :

-   Obtient ou définit les propriétés prises en charge par l’élément que l’objet est utilisé pour représenter.
-   Obtenir des informations sur l’élément et ses propriétés.

La classe [**COMAdminCatalogObject**](comadmincatalogobject.md) implémente l’interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès au catalogue COM+](accessing-the-com--catalog.md)
</dt> <dt>

[Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



