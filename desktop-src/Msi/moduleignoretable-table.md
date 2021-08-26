---
description: Si une table du module de fusion est listée dans la table ModuleIgnoreTable, elle n’est pas fusionnée dans le fichier .msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Table ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46337b74f6822b374314a9248f0377ec63359c6576a6ca1398a931d27e548138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042857"
---
# <a name="moduleignoretable-table"></a>Table ModuleIgnoreTable

Si une table du module de fusion est listée dans la table ModuleIgnoreTable, elle n’est pas fusionnée dans le fichier .msi. Si la table existe déjà dans le fichier .msi, elle n’est pas modifiée par la fusion. Les tables dans ModuleIgnoreTable peuvent donc contenir des données qui ne sont pas nécessaires après la fusion.

La table ModuleIgnoreTable contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| Table de charge de travail  | [Identificateur](identifier.md) | O   | Non       |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Nom de la table dans le module de fusion qui ne doit pas être fusionnée dans le fichier .msi.

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour réduire la taille du fichier. msm, il est recommandé aux développeurs de supprimer les tables inutilisées des modules destinés à la redistribution plutôt que de répertorier ces tables dans la table ModuleIgnoreTable.

 

 



