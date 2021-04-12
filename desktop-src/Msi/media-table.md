---
description: La table des médias décrit l’ensemble des disques qui composent le média source pour l’installation.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Table des médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321478"
---
# <a name="media-table"></a>Table des médias

La table des médias décrit l’ensemble des disques qui composent le média source pour l’installation.

La table des médias contient les colonnes indiquées dans le tableau suivant.



| Colonne       | Type                     | Clé | Nullable |
|--------------|--------------------------|-----|----------|
| DiskId       | [Integer](integer.md)   | O   | N        |
| LastSequence | [Integer](integer.md)   | N   | N        |
| DiskPrompt   | [Text](text.md)         | N   | O        |
| CAB      | [CAB](cabinet.md)   | N   | O        |
| VolumeLabel  | [Text](text.md)         | N   | O        |
| Source       | [Propriété](property.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Détermine l’ordre de tri de la table. Ce nombre doit être supérieur ou égal à 1.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Numéro de séquence du fichier pour le dernier fichier de ce média. Les nombres dans la colonne LastSequence spécifient les fichiers de la table de [fichiers](file-table.md) qui se trouvent sur un disque source particulier. Chaque disque source contient tous les fichiers avec des numéros de séquence (comme indiqué dans la colonne séquence de la table file) inférieurs ou égaux à la valeur de la colonne LastSequence et supérieur à la valeur LastSequence du disque précédent (ou supérieur à 0, pour la première entrée de la table Media). Ce nombre ne doit pas être négatif. la limite maximale est de 32767 fichiers. Pour plus d’informations sur la création d’un package Windows Installer avec d’autres fichiers, consultez [création d’un package volumineux](authoring-a-large-package.md).

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Le nom du disque, qui est généralement le texte visible imprimé sur le disque. Ce texte localisable est utilisé pour inviter l’utilisateur lorsque ce disque doit être inséré.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>CAB
</dt> <dd>

Nom de l’armoire si certains ou l’ensemble des fichiers stockés sur le support sont compressés dans un fichier CAB. Si aucune armoire n’est utilisée, cette colonne doit être vide. Le nom du fichier cab doit utiliser la syntaxe du type de données [Cabinet](cabinet.md) . Windows Installer requiert toujours une source valide pour réparer les fichiers inclus dans les fichiers CAB incorporés. Lorsque Windows Installer installe un package contenant un fichier CAB incorporé, une copie du fichier CAB peut être enregistrée par le système. Cette copie ne peut pas être utilisée pour réparer le fichier CAB. Pour économiser de l’espace disque, utilisez des fichiers CAB externes plutôt que des fichiers CAB incorporés.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Étiquette attribuée au volume. Il s’agit de l’étiquette de volume retournée par la fonction [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) . Si la propriété [**SourceDir**](sourcedir.md) fait référence à un volume amovible (disquette ou CD-ROM), ce nom de volume est utilisé pour vérifier que le disque approprié se trouve dans le lecteur avant de tenter d’installer des fichiers. L’entrée dans cette colonne doit correspondre à l’étiquette de volume du support physique.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Code
</dt> <dd>

Ce champ est utilisé uniquement par la mise à jour corrective et n’est pas vide. Une transformation de correctif peut entrer ici une propriété qui correspond à l’emplacement du fichier cab contenant les fichiers correctifs ou les nouveaux fichiers ajoutés par le correctif. Vous devez spécifier une source différente pour ces fichiers, car la source du package de correctifs peut être stockée séparément de la source du produit. Si le champ Cabinet est vide, le programme d’installation ignore la valeur de cette colonne. Si ce champ est vide, le programme d’installation utilise la valeur de la propriété [**SourceDir**](sourcedir.md) comme source du fichier CAB.

</dd> </dl>

## <a name="remarks"></a>Notes

Si le nom du fichier cab est précédé d’un signe dièse ( \# ), les fichiers qui font référence à cet enregistrement de table de média sont empaquetés dans un fichier CAB stocké dans la base de données sous la forme d’un flux distinct.

Pour plus d’informations sur l’ajout d’armoires aux tables de fichiers et aux tables multimédias, consultez [utilisation des armoires et des sources compressées](using-cabinets-and-compressed-sources.md).

Windows Installer nécessite que le fichier. msi se trouve sur le premier disque d’un support amovible (CD, DVD ou disquette) utilisé pour l’installation du produit.

**Détermination de la SourceMode**

La propriété [**Résumé du nombre de mots**](word-count-summary.md) détermine le mode source pour l’installation actuelle. Si cette propriété a la valeur 2 ou 3, l’installation d’un fichier cab est supposée. Dans ce mode, les fichiers CAB sont supposés exister dans le répertoire indiqué par la propriété [**SourceDir**](sourcedir.md) . Si la valeur du type de source est 0 ou 1, tous les fichiers sources sont supposés exister dans l’arborescence dont la racine est indiquée par la propriété **SourceDir** .

Notez que cela s’applique uniquement aux fichiers de la table de fichiers qui n’ont pas les bits compressés ou non compressés définis dans la colonne attributs. Ces bits remplacent la valeur de la propriété [**Résumé du nombre de mots**](word-count-summary.md) lorsque vous déterminez si un fichier particulier est compressé ou non.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 
