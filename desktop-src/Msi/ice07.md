---
description: ICE07 valide le fait que le package d’installation spécifie que les polices doivent être installées dans le FontsFolder. Si une police est installée dans un dossier autre que le FontsFolder, le programme d’installation crée un raccourci plutôt que d’installer réellement la police.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a0e555a35c7d5735abe0b14520d000bfeea8c888488ce37b15a78674ff9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581289"
---
# <a name="ice07"></a>ICE07

ICE07 valide le fait que le package d’installation spécifie que les polices doivent être installées dans le FontsFolder. Si une police est installée dans un dossier autre que le FontsFolder, le programme d’installation crée un raccourci plutôt que d’installer réellement la police.

L’action personnalisée ICE07 effectue les opérations suivantes pour chaque police de la [table de polices](font-table.md).

1.  Recherche le fichier de police auquel chaque titre de police appartient à l’aide de la [table de polices](font-table.md).
2.  Interroge la \_ colonne de composant de la [table de fichiers](file-table.md) pour le composant qui contrôle chaque fichier.
3.  Interroge la \_ colonne Directory de la [table Component](component-table.md) pour obtenir une clé dans la table de répertoires.
4.  Résout la [table de répertoire](directory-table.md) pour déterminer le nom du dossier dans lequel le programme d’installation doit installer le fichier de police
5.  Publie une erreur si le fichier de police est en cours d’installation dans un dossier autre que FontsFolder.

## <a name="result"></a>Résultat

ICE07 publie une erreur s’il détecte que la base de données spécifie qu’un fichier de polices doit être installé dans un dossier autre que FontsFolder.

## <a name="example"></a>Exemples

IC07 publie le message d’erreur suivant pour l’exemple indiqué.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Tableau des polices](font-table.md)



| fichier\_ | FontTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier   | Composant\_   |
|--------|---------------|
| Myrtle | Myrtle \_ Beach |



 

[Table des composants](component-table.md) (partielle)



| Composant     | Répertoire\_ |
|---------------|-------------|
| Myrtle \_ Beach | SandBar     |



 

Dans cet exemple, la police Tahoma est mappée au fichier de polices Myrtle. Le fichier Myrtle appartient au composant Myrtle \_ Beach. La résolution de la table d’annuaires indique que tous les fichiers appartenant à Myrtle \_ Beach doivent être installés dans le dossier Sandbar. Comme il ne s’agit pas du FontsFolder, ICE07 publie un message d’erreur.

Notez que si le composant Myrtle \_ Beach appartient dans le dossier Sandbar, et non dans le FontsFolder, la police Tahoma ne peut pas appartenir à Myrtle \_ Beach. Un correctif possible pour l’erreur consisterait à inclure Tahoma dans un autre composant qui est installé dans le répertoire FontsFolder.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



