---
description: Les applications doivent allouer de la mémoire pour ces données ; L’interface TAPI et le fournisseur de services fournissent les données. Si l’opération est asynchrone, les données ne sont pas disponibles tant que le message de réponse asynchrone n’indique pas la réussite.
ms.assetid: 61313fe3-74a1-4195-b5af-37463dad02c1
title: Allocation de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f192e34fdc652293c480277631c3839ecd2435fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514374"
---
# <a name="memory-allocation"></a>Allocation de mémoire

Les applications doivent allouer de la mémoire pour ces données ; L’interface TAPI et le fournisseur de services fournissent les données. Si l’opération est asynchrone, les données ne sont pas disponibles tant que le message de réponse asynchrone n’indique pas la réussite.

Toutes les structures de données utilisées pour passer des données entre l’application et l’interface TAPI sont *aplaties*. Autrement dit, les structures de données ne contiennent pas de pointeurs vers les sous-structures qui contiennent des composants de données de taille variable. Au lieu de cela, les structures de données utilisées pour passer des quantités variables de données à l’application doivent avoir la nanostructure suivante :

``` syntax
  DWORD  dwTotalSize;
  DWORD  dwNeededSize;
  DWORD  dwUsedSize; 
    <fixed size fields> 
  DWORD  dw<VarSizeField1>Size;
  DWORD  dw<VarSizeField1>Offset; 
    <fixed size fields> 
  DWORD  dw<VarSizeField2>Size;
  DWORD  dw<VarSizeField2>Offset; 
    <common extensions> 
    <var sized field1> 
    <var sized field2>
```

Le membre **dwTotalSize** est la taille, en octets, allouée à cette structure de données. Elle marque la fin de la structure de données et est définie par l’application avant d’appeler la fonction qui utilise cette structure de données. La fonction ne lit pas ou n’écrit pas au-delà de cette taille. Une application doit définir le membre **dwTotalSize** pour indiquer le nombre total d’octets alloués pour que l’interface TAPI retourne le contenu de la structure.

L’interface TAPI remplit le membre **dwNeededSize** . Elle indique le nombre d’octets requis pour retourner toutes les données demandées. L’existence de champs de taille variable rend souvent impossible pour l’application d’estimer la taille de la structure de données requise pour l’allocation. Ce champ retourne le nombre d’octets réellement requis pour les données. Ce nombre peut être inférieur, égal ou supérieur à **dwTotalSize**, et il comprend de l’espace pour le membre **dwTotalSize** lui-même. Si la taille est supérieure, la structure retournée n’est que partiellement remplie. Si les champs requis par l’application sont disponibles dans la structure partielle, rien d’autre ne doit être fait. Dans le cas contraire, l’application doit allouer une structure au moins à la taille de **dwNeededSize** et appeler à nouveau la fonction. En règle générale, un espace suffisant est disponible cette fois pour renvoyer toutes les informations, bien qu’il soit possible que la taille soit de nouveau augmentée.

L’interface TAPI remplit le membre **dwUsedSize** s’il retourne des données à l’application pour indiquer la taille réelle, en octets, de la partie de la structure de données qui contient des données utiles. Si, par exemple, une structure qui a été allouée était trop petite et que le champ tronqué est un champ de taille variable, **dwNeededSize** est plus grand que **dwTotalSize** et le champ tronqué est laissé vide. Le membre **dwUsedSize** peut donc être plus petit que **dwTotalSize**. Les valeurs de champ partielles ne sont pas retournées.

Le fait de suivre cet en-tête est la partie fixe de la structure de données. Il contient des champs normaux et des paires taille/décalage qui décrivent les champs de taille variable réels. Le champ décalage contient le décalage en octets du champ de taille variable à partir du début de l’enregistrement. Le champ Taille contient la taille en octets du champ de taille variable. Si un champ de taille variable est vide, le champ taille est égal à zéro et le décalage est défini sur zéro. Les champs de taille variable qui seraient tronqués si la taille totale de la structure est insuffisante sont laissés vides. Autrement dit, leur champ de taille est défini sur zéro et le décalage est défini sur zéro. Les champs de taille variable suivent les champs fixes.

Si le fournisseur de services doit remplir un membre de variable, TAPI initialise la taille et les membres de décalage correspondants à zéro. Si le fournisseur de services remplit le membre de la variable, il doit définir les membres size et offset correspondants aux valeurs appropriées, y compris **dwUsedSize** et **dwNeededSize** s’il définit des membres de variable. Le fournisseur de services ne doit pas tronquer un membre de variable pour l’adapter à l’espace disponible.

Le fournisseur de services doit démarrer les membres de variable immédiatement après les membres fixes de la structure, et conserver tout espace supplémentaire à la fin de la mémoire allouée afin que TAPI puisse l’utiliser pour les membres de longueur variable. Elle peut placer les membres de la variable dans n’importe quel ordre, mais les membres doivent être contigus.

 

 



