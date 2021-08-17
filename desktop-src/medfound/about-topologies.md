---
description: À propos des topologies
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: À propos des topologies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9410207ed5f235f61e167564f7a5dee8a1367044032be0a15cef9ac3b95fb9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975111"
---
# <a name="about-topologies"></a>À propos des topologies

Une topologie est un objet qui représente la façon dont les données circulent dans le pipeline. Une application crée une topologie pour décrire le chemin d’accès de chaque flux de la source du média à un récepteur multimédia. L’application transmet la topologie à la session multimédia, et la session multimédia utilise la topologie pour contrôler le Workflow.

Les composants de traitement de données dans le pipeline (sources de média, transformations et récepteurs multimédias) sont représentés dans la topologie sous forme de *nœuds*. Le déroulement des données d’un composant vers un autre est représenté par une connexion entre les nœuds. Les types de nœuds suivants sont définis :

-   Nœud source : représente un flux multimédia sur une source de média.
-   Nœud de transformation : représente une transformation de Media Foundation (MFT).
-   Nœud de sortie : représente un récepteur de flux sur un récepteur multimédia.
-   Nœud Tee : représente une fourche dans le flux. Les nœuds tee sont une exception à la règle qu’un nœud représente un objet Pipeline. Contrairement à d’autres types de nœuds, le nœud tee dirige simplement le workflow de données.

Une topologie fonctionnelle doit contenir au moins un nœud source connecté à un nœud de sortie, éventuellement via un ou plusieurs nœuds de transformation. Par exemple, le diagramme suivant illustre une topologie simple avec un flux.

![diagramme qui montre une topologie avec un flux.](images/topology01.png)

Pour la lecture de fichier, le nœud de transformation peut représenter un décodeur et le nœud de sortie représente le convertisseur audio ou vidéo. Pour l’encodage de fichier, le nœud de transformation représente un encodeur et le nœud de sortie représente un récepteur d’archive, tel que le récepteur de fichiers ASF.

Si deux nœuds sont connectés, le nœud qui produit des données est appelé nœud *amont* , et le nœud qui reçoit les données est appelé nœud en *aval* . Par exemple, dans le diagramme précédent, le nœud source est en amont du nœud transformer.

Dans une paire de nœuds connectés, le point de connexion sur le nœud amont est appelé une *sortie*. Le point de connexion sur le nœud en aval est appelé une *entrée*. Le diagramme suivant montre une paire de nœuds avec leurs points de connexion, et le Flow de données entre eux. Les points de connexion ne sont pas représentés en tant qu’objets distincts dans la topologie. Ils sont spécifiés par la valeur d’index sur l’objet de nœud.

![diagramme qui affiche deux nœuds connectés.](images/topology04.png)

Un nœud source ne peut avoir aucune entrée. Par conséquent, il ne peut pas y avoir de nœuds en amont d’un nœud source. De même, un nœud de sortie ne peut pas avoir de sorties, et il ne peut pas y avoir de nœuds en aval d’un nœud de sortie. Une chaîne de nœuds d’un nœud source à un nœud de sortie est appelée une *branche* de la topologie. Le premier diagramme de cette rubrique illustre une topologie avec une seule branche. En général, il existe une branche par flux. Pour lire un fichier avec un flux audio et un flux vidéo, par exemple, nécessite une topologie avec deux branches.

## <a name="partial-topologies"></a>Topologies partielles

Une topologie complète ou *complète* contient un nœud pour chaque objet de pipeline qui est nécessaire. Toutefois, l’application n’a pas toujours besoin de créer une topologie complète. Au lieu de cela, il crée une topologie *partielle* qui omet un ou plusieurs nœuds de transformation.

La session de média termine la topologie à l’aide d’un objet appelé *chargeur de topologie*. Le chargeur de topologie convertit les topologies partielles en topologies complètes en insérant les transformations nécessaires. Le processus de conversion est appelé *résolution* de la topologie.

Par exemple, pour lire un flux audio encodé, la topologie doit avoir un décodeur entre les nœuds source et de sortie. L’application crée une topologie partielle qui connecte directement le nœud source au nœud de sortie, sans le décodeur. Le chargeur de topologie examine les formats de flux, recherche le décodeur approprié et insère un nœud de transformation dans la topologie.

Le diagramme suivant montre la topologie partielle créée par l’application.

![diagramme qui montre un partiel avec un nœud source et un nœud de sortie.](images/topology02.png)

Le diagramme suivant montre la topologie complète une fois que le chargeur de topologie l’a résolu. Dans cet exemple, le chargeur de topologie a inséré un nœud de transformation pour le décodeur.

![diagramme qui montre une topologie complète.](images/topology03.png)

Dans la version actuelle de Media Foundation, le chargeur de topologie prend en charge les topologies pour la lecture. Pour l’encodage de fichier et d’autres scénarios, l’application doit construire une topologie complète.

Les applications peuvent également créer le chargeur de topologie et l’utiliser directement. Par exemple, vous pouvez utiliser le chargeur de topologie pour résoudre une topologie partielle, puis modifier la topologie complète avant de l’attribuer à la session multimédia. Pour créer le chargeur de topologie, appelez [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Topologies](topologies.md)
</dt> </dl>

 

 



