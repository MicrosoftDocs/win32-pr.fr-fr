---
description: ICE92 vérifie qu’un composant sans GUID d’ID de composant n’est pas également spécifié en tant que composant permanent.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866089"
---
# <a name="ice92"></a>ICE92

ICE92 vérifie qu’un composant sans GUID d’ID de composant n’est pas également spécifié en tant que composant permanent. Cette action personnalisée ICE vérifie la [table](component-table.md) des composants pour rechercher les composants sans [GUID](guid.md) spécifié dans le champ ComponentID et vérifie que l’indicateur **msidbComponentAttributesPermanent** n’a pas été défini dans le champ attributs. ICE92 vérifie également qu’aucun composant n’a à la fois les attributs **msidbComponentAttributesPermanent** et **msidbComponentAttributesUninstallOnSupersedence** .

Si la colonne ComponentId a la valeur null, le programme d’installation n’inscrit pas le composant et le composant ne peut pas être supprimé ou réparé par le programme d’installation.

## <a name="result"></a>Résultats

ICE92 publie l’erreur suivante.



| Erreur ICE92                                                          | Description                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le composant' \[ 1 \] 'n’a pas de ComponentID et est marqué comme permanent. | L’entrée de ce composant dans la table des composants a la valeur null dans la colonne ComponentId et contient **msidbComponentAttributesPermanent** dans la colonne attributs. |



 

ICE92 publie l’avertissement suivant.



| AVERTISSEMENT ICE92                                                                                                                                                           | Description                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le composant « \[ 1 \] » est marqué comme permanent et désinstallation lors du remplacement. L’attribut Uninstall-on-deremplacement sera ignoré, car le composant est permanent. | L’entrée de ce composant dans la [table des composants](component-table.md) a les attributs **msidbComponentAttributesPermanent** et **msidbComponentAttributesUninstallOnSupersedence** spécifiés. |



 

## <a name="example"></a>Exemple

ICE92 signale l’erreur suivante pour l’exemple :

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Table des composants](component-table.md) (partielle)



| Composant  | ComponentId | Répertoire\_ | Attributs | KeyPath |
|------------|-------------|-------------|------------|---------|
| Composant1 |             | Annuaire  | 16         | Filea   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



