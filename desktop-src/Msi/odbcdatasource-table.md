---
description: Le tableau ODBCDataSource répertorie les sources de données appartenant à l’installation.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: Table ODBCDataSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519349"
---
# <a name="odbcdatasource-table"></a>Table ODBCDataSource

Le tableau ODBCDataSource répertorie les sources de données appartenant à l’installation.

La table ODBCDataSource contient les colonnes suivantes.



| Colonne            | Type                         | Clé | Nullable |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identificateur](identifier.md) | O   | N        |
| -\_       | [Identificateur](identifier.md) | N   | N        |
| Description       | [Text](text.md)             | N   | N        |
| DriverDescription | [Text](text.md)             | N   | N        |
| Inscription      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>Mustek
</dt> <dd>

Nom de jeton interne de la source de données. Clé primaire pour la table.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la [table des composants](component-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description inscrite pour cette source de données. Cette valeur ne peut pas être localisée. Les descriptions de source de données ODBC ne peuvent pas dépasser la \_ longueur maximale de \_ DSN SQL \_ .

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription
</dt> <dd>

Pilote associé qui peut être préexistant. Cette valeur ne peut pas être localisée.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Abonnement
</dt> <dd>

Ce champ spécifie le type d’inscription de la source de données.



| Constante                                      | Valeur hexadécimale | Decimal | Description                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbODBCDataSourceRegistrationPerMachine** | 0x000       | 0       | La source de données est inscrite par ordinateur. |
| **msidbODBCDataSourceRegistrationPerUser**    | 0x001       | 1       | La source de données est inscrite par utilisateur.    |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Les actions [InstallODBC](installodbc-action.md) et [RemoveODBC](removeodbc-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau. Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



