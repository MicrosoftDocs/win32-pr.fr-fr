---
description: Le tableau ODBCDriver répertorie les pilotes ODBC appartenant à l’installation.
ms.assetid: 3518b370-0652-4b54-8057-9871365d5e8c
title: Table ODBCDriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eb0da3217d7466fc0beef90933c8a6af32e3d0551ecc6975a31ac55ed2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943120"
---
# <a name="odbcdriver-table"></a>Table ODBCDriver

Le tableau ODBCDriver répertorie les pilotes ODBC appartenant à l’installation.

La table ODBCDriver contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Pilote      | [Identificateur](identifier.md) | O   | N        |
| Composant\_ | [Identificateur](identifier.md) | N   | N        |
| Description | [Text](text.md)             | N   | N        |
| fichier\_      | [Identificateur](identifier.md) | N   | N        |
| Configuration des fichiers \_ | [Identificateur](identifier.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>Pilote
</dt> <dd>

Nom du jeton interne pour le pilote. Une clé primaire pour la table

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la table des composants.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description inscrite pour ce pilote ODBC. Cette valeur ne peut pas être localisée.

</dd> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_
</dt> <dd>

Fichier DLL pour les pilotes figurant dans la colonne Driver. La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md). Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short. La \| syntaxe SFN LFN ne peut pas être utilisée.

</dd> <dt>

<span id="File_Setup"></span><span id="file_setup"></span><span id="FILE_SETUP"></span>Configuration des fichiers \_
</dt> <dd>

Fichier DLL d’installation du pilote, s’il est différent de celui du pilote. La colonne de fichier \_ est une clé externe dans la [table de fichiers](file-table.md). Le nom de fichier entré dans la colonne de nom de fichier de cet enregistrement de table de fichiers doit être au format de nom de fichier Short. La \| syntaxe SFN LFN ne peut pas être utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



