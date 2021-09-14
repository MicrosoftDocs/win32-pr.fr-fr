---
description: Une famille d’images est un groupe d’une ou de plusieurs images mises à niveau d’un produit qui ont été mises à jour vers la version la plus récente.
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: Table ImageFamilies (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021399"
---
# <a name="imagefamilies-table-patchwizdll"></a>Table ImageFamilies (Patchwiz.dll)

Une famille d’images est un groupe d’une ou de plusieurs images mises à niveau d’un produit qui ont été mises à jour vers la version la plus récente. Chaque image mise à niveau ne peut appartenir qu’à une seule famille. Les images mises à niveau appartenant à une famille d’images partagent un ou plusieurs fichiers. Chaque famille d’images a son propre fichier cab dans le fichier. msp contenant les correctifs binaires et les nouveaux fichiers nécessaires pour mettre à jour les différences entre les fichiers cibles et les fichiers mis à niveau. Le fichier CAB ne réplique pas les correctifs binaires et les nouveaux fichiers utilisés par les fichiers partagés.

Une table ImageFamilies contenant au moins un enregistrement est requise dans chaque base de données de création de correctif (fichier. PCP). Cette table est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La table ImageFamilies contient les informations de mise à jour corrective qui doivent être ajoutées à la [table multimédia](media-table.md). Un correctif ajoute une entrée à la table des médias. Chaque enregistrement dans les tables ImageFamilies fait référence à un groupe d’images de produits associées qui ont été mises à jour vers la version la plus récente du produit.

La table ImageFamilies contient les colonnes suivantes. une valeur null peut être utilisée dans les colonnes MediaSrcPropName, MediaDiskId et FileSequenceStart si le correctif est appliqué avec Windows Installer et Patchwiz.dll version 2,0.



| Colonne            | Type    | Clé | Nullable |
|-------------------|---------|-----|----------|
| Famille            | text    | O   | N        |
| MediaSrcPropName  | text    |     | O        |
| MediaDiskId       | entier |     | O        |
| FileSequenceStart | entier |     | O        |
| DiskPrompt        | text    |     | O        |
| VolumeLabel       | text    |     | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famille
</dt> <dd>

La valeur entrée dans ce champ est un identificateur pour un groupe d’images de produits associées qui ont été mises à jour vers la version la plus récente du produit. Limité à un total de 8 caractères alphanumériques ou traits de soulignement. le programme d’installation incorpore un flux de fichier cab dans le Windows Installer fichier correctif (fichier. msp) de chaque famille dans la table. Le fichier cab contient les correctifs binaires et les nouveaux fichiers nécessaires à la mise à jour d’une image cible dans une image mise à niveau du produit. Le programme d’installation préfixe le nom de famille avec PCW \_ CAB \_ pour générer le nom de flux de l’armoire qu’il entre dans le champ Cabinet de la nouvelle entrée de [table de médias](media-table.md) .

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName
</dt> <dd>

Valeur entrée dans le champ source de la nouvelle entrée de la [table multimédia](media-table.md) de l’image mise à niveau. Ce champ peut avoir la valeur NULL uniquement si vous utilisez la version 2,0 de Patchwiz.dll et si le MinimumRequiredMsiVersion dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md) a la valeur 200.

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId
</dt> <dd>

Le programme d’installation entre cette valeur dans le champ depatinage du nouvel enregistrement de la [table de médias](media-table.md) . La valeur de l’irdérapante doit être supérieure à n’importe quel didérapageur actuel dans le package cible. La limite de MediaDiskId est 32767. Ce champ peut avoir la valeur NULL uniquement si vous utilisez la version 2,0 de Patchwiz.dll et si le MinimumRequiredMsiVersion dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md) a la valeur 200.

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart
</dt> <dd>

Ce champ est le numéro de séquence du fichier de départ. Ce même numéro de séquence de fichier ne doit pas exister dans deux correctifs pour le même produit. Pour ce faire, la valeur de ce champ doit être supérieure à tous les numéros de séquence utilisés dans les correctifs précédents ou dans le package d’installation d’origine. Le numéro de séquence le plus élevé d’un correctif peut être déterminé en ajoutant le nombre total d’entrées dans le fichier CAB du correctif au numéro FileSequenceStart pour ce correctif. Une façon de déterminer cela consiste à examiner le fichier. ddf généré par [Patchwiz.dll](patchwiz-dll.md) lors de la création du correctif. La limite de FileSequenceStart est 32767. Ce champ peut avoir la valeur NULL uniquement si vous utilisez la version 2,0 de Patchwiz.dll et si le MinimumRequiredMsiVersion dans la [table de propriétés (Patchwiz.dll)](properties-table-patchwiz-dll-.md) a la valeur 200.

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Le programme d’installation entre cette valeur dans le champ DiskPrompt du nouvel enregistrement de la [table de médias](media-table.md) .

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Le programme d’installation entre cette valeur dans le champ VolumeLabel du nouvel enregistrement multimédia.

</dd> </dl>

## <a name="remarks"></a>Notes

Le correctif ajoute le nom de l’armoire dans le fichier. msp au champ Cabinet du nouvel enregistrement ajouté à la [table multimédia](media-table.md). Étant donné qu’il s’agit d’un fichier CAB incorporé, le nom est préfixé avec un \# caractère «». Le correctif ajoute une propriété au champ source du nouvel enregistrement dans la table multimédia. Deux correctifs ne peuvent pas avoir la même propriété source.

Les fichiers qui sont partagés dans la famille d’images doivent avoir la même clé de table de fichiers dans chaque image mise à niveau de la famille. Toutes les clés de table de fichiers partagées entre les images mises à niveau doivent représenter le même fichier et doivent être identiques dans toutes les images mises à niveau. La clé de table de fichier est la valeur entrée dans la colonne fichier de la [table de fichiers](file-table.md).

La limite pour MediaDiskId et FileSequenceStart est 32767. Pour augmenter cette limite, exportez la table ImageFamilies vers un fichier. IDT avec [Msidb.exe](msidb-exe.md) et remplacez le type de colonne I2 par i4, ou de I2 par i4, puis importez à nouveau le fichier. IDT dans la base de données. PCP. Les transformations et les correctifs ne peuvent pas être créés entre deux packages ayant des types de colonnes différents.

 

 



