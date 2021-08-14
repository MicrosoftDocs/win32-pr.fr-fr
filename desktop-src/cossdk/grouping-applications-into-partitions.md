---
description: Regroupement d’applications en partitions
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Regroupement d’applications en partitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40491e95313544a32e23db78d8959736665db8c21782d3f1b30729e6eda6f1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991099"
---
# <a name="grouping-applications-into-partitions"></a>Regroupement d’applications en partitions

Lorsque vous décidez comment regrouper des applications en partitions, les administrateurs doivent être conscients de certaines règles et restrictions, y compris les suivantes :

-   Une application peut être installée dans une ou plusieurs partitions.
-   Une seule instance d’un composant donné peut exister dans une application.

## <a name="public-and-private-components"></a>Composants publics et privés

D’autres restrictions existent quand vous décidez comment grouper des applications COM+. Ces restrictions s’appliquent aux composants publics et privés au sein d’une application. Les composants de l’application peuvent généralement être publics ou privés. Toutefois, lorsque vous regroupez des applications en partitions, les administrateurs doivent tenir compte de certaines restrictions concernant les composants publics et privés. Le tableau suivant répertorie ces restrictions.



| Si une application est :              | Les composants d’une partition peuvent être :                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Une application serveur<br/>    | Public et privé.<br/>                                                                                           |
| Une application de bibliothèque<br/>   | Public uniquement. Dans le cas contraire, l’application appelants pourrait avoir les mêmes composants, ce qui créerait une ambiguïté.<br/> |
| Dans la partition globale<br/> | Public uniquement. Cela garantit la compatibilité descendante.<br/>                                                             |



 

## <a name="application-ids"></a>ID d’application

Chaque application COM+ installée sur un ordinateur possède un ID d’application unique. Toutefois, les noms d’application ne doivent être uniques que dans une seule partition et non sur l’intégralité de l’ordinateur.

Le tableau suivant montre ce qui se passe à l’ID d’application lorsqu’une application est importée dans une partition ou exportée à partir d’une partition.



| Si une application est :                                              | Ensuite, l’ID d’application :                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importé dans la partition globale<br/>                        | Reste le même<br/>                 |
| Importé dans une partition autre que la partition globale<br/> | Est modifié<br/>                       |
| Exporté<br/>                                                | Est inclus dans le fichier exporté<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Collecte des métriques de partition](collecting-partition-metrics.md)
</dt> <dt>

[Configuration du cache de partition](configuring-the-partition-cache.md)
</dt> <dt>

[Gestion des partitions locales](managing-local-partitions.md)
</dt> <dt>

[Gestion des partitions dans Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Définition des droits d’administration pour une partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




