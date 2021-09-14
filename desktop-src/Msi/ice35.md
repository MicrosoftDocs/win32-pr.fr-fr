---
description: ICE35 valide que les composants contenant des fichiers compressés stockés dans un fichier CAB ne sont pas configurés pour s’exécuter à partir de la source. avec Windows Installer 2,0 ou une version ultérieure, cette restriction a été supprimée.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021568"
---
# <a name="ice35"></a>ICE35

ICE35 valide que les composants contenant des fichiers compressés stockés dans un [fichier CAB](cabinet-files.md) ne sont pas configurés pour s’exécuter à partir de la source. avec Windows Installer 2,0 ou une version ultérieure, cette restriction a été supprimée.

ICE35 interroge la colonne CAB de la [table Media](media-table.md) pour déterminer quels fichiers sont compressés et stockés dans un fichier CAB. Il interroge la [table de fichiers](file-table.md) pour identifier les composants qui contiennent ces fichiers. Enfin, il vérifie la [table des composants](component-table.md) pour déterminer si les bits d’exécution à partir de la source sont définis dans la colonne attributs.

## <a name="result"></a>Résultats

ICE35 publie un message d’erreur s’il existe un fichier compressé stocké dans un fichier CAB appartenant à un composant avec le bit msidbComponentAttributesSourceOnly défini dans la colonne attributs de la [table des composants](component-table.md). avec Windows Installer 2,0 ou une version ultérieure, la valeur d’un message d’avertissement est remplacée par une erreur. un package qui prend uniquement en charge Windows Installer 2,0 et versions ultérieures a la \_ propriété PID PAGECOUNT du flux d’informations de synthèse définie sur une valeur d’au moins 200.

ICE35 publie un message d’avertissement si un fichier compressé est stocké dans un fichier CAB appartenant à un composant avec le bit msidbComponentAttributesOptional défini dans la colonne attributs de la [table des composants](component-table.md). ce message d’avertissement a été supprimé avec Windows Installer 2,0 et versions ultérieures.

Si plusieurs fichiers d’un composant se trouvent dans un fichier CAB, ICE35 signale les erreurs pour chaque fichier dont l’exécution provient du bit source défini.

## <a name="example"></a>Exemple

ICE35 signale les erreurs et avertissements suivants pour l’exemple indiqué à l’aide d’une version antérieure à la version 2,0 de Windows Installer.



| Erreur ICE35                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERREUR : le composant Component3 ne peut pas être exécuté à partir de la source uniquement, car son fichier membre’fichier3 'est compressé. | Un fichier compressé est stocké dans un fichier CAB et ce fichier appartient à un composant avec le bit SourceOnly défini dans la colonne attributs de la [table des composants](component-table.md). Pour corriger cette erreur, remplacez les 2 bits inférieurs de la valeur des attributs Component2's par « 00 », ce qui correspond uniquement à local, ou supprimez Fichier4 du fichier CAB.<br/>                                                                                                                                                                         |
| ERREUR : le composant Component3 ne peut pas être exécuté à partir de la source uniquement, car son fichier membre’fichier3 'est compressé. | Un fichier compressé est stocké dans un fichier CAB et ce fichier appartient à un composant avec le bit SourceOnly défini dans la colonne attributs de la [table des composants](component-table.md). Étant donné que les fichiers d’un composant ne doivent pas nécessairement provenir du même support, ICE35 signale les erreurs pour chaque fichier du composant qui se trouve dans un fichier CAB.<br/> Pour corriger cette erreur, remplacez les 2 bits inférieurs de la valeur des attributs Component2's par « 00 », ce qui correspond uniquement à local, ou supprimez Fichier4 du fichier CAB.<br/> |



 

[Table des médias](media-table.md) (partielle)



| DiskID | LastSequence | CAB   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Composant\_ | Séquence |
|-------|-------------|----------|
| Fichier1 | Composant1  | 1        |
| Fichier2 | Component2  | 2        |
| Fichier3 | Component2  | 3        |
| Fichier4 | Component3  | 4        |
| Fichier5 | Component3  | 5        |



 

[Table des composants](component-table.md) (partielle)



| Composant  | Attributs |
|------------|------------|
| Composant1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Icône\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

Notez que les fichiers peuvent également être marqués comme compressés à l’aide de la propriété [**Résumé du nombre de mots**](word-count-summary.md) du flux d’informations de [synthèse](summary-information-stream.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




