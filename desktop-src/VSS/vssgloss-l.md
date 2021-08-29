---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ef027528155e3a1d72b1a8e9190fd2e2f8ebb71046dd942df37bf0467e0a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997949"
---
# <a name="l-volume-shadow-copy-service"></a>L (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**chemin logique**
</dt> <dd>

Mécanisme permettant de décrire les composants d’un enregistreur. Il est utilisé pour exprimer des relations entre les composants, en particulier leur hiérarchie. Par exemple, si un writer gérait plusieurs livres électroniques, il peut affecter des chemins logiques « \\ ebook \\ Classeur1 » et « \\ ebook \\ book2 » aux composants de groupe de fichiers contenant chaque livre. Les chemins d’accès logiques sont requis lors de la spécification des sous-composants.

Par Convention, la barre oblique inverse « \\ » est utilisée pour séparer les éléments d’un chemin d’accès logique. En outre, il n’existe aucune restriction sur les caractères qui peuvent apparaître dans un chemin logique non **null** .

Un chemin d’accès logique peut être **null**. Par Convention, les composants avec des chemins logiques **null** sont considérés comme étant au niveau supérieur de la hiérarchie des chemins d’accès logiques d’un writer.

Voir aussi [*composant*](vssgloss-c.md), sous- [*composant*](vssgloss-s.md).

</dd> </dl>

 

 



