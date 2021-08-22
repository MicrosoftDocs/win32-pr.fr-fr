---
description: ICE02 valide le fait que certaines références entre le composant, le fichier et les tables du Registre sont réciproques. Ces références doivent être réciproques pour permettre au programme d’installation de déterminer correctement l’état d’installation des composants.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97696ee4a8f93d49237dbac8661b6bfc72e478922c87b9095620bc5c29dc546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946653"
---
# <a name="ice02"></a>ICE02

ICE02 valide le fait que certaines références entre le [composant](component-table.md), le [fichier](file-table.md)et les tables [du Registre](registry-table.md) sont réciproques. Ces références doivent être réciproques pour permettre au programme d’installation de déterminer correctement l’état d’installation des composants.

Le programme d’installation utilise la colonne keyPath de la table Component pour détecter la présence du composant figurant dans la colonne Component. La colonne keyPath contient une clé dans le registre ou les tables de fichiers. Ces deux tables ont une colonne de composant \_ qui contient une clé dans la table des composants pointant vers le composant qui contrôle l’entrée ou le fichier de registre. Ces références doivent être réciproques.

## <a name="result"></a>Résultat

ICE02 publie un message d’erreur s’il trouve une référence qui doit être réciproque et ne l’est pas.

## <a name="example"></a>Exemple

ICE02 publie le message d’erreur suivant pour un fichier .msi contenant les entrées de la base de données affichées.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Table des composants](component-table.md) (partielle)



| Composant | KeyPath   |
|-----------|-----------|
| Rouge       | \_Fichier rouge |
| Bleu      | \_Fichier rouge |



 

[Table de fichiers](file-table.md) (partielle)



| Colonne de fichier | Composant\_ |
|-------------|-------------|
| \_Fichier rouge   | Rouge         |
| \_Fichier Blue  | Bleu        |



 

Le composant Blue fait référence \_ à un fichier rouge, mais le fichier rouge \_ n’est pas contrôlé par le composant Blue et ne peut donc pas être le fichier keyPath. Si le programme d’installation a été appelé pour avoir l’état d’installation bleu, il ne vérifierait pas correctement si le \_ fichier rouge a été installé. La modification du champ keyPath pour Blue dans la table Component en \_ fichier Blue corrige l’erreur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



