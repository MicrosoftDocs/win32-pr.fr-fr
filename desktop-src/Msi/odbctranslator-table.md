---
description: Le tableau ODBCTranslator répertorie les convertisseurs ODBC appartenant à l’installation.
ms.assetid: fecb7454-29bb-4ddf-b4d5-2e56c20ff2dc
title: Table ODBCTranslator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fdf85f73b649e18c0980508e234bf7599e69c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218969"
---
# <a name="odbctranslator-table"></a>Table ODBCTranslator

Le tableau ODBCTranslator répertorie les convertisseurs ODBC appartenant à l’installation.

La table ODBCTranslator contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Traducteur  | [Identificateur](identifier.md) | O   | N        |
| Composant\_ | [Identificateur](identifier.md) | N   | N        |
| Description | [Text](text.md)             | N   | N        |
| fichier\_      | [Identificateur](identifier.md) | N   | N        |
| Configuration des fichiers \_ | [Identificateur](identifier.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Translator"></span><span id="translator"></span><span id="TRANSLATOR"></span>Traducteur
</dt> <dd>

Nom de jeton interne pour le traducteur. Clé primaire pour la table.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la table des composants.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description enregistrée pour ce convertisseur de pilote ODBC. Cette valeur ne peut pas être localisée.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

fichier DLL du transfert figurant dans la colonne Traducteur. La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md). Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short. La \| syntaxe SFN LFN ne peut pas être utilisée.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuration des fichiers \_
</dt> <dd>

fichier DLL d’installation pour le convertisseur, s’il est différent de la colonne Traducteur. La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md). Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short. La \| syntaxe SFN LFN ne peut pas être utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



