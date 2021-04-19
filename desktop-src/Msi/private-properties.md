---
description: Les propriétés privées sont utilisées en interne par le programme d’installation et leurs valeurs doivent être entrées dans la base de données par l’auteur du package d’installation ou définies par le programme d’installation lors de l’installation sur les valeurs déterminées par l’environnement d’exploitation.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propriétés privées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528250"
---
# <a name="private-properties"></a>Propriétés privées

Les propriétés privées sont utilisées en interne par le programme d’installation et leurs valeurs doivent être entrées dans la base de données par l’auteur du package d’installation ou définies par le programme d’installation lors de l’installation sur les valeurs déterminées par l’environnement d’exploitation. La seule façon dont un utilisateur peut interagir avec les propriétés privées consiste à utiliser des [événements de contrôle](control-events.md) dans l’interface utilisateur créée du package. Les noms de propriétés privées doivent inclure des lettres minuscules. Consultez [restrictions sur les noms de propriété](restrictions-on-property-names.md).

Les propriétés privées décrivent généralement l’environnement d’exploitation. Par exemple, si l’installation est exécutée sur une plate-forme Windows, le programme d’installation définit la propriété [**WindowsFolder**](windowsfolder.md) sur la valeur spécifiée dans la table de propriétés.

Les valeurs de propriété privées ne peuvent pas être substituées sur une ligne de commande. Pour effacer une propriété privée d’une installation, ne la laissez pas dans la [table des propriétés](property-table.md). Sur Windows XP et Windows 2000, vous ne pouvez pas définir une propriété privée dans la phase de l’interface utilisateur de l’installation, puis passer la valeur à la phase d’exécution.

Pour obtenir la liste de toutes les propriétés privées standard utilisées par le programme d’installation, consultez Référence de la [propriété](property-reference.md). Vous pouvez définir une propriété privée personnalisée en entrant le nom et la valeur initiale de la propriété dans la table de propriétés. Les noms de propriétés privées doivent toujours inclure des lettres minuscules.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propri&amp;#233;t&amp;#233;s publiques](public-properties.md)
</dt> </dl>

 

 



