---
description: la table MsiFileHash est utilisée pour stocker un hachage 128 bits d’un fichier source fourni par le package Windows Installer. Le hachage est divisé en valeurs 4 32 bits et stocké dans des colonnes distinctes de la table.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Table MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc43c7fd812781057ec0be271ffc370a6b5eb2e3054926e1f969383c0fb390c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944946"
---
# <a name="msifilehash-table"></a>Table MsiFileHash

la table **MsiFileHash** est utilisée pour stocker un hachage 128 bits d’un fichier source fourni par le package Windows Installer. Le hachage est divisé en valeurs 4 32 bits et stocké dans des colonnes distinctes de la table.

Windows Le programme d’installation peut utiliser le hachage de fichiers comme un moyen de détecter et d’éliminer les copies de fichiers inutiles. Un hachage de fichier stocké dans la table **MsiFileHash** peut être comparé à un hachage d’un fichier existant sur l’ordinateur de l’utilisateur obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). La table **MsiFileHash** peut uniquement être utilisée avec des fichiers sans version.

La table **MsiFileHash** contient les colonnes suivantes.



| Colonne    | Type                               | Clé | Nullable |
|-----------|------------------------------------|-----|----------|
| fichier\_    | [Identificateur](identifier.md)       | O   | N        |
| Options   | [Integer](integer.md)             | N   | N        |
| HashPart1 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart2 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart3 | [DoubleInteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Clé étrangère vers [table de fichiers](file-table.md). chaîne de caractères 72.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options
</dt> <dd>

Cette colonne doit avoir la valeur 0 et être réservée à une utilisation ultérieure.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Premier 32 bits de hachage. Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md). N’utilisez pas d’autres méthodes.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Deuxième 32 bits de hachage. Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md). N’utilisez pas d’autres méthodes de hachage.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Troisième 32 bits de hachage. Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md). N’utilisez pas d’autres méthodes.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Quatrième 32 bits de hachage. Le hachage de fichier entré dans ce champ doit être obtenu en appelant [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) ou la [**méthode FileHash**](installer-filehash.md). N’utilisez pas d’autres méthodes.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Contrôle de version de fichier par défaut](default-file-versioning.md)
</dt> </dl>

 

 



