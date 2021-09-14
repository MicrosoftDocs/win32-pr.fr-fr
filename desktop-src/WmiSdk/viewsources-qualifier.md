---
description: Toutes les classes d’affichage doivent avoir un qualificateur de tableau de chaînes appelé ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Qualificateur ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923307"
---
# <a name="viewsources-qualifier"></a>Qualificateur ViewSources

Toutes les classes d’affichage doivent avoir un qualificateur de tableau de chaînes appelé **ViewSources**. Le qualificateur **ViewSources** contient les requêtes source qui définissent les instances source utilisées dans la classe de vue. La valeur du qualificateur **ViewSources** est un tableau de chaînes contenant des requêtes [*langage de requêtes WMI (WQL) (WQL)*](gloss-w.md) . Vous pouvez définir des classes sources et restreindre les instances sources que votre classe de vue utilise avec la[clause](where-clause.md) d' [interrogation avec WQL](querying-with-wql.md)pour créer une vue filtrée.

Le [fournisseur de vues](view-provider.md) met en correspondance les requêtes sources du qualificateur **ViewSources** avec les espaces de noms répertoriés dans le [qualificateur ViewSpaces](viewspaces-qualifier.md) dans l’ordre dans lequel les requêtes et les espaces de noms sont répertoriés. Le nombre de requêtes source doit correspondre au nombre d’espaces de noms figurant dans le qualificateur ViewSpaces. L’ordre dans lequel vous répertoriez les requêtes source détermine les espaces de noms à partir desquels les instances source sont dessinées.

L’exemple suivant sélectionne uniquement les instances de la classe **LocalDisk** où la valeur de la propriété **FileSystem** est « NTFS » et les instances de la classe **RemoteDisk** où la valeur de la propriété **FreeSpace** est supérieure à 45 mégaoctets :


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> Le nombre de requêtes sources que vous pouvez définir pour les classes de vue de jointure dépend du nombre d’instances retournées par ces requêtes et du nombre de façons dont ces instances peuvent être jointes. Le nombre de combinaisons possibles d’instances source pour les classes d’affichage augmente de façon exponentielle, donc gardez les requêtes source pour les classes de vue de jointure aussi simples que possible.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs spécifiques au fournisseur de vues**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




