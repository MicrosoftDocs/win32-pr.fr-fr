---
description: L’action AppSearch utilise des signatures de fichiers pour rechercher les versions existantes des produits.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Action AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092642"
---
# <a name="appsearch-action"></a>Action AppSearch

L’action AppSearch utilise des signatures de fichiers pour rechercher les versions existantes des produits. L’action AppSearch peut utiliser ces informations pour déterminer où les mises à niveau doivent être installées. L’action AppSearch peut également être utilisée pour affecter à une propriété la valeur existante d’une entrée de registre ou .ini fichier.

## <a name="sequence-restrictions"></a>Restrictions de séquence

AppSearch doit être créé dans la [table InstallUISequence](installuisequence-table.md) et la [table InstallExecuteSequence](installexecutesequence-table.md). Le programme d’installation empêche l’action AppSearch de s’exécuter dans la séquence InstallExecuteSequence si l’action a déjà été exécutée dans la séquence InstallUISequence.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action      |
|-------|---------------------------------|
| \[1\] | Propriété contenant l’emplacement du fichier. |
| \[2\] | Signature de fichier.                 |



 

## <a name="remarks"></a>Notes

L’action AppSearch requiert que la table de [signatures](signature-table.md) soit présente dans le package d’installation. Les signatures de fichiers sont répertoriées dans la table de signature. Une signature qui ne figure pas dans la table de signature désigne un répertoire et l’action définit la propriété sur le chemin d’accès au répertoire de cette signature.

L’action AppSearch recherche d’abord des signatures de fichier à l’aide de la table [CompLocator](complocator-table.md) , la table [RegLocator](reglocator-table.md) , puis la table [IniLocator](inilocator-table.md) et enfin la table [DrLocator](drlocator-table.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[AppSearch](appsearch-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 



