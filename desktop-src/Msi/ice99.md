---
description: ICE99 vérifie qu’aucun nom de propriété entré dans la table de répertoire ne duplique un nom réservé pour l’utilisation publique ou privée de l’Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315269"
---
# <a name="ice99"></a>ICE99

ICE99 vérifie qu’aucun nom de propriété entré dans la table de [répertoire](directory-table.md) ne duplique un nom réservé pour l’utilisation publique ou privée de l’Windows Installer.

## <a name="result"></a>Résultat

ICE99 publie l’erreur suivante.



| Erreur ICE99                                                                                                      | Description                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Le nom du répertoire : \[ 1 \] est identique à l’une des propriétés publiques du MSI et peut entraîner des effets secondaires imprévus. | la valeur de la colonne directory de la table [directory](directory-table.md) duplique un nom de propriété réservé par le Windows Installer. |



 

## <a name="example"></a> Exemple

ICE99 signale l’erreur suivante pour l’exemple :

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Répertoire](directory-table.md) (partiel)



| Répertoire        | Répertoire \_ parent | DefaultDir |
|------------------|-------------------|------------|
| CustomActionData |                   |            |



 

Pour corriger cet avertissement, vous devez modifier le nom de CustomActionData.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> <dt>

[Table de répertoire](directory-table.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,0 et versions antérieures](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



