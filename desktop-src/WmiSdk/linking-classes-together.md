---
description: Les fournisseurs WMI sont généralement conçus pour fournir des informations sur un objet géré spécifique sur un seul ordinateur.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Liaison de classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534731"
---
# <a name="linking-classes-together"></a>Liaison de classes

Les fournisseurs WMI sont généralement conçus pour fournir des informations sur un objet géré spécifique sur un seul ordinateur. S’il existe une propriété commune qui peut servir de clé pour identifier de façon unique toutes les différentes instances sources, utilisez le [fournisseur d’affichage](view-provider.md) pour combiner les propriétés de différentes classes, espaces de noms ou ordinateurs en une seule classe.

Vous devez d’abord [inscrire le fournisseur d’affichage](registering-the-view-provider.md). Après l’inscription, vous pouvez créer les types de classes d’affichage suivants :

-   [Vue de jointure](creating-a-new-instance-from-old-properties.md)

    Instances de différentes classes connectées par une valeur de propriété commune.

-   [Vue Association](associating-instances-between-namespaces.md)

    Vues des classes d’association existantes à travers la limite de l’espace de noms.

-   [Vue Union](creating-a-union-view-class.md)

    Union d’une ou plusieurs instances.

 

 



