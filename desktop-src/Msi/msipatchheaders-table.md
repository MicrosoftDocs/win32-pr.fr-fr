---
description: La table MsiPatchHeaders contient les flux d’en-tête de correctifs binaires utilisés pour la validation des correctifs.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Table MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119745"
---
# <a name="msipatchheaders-table"></a>Table MsiPatchHeaders

La table MsiPatchHeaders contient les flux d’en-tête de correctifs binaires utilisés pour la validation des correctifs.

La table MsiPatchHeaders est utilisée lorsque les clés de [table de fichiers](file-table.md) longs entraînent l’échec de la génération du flux d’en-tête de correctif dans la [table des correctifs](patch-table.md). Cela peut être dû à la limitation du nom de flux décrite dans [restrictions OLE sur flux](ole-limitations-on-streams.md). Dans ce cas, la table de correctifs peut faire référence à la table MsiPatchHeaders pour créer le flux d’en-tête de correctif.

La table MsiPatchHeaders contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificateur](identifier.md) | O   | N        |
| En-tête    | [Binaire](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

Clé primaire de la table qui identifie de façon unique un en-tête de correctif spécifique.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Titre
</dt> <dd>

Cette colonne est l’en-tête de correctif de flux binaire utilisé pour la validation des correctifs.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est traitée par l' [action PatchFiles](patchfiles-action.md). Cette table est généralement ajoutée au package d’installation par une transformation à partir d’un package correctif. En général, il n’est pas directement créé dans un package d’installation.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



