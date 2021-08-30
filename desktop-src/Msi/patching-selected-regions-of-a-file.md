---
description: Lors de la mise à jour corrective des fichiers ayant un contenu variable, il peut être nécessaire de conserver les régions sélectionnées du fichier cible pour éviter la perte d’informations critiques.
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: Mise à jour corrective des régions sélectionnées d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c075a3632dd6cf4d39a98467503c584cbf34a15311f37d0c8aabe0990bc74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926231"
---
# <a name="patching-selected-regions-of-a-file"></a>Mise à jour corrective des régions sélectionnées d’un fichier

Lors de la mise à jour corrective des fichiers ayant un contenu variable, il peut être nécessaire de conserver les régions sélectionnées du fichier cible pour éviter la perte d’informations critiques. Par exemple, certaines applications marquent les informations utilisateur dans le fichier exécutable. Étant donné que le contenu du fichier cible peut dépendre de l’ordinateur sur lequel l’application est installée, il devient difficile de déterminer si un fichier particulier est une cible valide pour le correctif. Les informations utilisateur écrites dans le fichier cible peuvent également être remplacées par un correctif.

Quand vous générez un fichier de propriétés de création de correctifs (PCP) avec [Msimsp.exe](msimsp-exe.md) et [PATCHWIZ.DLL](patchwiz-dll.md), vous pouvez spécifier que les informations dans certaines régions du fichier cible soient ignorées lors de la mise à jour corrective. Vous pouvez également spécifier que les informations dans d’autres régions du fichier cible soient conservées et copiées dans un emplacement de décalage dans le fichier mis à jour. Vous spécifiez les régions du fichier cible à ignorer et les régions à conserver lors de la création des tables [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md), [ExternalFiles](externalfiles-table-patchwiz-dll-.md)et [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) .

Utilisez la colonne RetainOffsets de la table [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) et les colonnes RetainOffsets et RetainLengths de la table [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) pour copier une plage d’informations du fichier cible vers une plage de décalage dans le fichier mis à jour. Les informations de cette plage sont conservées. Spécifiez la longueur de la plage à l’aide des colonnes RetainLengths de la table FamilyFileRanges. La longueur de la plage conservée est identique dans les fichiers cible et mis à jour. Spécifiez le décalage de la plage dans le fichier cible à l’aide de la colonne RetainOffsets de la table TargetFiles OptionalData. Spécifiez le décalage de la plage dans le fichier mis à jour à l’aide de la colonne RetainOffsets de la table FamilyFileRanges. La plage du fichier cible conservé est donc la valeur de RetainOffsets dans la table TargetFiles OptionalData plus RetainLengths. Ces informations sont copiées dans le fichier de mise à jour dans la plage spécifiée par la valeur de RetainOffsets dans les tables FamilyFileRanges plus RetainLengths. Vous pouvez spécifier plusieurs plages, mais l’ordre des longueurs doit correspondre à l’ordre des décalages.

Utilisez la table [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) pour ignorer une plage du fichier cible. Les informations de cette plage du fichier cible peuvent toujours être remplacées par le correctif. Spécifiez le décalage de la plage dans la colonne IgnoreOffsets et sa longueur dans la colonne IgnoreLengths. Vous pouvez spécifier plusieurs plages, mais l’ordre des longueurs doit correspondre à l’ordre des décalages.

Les valeurs des colonnes lengths et offsets peuvent être décimales ou hexadécimales. [PATCHWIZ.DLL](patchwiz-dll.md) traite la valeur comme hexadécimale si elle est préfixée par « 0x ». Les colonnes sont des colonnes de type chaîne, donc PATCHWIZ.DLL convertit les valeurs en ULONGs. La colonne length spécifie la longueur en octets.

 

 



