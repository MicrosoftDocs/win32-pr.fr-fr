---
description: La table file contient la liste complète des fichiers sources avec leurs différents attributs, classés par un identificateur unique et non localisé.
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: Table de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021747"
---
# <a name="file-table"></a>Table de fichier

La table file contient la liste complète des fichiers sources avec leurs différents attributs, classés par un identificateur unique et non localisé. Les fichiers peuvent être stockés sur le support source en tant que fichiers individuels ou compressés dans un [*fichier CAB*](c-gly.md). Pour plus d’informations, consultez [utilisation d’armoires et de sources compressées](using-cabinets-and-compressed-sources.md).

La table de fichiers contient les colonnes suivantes.



| Colonne      | Type                               | Clé | Nullable |
|-------------|------------------------------------|-----|----------|
| Fichier        | [Identificateur](identifier.md)       | O   | N        |
| Composant\_ | [Identificateur](identifier.md)       | N   | N        |
| FileName    | [Nom du fichier](filename.md)           | N   | N        |
| FileSize    | [DoubleInteger](doubleinteger.md) | N   | N        |
| Version     | [Version](version.md)             | N   | O        |
| Langage    | [Langage](language.md)           | N   | O        |
| Attributs  | [Integer](integer.md)             | N   | O        |
| Séquence    | [Integer](integer.md)             | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>Txt
</dt> <dd>

Jeton non localisé qui identifie de façon unique le fichier. Ce champ n’est pas sensible à la casse. N’assignez pas d’identificateurs à des fichiers différents qui diffèrent uniquement par leur casse.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md). Ce champ identifie le composant qui contrôle le fichier.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Nom de fichier utilisé pour l’installation. Le nom peut être localisé.

Étant donné que certains serveurs Web peuvent respecter la casse, le nom de fichier doit correspondre exactement à la casse des fichiers sources pour garantir la prise en charge des téléchargements Internet.

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>Taille
</dt> <dd>

Taille du fichier en octets. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Ce champ correspond à la chaîne de version d’un fichier avec version. Ce champ est vide pour les fichiers sans version. La version de fichier entrée dans ce champ doit être identique à la version du fichier inclus dans le package d’installation.

Le champ version peut également être défini pour contenir la clé primaire d’un autre enregistrement dans la table de fichiers. Le fichier référencé détermine ensuite la logique de contrôle de version pour ce fichier. Pour plus d’informations, consultez [fichiers d’accompagnement](companion-files.md). Notez que si ce fichier est le chemin d’accès de clé de son composant, il ne doit pas être spécifié en tant que fichier compagnon.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous
</dt> <dd>

Liste d’ID de langue décimaux séparés par des virgules.

Les fichiers de polices ne doivent pas être créés avec un ID de langue, car les polices n’ont pas de ressource d’ID de langue incorporée. Par conséquent, cette colonne doit être laissée null pour les fichiers de polices.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Entier qui contient des indicateurs binaires qui représentent des attributs de fichier.

Le tableau suivant montre la définition du champ de bits.



| Constante                             | Valeur hexadécimale | Decimal | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | Lecture seule                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Hidden                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesSystem**        | 0x000004    | 4       | Système                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | Le fichier est essentiel pour le fonctionnement précis du composant auquel il appartient. Si l’installation d’un fichier avec l’attribut msidbFileAttributesVital échoue, l’installation s’arrête et est annulée. Dans ce cas, le programme d’installation affiche une boîte de dialogue sans bouton ignorer. Si cet attribut n’est pas défini et que l’installation du fichier échoue, le programme d’installation affiche une boîte de dialogue avec un bouton ignorer. Dans ce cas, l’utilisateur peut choisir d’ignorer l’échec d’installation du fichier et de continuer. <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1 024    | Le fichier contient une [*somme de contrôle*](c-gly.md)valide. Une somme de contrôle est nécessaire pour réparer un fichier qui a été endommagé.                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | Ce bit doit être ajouté uniquement par un correctif et si le fichier est ajouté par le correctif.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8 192    | Le type de source du fichier n’est pas compressé. Si cette option est définie, ignore la propriété [**Résumé du nombre de mots**](word-count-summary.md) . Si ni **msidbFileAttributesNoncompressed** ni **msidbFileAttributesCompressed** n’est défini, l’état de compression du fichier est spécifié par la propriété **Résumé du nombre de mots** . Ne définissez pas à la fois **msidbFileAttributesNoncompressed** et **msidbFileAttributesCompressed**.                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | Le type de source du fichier est compressé. Si cette option est définie, ignore la propriété [**Résumé du nombre de mots**](word-count-summary.md) . Si ni **msidbFileAttributesNoncompressed** ni **msidbFileAttributesCompressed** n’est défini, l’état de compression du fichier est spécifié par la propriété **Résumé du nombre de mots** . Ne définissez pas à la fois **msidbFileAttributesNoncompressed** et **msidbFileAttributesCompressed**.                                                                                                                              |



 

Si le bit **msidbFileAttributesVital** dans la colonne attributs est défini, et si le composant auquel appartient le fichier est sélectionné pour l’installation, le programme d’installation doit être en mesure d’installer ce fichier pour que l’installation soit effectuée correctement. Si le programme d’installation ne parvient pas à installer le fichier pour une raison quelconque (par exemple, si le fichier source est introuvable dans l’image source), une boîte de dialogue d’erreur s’affiche avec les options « réessayer » ou « annuler ». Dans le cas d’un fichier pour lequel **msidbFileAttributesVital** n’est pas défini, les options en cas d’erreur d’installation sont « abandonner », « Réessayer » et « ignorer » (autrement dit, l’utilisateur a la possibilité d’effectuer correctement l’installation sans installer ce fichier).

Le bit **msidbFileAttributesChecksum** dans la colonne attributs doit être défini pour chaque fichier exécutable de l’installation dont la [*somme de contrôle*](c-gly.md) valide est stockée dans l’en-tête de fichier exécutable portable (PE). Seuls les fichiers qui ont cet ensemble de bits sont vérifiés pour une somme de contrôle valide pendant une réinstallation. Pour plus d’informations, consultez [**REINSTALLMODE**](reinstallmode.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence
</dt> <dd>

Position de séquence de ce fichier sur les images de média. Cet ordre doit correspondre à l’ordre des fichiers dans le fichier cab si les fichiers sont compressés. Les entiers dans ce champ doivent être égaux ou supérieurs à 1.

Les numéros de séquence de la colonne séquence sont utilisés pour spécifier l’ordre d’installation des fichiers et le support source sur lequel le fichier se trouve (conjointement avec la [table des médias](media-table.md)). Supposons, par exemple, qu’un fichier a un numéro de séquence de 92. Pour déterminer le disque source sur lequel réside ce fichier, recherchez dans la table des supports l’entrée dont la dernière valeur de séquence est supérieure à 92.

Bien que les numéros de séquence internes soient affectés aux fichiers compressés dans les armoires, ces derniers ne doivent pas nécessairement correspondre aux numéros de séquence de la table de fichiers. Toutefois, il est important que la séquence de fichiers de la table de fichiers soit identique à celle des fichiers dans les armoires.

Pour les fichiers qui ne sont pas compressés, les numéros de séquence n’ont pas besoin d’être uniques. Par exemple, si tous vos fichiers sont décompressés et que tous les fichiers résident sur un disque, vous pouvez attribuer à tous les fichiers le même numéro de séquence.

La limite maximale est de 32767 fichiers. pour créer un package Windows Installer avec d’autres fichiers, consultez [création d’un package volumineux](authoring-a-large-package.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Les actions [InstallFiles](installfiles-action.md) et [RemoveFiles](removefiles-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations de cette table. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

La table est initialement générée à partir de la liste de fichiers, mais si la compression cab est utilisée, la table est régénérée à partir de la sortie du moteur de compression. Pour plus d’informations, consultez [fichiers CAB](cabinet-files.md).

Pour déplacer un fichier existant sur l’ordinateur de l’utilisateur pendant l’installation, utilisez l' [action MoveFiles](movefiles-action.md) et la [table MoveFile](movefile-table.md). Pour installer un fichier dans plusieurs emplacements, utilisez l' [action DuplicateFiles](duplicatefiles-action.md) et la [table DuplicateFile](duplicatefile-table.md).

Le tableau suivant récapitule les combinaisons possibles de valeurs dans la colonne version et la colonne Language. Pour plus d’informations, consultez règles de contrôle de [version de fichier](file-versioning-rules.md).



| Version | Langage | Description                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 1033     | Version et langue.                                                       |
| 1.2.3.4 | Nul   | La version, mais pas de langue.                                                    |
| 1.2.3.4 | 0        | La version et la langue sont neutres.                                           |
| TestDB  | Nul   | Fichier compagnon sans langage associé.                         |
| TestDB  | 1033     | Le fichier et la langue de l’Assistant.                                                |
| Nul  | 1033     | Aucune version, mais un langage lui est associé (c’est-à-dire TypeLib, HelpFile). |



 

Pour plus d’informations, consultez la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) et la [table LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE39](ice39.md)  
[ICE42](ice42.md)  
[ICE45](ice45.md)  
[ICE50](ice50.md)  
[ICE51](ice51.md)  
[ICE54](ice54.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE60](ice60.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE76](ice76.md)  
[ICE91](ice91.md)  
</dl>

 

 




