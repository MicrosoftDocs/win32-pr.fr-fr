---
description: Cette table temporaire active l’option de désinstallation correctif de l’action personnalisée pour les actions personnalisées ajoutées ou mises à jour par un correctif.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b6c46ebfcfb82ee23ce6acec998490f53fe67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111050"
---
# <a name="msitransformview"></a>MsiTransformView

Cette table temporaire active l' [option de désinstallation correctif de l’action personnalisée](custom-action-patch-uninstall-option.md) pour les actions personnalisées ajoutées ou mises à jour par un correctif.

si un correctif ajoute ou met à jour une action personnalisée ayant l’attribut **msidbCustomActionTypePatchUninstall** , Windows Installer exécute l’action personnalisée nouvelle ou mise à jour lorsque le correctif est désinstallé. Windows Le programme d’installation rend les mises à jour dans le correctif en cours de désinstallation disponibles pour l’action personnalisée de désinstallation des correctifs. le correctif doit inclure une table MsiTransformView *&lt; PatchGUID &gt;* pour fournir ces informations à Windows Installer. Les informations contenues dans ce tableau sont disponibles pour toute action personnalisée immédiate et ne sont pas disponibles pour les actions personnalisées différées.

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge. l' [Option de désinstallation corrective de l’Action personnalisée](custom-action-patch-uninstall-option.md) est disponible à partir de Windows Installer 4,5.

Cette table doit être nommée MsiTransformView *&lt; PatchGUID &gt;* table, où *&lt; PatchGUID &gt;* est le GUID qui identifie de façon unique le correctif. La table MsiTransformView *&lt; PatchGUID &gt;* contient les colonnes suivantes.



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

Les actions personnalisées de désinstallation des correctifs s’exécutent lorsque le correctif est désinstallé. Elles ne s’exécutent pas lorsque le produit est désinstallé. Utilisez l' [option de désinstallation corrective action personnalisée](custom-action-patch-uninstall-option.md) et le tableau ci-dessous pour exécuter une opération personnalisée uniquement lorsque le correctif est en cours de désinstallation.

Un correctif peut mettre à jour une action personnalisée fournie dans le package d’origine (fichier .msi.) Pour exécuter la version mise à jour de l’action personnalisée lorsque le correctif est désinstallé, marquez l’action personnalisée avec l’attribut **msidbCustomActionTypePatchUninstall** dans le package d’origine.

 

 



