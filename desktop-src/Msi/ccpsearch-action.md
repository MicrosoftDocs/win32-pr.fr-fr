---
description: L’action CCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Action CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092309"
---
# <a name="ccpsearch-action"></a>Action CCPSearch

L’action CCPSearch utilise des signatures de fichiers pour vérifier que les produits éligibles sont installés sur un système avant l’exécution d’une mise à niveau.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action CCPSearch doit être créée dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md). Le programme d’installation empêche l’action CCPSearch de s’exécuter dans la séquence InstallExecuteSequence si l’action a déjà été exécutée dans la séquence InstallUISequence. L’action CCPSearch doit précéder l’action [RMCCPSearch](rmccpsearch-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action CCPSearch recherche des signatures de fichiers listées dans la table CCPSearch sur le système en utilisant les tables suivantes dans l’ordre : signature, CompLocator, RegLocator, IniLocator et DrLocator.

Si une signature est identifiée comme existante, la propriété **CCP \_ Success** a la valeur 1 et l’action CCPSearch se termine.

L’absence de signature à partir de la table de signature désigne un répertoire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CCPSearch](ccpsearch-table.md)
</dt> <dt>

[Signature](signature-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



