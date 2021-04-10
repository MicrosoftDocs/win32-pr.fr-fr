---
description: Plusieurs consommateurs, tels que le consommateur d’événements active script ou le consommateur d’événements en ligne de commande, ont des propriétés de chaîne avec le qualificateur de modèle.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Utilisation de modèles de chaîne standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866866"
---
# <a name="using-standard-string-templates"></a>Utilisation de modèles de chaîne standard

Plusieurs consommateurs, tels que le consommateur d’événements active script ou le consommateur d’événements en ligne de commande, ont des propriétés de chaîne avec le qualificateur de **modèle** . Ces propriétés utilisent des modèles de chaîne standard pour construire une chaîne configurée en partie par l’instance de consommateur et en partie par un événement. La structure d’un modèle de chaîne standard est semblable à la spécification de variable d’environnement Microsoft Windows.

La liste suivante présente quelques exemples de la langue du modèle :

-   La chaîne « some Text here » produit toujours la chaîne « some Text here ».
-   « % CPUUtilization% » produit toujours la valeur de la propriété **CPUUtilization** de l’événement qui est remis. Si la propriété n’est pas une chaîne, elle est convertie en chaîne ; par exemple, « 90 » ou « TRUE ».
-   « L’utilisation du processeur de ce processeur est de% CPUUtilization% à ce moment-là » incorpore la valeur de la propriété **CPUUtilization** de l’événement dans la chaîne, ce qui produit un résultat tel que « l’utilisation du processeur de ce processeur est de 90 pour l’instant ».
-   « % TargetInstance. CPUUtilization% » récupère la valeur de la propriété **CPUUtilization** dans l’instance incorporée de la propriété **TargetInstance** .
-   « %% » produit un seul signe%.
-   Si la propriété Récupérée est un tableau, le tableau entier est généré au format suivant : « (1, 5, 10, 1024) ». S’il n’y a qu’un seul élément dans le tableau, les parenthèses sont omises. S’il n’y a aucun élément dans le tableau, "()" est produit.
-   Si une propriété est un objet incorporé, la représentation MOF de l’objet est générée (semblable à la méthode [**IWbemClassObject :: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).
-   Si une propriété d’un tableau incorporé d’objets est demandée, elle est traitée comme une propriété avec une valeur de tableau. Par exemple :% MyEvents. TargetInstance. DriverLetter% pourrait produire' ("C :", "D :") 'si MyEvents est un tableau d’événements de modification d’instance incorporée.

## <a name="string-literals"></a>Littéraux de chaîne

Tout ce qui se trouve à l’intérieur d’une paire de guillemets est considéré comme un littéral de chaîne et ne sera pas remplacé.

L’exemple suivant montre la chaîne que le compilateur voit pour « l’utilisation du processeur est% CPUUtilization% ».

``` syntax
CPU utilization is %CPUUtilization%
```

Cette chaîne produit la sortie suivante.

``` syntax
CPU utilization is 90
```

En revanche, la chaîne « utilisation de l’UC \\ » est « % CPUUtilization% \\ » est visible par le compilateur comme suit.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Cette chaîne produit la sortie suivante, sans substitution de variable.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



