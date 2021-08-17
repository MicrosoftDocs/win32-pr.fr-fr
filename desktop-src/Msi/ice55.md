---
description: ICE55 valide que tous les objets LockPermission existent et ont des valeurs d’autorisation valides.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044b9993c6c50dce32c04f98d8e000f0faae4280d244c4656d7b0cbed7b49749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635140"
---
# <a name="ice55"></a>ICE55

ICE55 valide que tous les objets LockPermission existent et ont des valeurs d’autorisation valides.

## <a name="result"></a>Résultat

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



| LockObject | Table de charge de travail | Domaine | Utilisateur  | Autorisation |
|------------|-------|--------|-------|------------|
| Fichier1      | Fichier  |        | guest |            |
| Fichier3      | Fichier  |        | guest | 1          |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Version | Langage |
|-------|---------|----------|
| Fichier1 | Fichier2   |          |
| Fichier2 | 1.0.0.0 | 1033     |



 

L’objet fichier1 a une valeur null dans la colonne autorisation. Chaque ligne doit avoir une valeur dans la colonne autorisations. Pour corriger cette erreur, spécifiez une valeur numérique dans cette colonne. Si aucun privilège n’est nécessaire pour cet objet, vous devez supprimer la ligne.

L’objet fichier3 décrit dans la table LockPermissions n’est pas répertorié dans la table file. Pour corriger cette erreur, reportez-vous à un objet valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



