---
description: Dans COM+, l’état transitoire partagé pour les objets est géré à l’aide du gestionnaire de propriétés partagées (SPM). Le SPM est un distributeur de ressources que vous pouvez utiliser pour partager l’état entre plusieurs objets au sein d’un processus serveur.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Concepts de Gestionnaire de propriétés partagés COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411128"
---
# <a name="com-shared-property-manager-concepts"></a>Concepts de Gestionnaire de propriétés partagés COM+

Dans COM+, l’état transitoire partagé pour les objets est géré à l’aide du gestionnaire de propriétés partagées (SPM). Le SPM est un distributeur de ressources que vous pouvez utiliser pour partager l’état entre plusieurs objets au sein d’un processus serveur.

Vous ne pouvez pas utiliser de variables globales dans un environnement distribué en raison de problèmes de concurrence et de collision de noms. Le gestionnaire de propriétés partagées élimine les conflits de noms en fournissant des groupes de propriétés partagés, qui établissent des espaces de noms uniques pour les propriétés partagées qu’ils contiennent. Le SPM implémente également des verrous et des sémaphores pour aider à protéger les propriétés partagées de l’accès simultané, ce qui peut entraîner la perte de mises à jour et le fait de conserver les propriétés dans un État imprévisible.

> [!Note]  
> L’état transitoire partagé est des informations d’État conservées en mémoire qui ne survivent pas aux défaillances du système. Les informations sont conçues pour être partagées par plusieurs objets entre les limites des transactions (mais pas entre les processus).

 

Les propriétés partagées stockées dans le SPM sont uniquement disponibles pour les objets qui s’exécutent dans le même processus. Cela signifie que les objets qui utiliseront le SPM pour le stockage des valeurs et qui devront avoir accès à ces valeurs doivent être installés dans le cadre de la même application COM+. Il est possible pour les administrateurs système de déplacer des classes COM+ d’un package à un autre après le déploiement de votre application COM+. Si vous vous fiez à plusieurs objets qui partagent des propriétés via le SPM, vous devez clairement documenter qu’ils doivent être installés dans la même application COM+.

Il est également important que les composants partageant des propriétés aient le même attribut d’activation. Si deux composants dans le même package ont des attributs d’activation différents, ils ne peuvent généralement pas partager de propriétés. Par exemple, si un composant est configuré pour s’exécuter dans un processus client et que l’autre est configuré pour s’exécuter dans un processus serveur, ses objets s’exécutent généralement dans des processus différents même s’ils se trouvent dans le même package.

Vous devez toujours instancier les objets [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)et [**SHAREDPROPERTY**](sharedproperty.md) à partir de composants com+ plutôt qu’à partir d’un client de base. Si un client de base crée des groupes de propriétés et des propriétés partagés, les propriétés partagées se trouvent à l’intérieur du processus client de base, et non dans un processus serveur. Cela signifie que les objets COM+ ne peuvent pas partager les propriétés, à moins que les objets ne s’exécutent également dans le processus client (ce qui n’est généralement pas une bonne idée).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de propriétés partagé COM+](com--shared-property-manager.md)
</dt> <dt>

[Groupes de propriétés partagées](shared-property-groups.md)
</dt> </dl>

 

 



