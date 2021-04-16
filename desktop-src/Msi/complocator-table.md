---
description: La table CompLocator contient les informations nécessaires pour trouver un fichier ou un répertoire qui utilise les données de configuration du programme d’installation.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Table CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530238"
---
# <a name="complocator-table"></a>Table CompLocator

La table CompLocator contient les informations nécessaires pour trouver un fichier ou un répertoire qui utilise les données de configuration du programme d’installation.

La table CompLocator contient les informations suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificateur](identifier.md) | O   | N        |
| ComponentId | [GUID](guid.md)             | N   | N        |
| Type        | [Integer](integer.md)       | N   | O        |



 

## <a name="column-information"></a>Informations sur les colonnes

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

Cette colonne représente une signature de fichier unique et est également la clé externe dans la [table de signatures](signature-table.md). Si la clé est absente de la table de signatures, la recherche est supposée être en présence d’un répertoire désigné par la table CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

ID du composant dont le chemin d’accès de clé doit être utilisé pour la recherche. Il doit s’agir du GUID d’un composant qui apparaît dans le champ ComponentId de la [table des composants](component-table.md). Il peut s’agir de l’ID d’un composant appartenant à un autre produit installé sur l’ordinateur. Il ne doit pas s’agir du GUID d’un composant publié apparaissant dans le champ ComponentId de la [table PublishComponent](publishcomponent-table.md).

Pour trouver la valeur GUID de l’ID du composant pour un fichier installé par un autre produit, accédez au package d’installation du produit. Accédez à la [table file](file-table.md) et recherchez la ligne contenant l’identificateur de fichier du fichier. La \_ colonne composant de cette ligne contient l’identificateur de composant pour le composant qui contrôle le fichier. Accédez à la [table des composants](component-table.md) et recherchez la ligne qui contient cet identificateur de composant dans la colonne composant. La colonne ComponentId de cette ligne contient le GUID de l’ID du composant.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Valeur booléenne qui détermine si le chemin d’accès de la clé du composant est un nom de fichier ou un emplacement de répertoire.

Le tableau suivant répertorie les valeurs valides. Si elle est absente, le type est défini sur 1 (un).



| Constante                      | Valeur hexadécimale | Decimal | Description              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Le chemin d’accès de la clé est un répertoire. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Le chemin d’accès de la clé est un nom de fichier. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette table est utilisée avec la [table AppSearch](appsearch-table.md).

En règle générale, les colonnes de cette table ne sont pas localisées. Si un auteur décide de rechercher des produits dans plusieurs langues, il peut y avoir une entrée distincte incluse dans le tableau pour chaque langue.

Pour plus d’informations, consultez [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



