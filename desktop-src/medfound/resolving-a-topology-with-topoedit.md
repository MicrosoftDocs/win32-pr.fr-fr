---
description: Résolution d’une topologie avec TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Résolution d’une topologie avec TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201851"
---
# <a name="resolving-a-topology-with-topoedit"></a>Résolution d’une topologie avec TopoEdit

Il existe deux types de topologies :

-   Topologie partielle. Le nœud source est directement connecté au nœud de sortie. Dans certains cas, une topologie partielle peut avoir des nœuds de transformation intermédiaires, tels que des effets, mais pas tous. Les nœuds de transformation qui sont omis sont généralement des décodeurs ou des MFTs de conversion de format, tels que des convertisseurs de couleurs et des échantillonnages audio.

-   Topologie complète. Le nœud source est connecté au nœud de sortie via un nœud de transformation. Ce type de topologie doit avoir chaque nœud pour traiter les données.

TopoEdit peut uniquement lire des topologies complètes. TopoEdit utilise l’objet de chargeur de topologie, fourni par Media Foundation, pour convertir une topologie partielle en une topologie complète en insérant les transformations requises. Le processus de création d’une topologie complète est appelé résolution d’une topologie.

Pour plus d’informations sur les types de topologies, consultez la section topologies partielles dans [à propos des topologies](about-topologies.md).

Avant de résoudre une topologie, assurez-vous que :

-   La topologie contient un nœud source et un nœud de sortie.

-   Les nœuds source et de sortie sont connectés par une connexion de nœud valide. Pendant la résolution de la topologie, le chargeur de topologie vérifie la compatibilité du type de média des nœuds. S’il existe une connexion de nœud non valide, le processus échoue et un message d’erreur s’affiche.

Pour résoudre une topologie, dans le menu **topologie** , cliquez sur **résoudre** la topologie.

La barre d’outils indique l’état de la topologie : **\[ résolu \]** ou **\[ non résolu \]**.

Si TopoEdit résout correctement une topologie, l’état de la **topologie** est défini sur **\[ résolu \]** et les contrôles de lecture sont activés.

Chaque fois que vous apportez des modifications à la topologie, l’état de la **topologie** est défini sur **\[ non résolu \]** , ce qui indique qu’il doit être résolu à nouveau.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de topologies à l’aide de TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



