---
description: Lorsqu’il est installé sur un serveur d’applications, COM+ crée automatiquement une partition, appelée partition globale.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implémentation de la partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916799"
---
# <a name="partition-implementation"></a>Implémentation de la partition

Lorsqu’il est installé sur un serveur d’applications, COM+ crée automatiquement une partition, appelée *partition globale*. La partition globale comprend un ensemble standard d’applications COM+. Les applications COM+ qui sont installées dans la partition globale sont automatiquement disponibles pour tous les utilisateurs sur le serveur. Si vous avez d’autres applications COM+ que vous souhaitez mettre à la disposition de tous les utilisateurs sur le serveur, vous pouvez les ajouter à la partition globale.

En plus de la partition globale, vous pouvez créer d’autres partitions pour les utilisateurs sur ce serveur uniquement ou pour les utilisateurs dans le domaine. La création de partitions supplémentaires et l’installation simultanée de plusieurs configurations d’une application COM+ permettent à vos utilisateurs d’exécuter ces configurations d’application simultanément sur le même ordinateur. En outre, en installant des applications COM+ dans une partition autre que la partition globale, vous pouvez contrôler l’accès des utilisateurs à ces applications.

**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible. La partition globale est la seule partition COM+ disponible.

Pour plus d’informations sur les partitions locales et les partitions définies dans Active Directory, consultez les rubriques suivantes :

-   [Partitions locales](local-partitions.md)
-   [Partitions et Active Directory](partitions-and-active-directory.md)
-   [Partitions par défaut](default-partitions.md)
-   [Partition globale](the-global-partition.md)
-   [Propriétés de partition](partition-properties.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions relatives à la conception d’applications](application-design-restrictions.md)
</dt> <dt>

[Composants et partitions COM+ en file d’attente](com--queued-components-and-partitions.md)
</dt> <dt>

[Inscription et activation de composants dans des partitions](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Que sont les partitions COM+ ?](what-are-com--partitions-.md)
</dt> </dl>

 

 



