---
description: Il s’agit d’une table temporaire en lecture seule utilisée pour afficher des transformations à l’aide du mode d’affichage transformer. Cette table n’est jamais conservée par le programme d’installation.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Table _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093006"
---
# <a name="_transformview-table"></a>\_Table TransformView

Il s’agit d’une table temporaire en lecture seule utilisée pour afficher des transformations à l’aide du mode d’affichage transformer. Cette table n’est jamais conservée par le programme d’installation.

Pour appeler le mode d’affichage transformation, obtenez un handle et ouvrez la base de données de référence. Consultez [obtention d’un descripteur de base de données](obtaining-a-database-handle.md). Appelez [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) avec l' \_ erreur MSITRANSFORM \_ VIEWTRANSFORM. Cela arrête l’application de la transformation à la base de données et vide le contenu de la transformation dans la \_ table TransformView. vous pouvez accéder aux données de la table à l’aide de SQL requêtes. Consultez [utilisation des requêtes](working-with-queries.md).

La \_ table TransformView n’est pas effacée lorsqu’une autre transformation est appliquée. Le tableau reflète l’effet cumulatif des applications successives. Pour afficher les transformations séparément, vous devez libérer la table.

La \_ table TransformView contient les colonnes suivantes.



| Colonne  | Type                         | Clé | Nullable |
|---------|------------------------------|-----|----------|
| Table de charge de travail   | [Identificateur](identifier.md) | O   | N        |
| Colonne  | [Text](text.md)             | O   | N        |
| Ligne     | [Text](text.md)             | O   | O        |
| Données    | [Text](text.md)             | N   | O        |
| Actuel | [Text](text.md)             | N   | O        |



 

## <a name="column"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Nom d’une table de base de données modifiée.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Chronique
</dt> <dd>

Nom d’une colonne de table modifiée ou d’une insertion, d’une suppression, d’une création ou d’une suppression.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Haut
</dt> <dd>

Liste des valeurs de clé primaire séparées par des tabulations. Les valeurs de clé primaire NULL sont représentées par un caractère d’espace unique. Une valeur null dans cette colonne indique une modification de schéma.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée
</dt> <dd>

Les données, le nom d’un flux de données ou une définition de colonne.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Actif
</dt> <dd>

Valeur actuelle de la base de données de référence ou numéro de colonne.

</dd> </dl>

## <a name="remarks"></a>Notes

le \_ TransformView est conservé en mémoire par un nombre de verrous, qui peut être libéré avec la commande SQL suivante.

« ALTER TABLE \_ TRANSFORMVIEW Free ».

vous pouvez accéder aux données de la table à l’aide de SQL requêtes. le langage de SQL a deux divisions principales : le langage de définition de données (DDL) utilisé pour définir tous les objets d’une base de données SQL, et le langage de Manipulation de données (DML) utilisé pour sélectionner, insérer, mettre à jour et supprimer des données dans les objets définis à l’aide de DDL.

Les opérations de transformation de langage de manipulation de données (DML) sont indiquées comme suit. le langage de Manipulation de données (DML) sont ces instructions dans SQL qui manipulent, au lieu de définir, des données.



| Opération de transformation | résultat SQL                                    |
|---------------------|-----------------------------------------------|
| Modifier des données         | Tableau chronique haut métadonnée {valeur actuelle} |
| Insérer une ligne          | Tableau « INSERT » {Row} NULL NULL              |
| Supprimer la ligne          | Tableau « DELETE » {Row} NULL NULL              |



 

Les opérations de transformation DDL (Data Definition Language) sont indiquées comme suit. le langage de définition de données (DDL) sont ces instructions dans SQL qui définissent, par opposition à manipuler, les données.



| Opération de transformation | résultat SQL                                   |
|---------------------|----------------------------------------------|
| Add column          | Tableau chronique NULL {defn} {numéro de colonne} |
| Ajoute une table           | Tableau « CREATE » NULL NULL NULL              |
| Supprimer une table          | Tableau "DROP" NULL NULL NULL                |



 

Lorsque l’application d’une transformation ajoute cette table, le champ de données reçoit du texte qui peut être interprété comme une valeur entière de 16 bits. La valeur décrit la colonne nommée dans le champ de colonne. Vous pouvez comparer la valeur entière aux constantes dans le tableau suivant pour déterminer la définition de la colonne modifiée.



| bit                                                                                                       | Description                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7<br/>         | Hexadécimal : 0x0000 0x0100<br/> Décimal : 0 255<br/> Largeur de colonne<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Hexadécimal : 0x0100<br/> Décimal : 256<br/> Colonne persistante. Zéro signifie une colonne temporaire. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Hexadécimal : 0x0200<br/> Décimal : 1023<br/> Colonne localisable. Zéro signifie que la colonne ne peut pas être localisée.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | Hexadécimal : 0x0000<br/> Décimal : 0<br/> Entier long<br/> Hexadécimal : 0x0400<br/> Décimal : 1024<br/> Entier Short<br/> Hexadécimal : 0x0800<br/> Décimal : 2048<br/> Objet binaire<br/> Hexadécimal : 0x0C00<br/> Décimal : 3072<br/> String<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Hexadécimal : 0x1000<br/> Décimal : 4096<br/> Colonne Nullable. Zéro signifie que la colonne n’accepte pas les valeurs NULL.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Hexadécimal : 0x2000<br/> Décimal : 8192<br/> Colonne de clé primaire. Zéro signifie que cette colonne n’est pas une clé primaire.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15<br/> | Hexadécimal : 0x4000 0x8000<br/> Décimal : 16384 32768<br/> Réservé<br/>                                                                                                                                                                                                                                |



 

Pour obtenir un exemple de script qui illustre la \_ table TransformView, consultez [View a Transform](view-a-transform.md).

 

 




