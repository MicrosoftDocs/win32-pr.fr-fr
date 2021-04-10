---
description: Le tableau PatchPackage décrit tous les packages de correctifs qui ont été appliqués à ce produit. Pour chaque package de correctifs, l’identificateur unique du correctif est fourni, ainsi que des informations sur l’image de support sur laquelle le correctif est situé.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Table PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210770"
---
# <a name="patchpackage-table"></a>Table PatchPackage

Le tableau PatchPackage décrit tous les packages de correctifs qui ont été appliqués à ce produit. Pour chaque package de correctifs, l’identificateur unique du correctif est fourni, ainsi que des informations sur l’image de support sur laquelle le correctif est situé.

La table PatchPackage contient les colonnes suivantes.



| Colonne  | Type                   | Clé | Nullable |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | O   | N        |
| Multimédia\_ | [Integer](integer.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

Cette colonne contient un identificateur unique pour ce correctif.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_
</dt> <dd>

Cette colonne est une clé étrangère de la colonne depatinages de la [table Media](media-table.md) et indique le disque contenant le package de correctifs.

</dd> </dl>

## <a name="remarks"></a>Notes

La table PatchPackage est requise dans chaque package correctif. Si la table est manquante, les tentatives d’installation du correctif échouent avec « erreur 2768 : la transformation dans le package correctif n’est pas valide. » Cette table est généralement ajoutée au package d’installation par une transformation à partir d’un package correctif. En général, il n’est pas directement créé dans un package d’installation.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



