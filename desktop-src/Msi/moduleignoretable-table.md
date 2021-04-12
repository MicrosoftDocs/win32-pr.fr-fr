---
description: Si une table du module de fusion est listée dans le tableau ModuleIgnoreTable, elle n’est pas fusionnée dans le fichier. msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Table ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210252"
---
# <a name="moduleignoretable-table"></a>Table ModuleIgnoreTable

Si une table du module de fusion est listée dans le tableau ModuleIgnoreTable, elle n’est pas fusionnée dans le fichier. msi. Si la table existe déjà dans le fichier. msi, elle n’est pas modifiée par la fusion. Les tables dans ModuleIgnoreTable peuvent donc contenir des données qui ne sont pas nécessaires après la fusion.

La table ModuleIgnoreTable contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| Table de charge de travail  | [Identificateur](identifier.md) | O   | Non       |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Nom de la table dans le module de fusion qui ne doit pas être fusionnée dans le fichier. msi.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour réduire la taille du fichier. msm, il est recommandé aux développeurs de supprimer les tables inutilisées des modules destinés à la redistribution plutôt que de répertorier ces tables dans la table ModuleIgnoreTable.

 

 



