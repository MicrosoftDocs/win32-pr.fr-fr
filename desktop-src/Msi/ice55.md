---
description: ICE55 valide que tous les objets LockPermission existent et ont des valeurs d’autorisation valides.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204190"
---
# <a name="ice55"></a>ICE55

ICE55 valide que tous les objets LockPermission existent et ont des valeurs d’autorisation valides.

## <a name="result"></a>Résultats

ICE55 publie une erreur si un LockObject listé dans la [table LockPermissions](lockpermissions-table.md) n’existe pas ou si aucun niveau de privilège n’est spécifié dans la colonne autorisation.

## <a name="example"></a>Exemple

ICE55 signale les erreurs suivantes pour l’exemple.

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

[Table LockPermissions](lockpermissions-table.md) (partielle)



| LockObject | Table de charge de travail | Domain | Utilisateur  | Autorisation |
|------------|-------|--------|-------|------------|
| Fichier1      | Fichier  |        | guest |            |
| Fichier3      | Fichier  |        | guest | 1          |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Version | Language |
|-------|---------|----------|
| Fichier1 | Fichier2   |          |
| Fichier2 | 1.0.0.0 | 1033     |



 

L’objet fichier1 a une valeur null dans la colonne autorisation. Chaque ligne doit avoir une valeur dans la colonne autorisations. Pour corriger cette erreur, spécifiez une valeur numérique dans cette colonne. Si aucun privilège n’est nécessaire pour cet objet, vous devez supprimer la ligne.

L’objet fichier3 décrit dans la table LockPermissions n’est pas répertorié dans la table file. Pour corriger cette erreur, reportez-vous à un objet valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



