---
description: Est un entier lié à une propriété avec les qualificateurs BitMap et BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificateurs BitMap et BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536357"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Qualificateurs BitMap et BitValue

Une image bitmap est un entier lié à une propriété avec les qualificateurs **bitmap** et **BitValue** . Chaque bit de la valeur de propriété agit comme un index dans le tableau de valeurs de la liste **BitValue** . Étant donné que plusieurs bits de la valeur de propriété peuvent être « on » en même temps, il est possible d’utiliser une seule valeur de propriété pour indiquer plusieurs valeurs simultanées.

Par exemple, l’exemple de code MOF suivant établit la propriété **filetype** comme avec les qualificateurs **bitmap** et **BitValue** . Il établit en outre que le bit de poids faible (bit 0) correspond à la valeur « lecture seule ». Le bit suivant (bit 1) correspond à « Hidden », et ainsi de suite. (Tous les bits ne doivent pas être significatifs. Dans ce système huit bits, les deux bits de poids fort, 6 et 7, n’ont pas d’importance.)

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

Si la propriété **filetype** signale la valeur 7 (bits 0000 0111), le fichier est « lecture seule », « système » et « masqué ». Si la propriété **filetype** signale la valeur 18 (0x12, bits 0001 0010), il s’agit d’un sous-répertoire masqué.

Il existe deux types de bitmaps différents utilisant le code MOF :

-   Bits significatifs consécutifs commençant par le bit de poids faible (bit 0)

    Vous pouvez définir un tableau de valeurs de bit sans spécifier explicitement les bits significatifs si les bits significatifs commencent par le bit de poids faible (bit 0) et progressent sans interruption sur tous les éléments du tableau **BitValue** . L’exemple de code MOF suivant exécute la même fonction que l’exemple précédent.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Bit significatif précédé d’un bit non significatif

    Si le bit de poids faible n’est pas significatif, ou si la séquence de bits significatifs n’est pas continue, vous devez spécifier à la fois les qualificateurs **bitmap** et **BitValue** . L’exemple de code MOF suivant illustre une situation dans laquelle le bit de poids faible n’est pas significatif et il y a un écart dans la séquence de bits significatifs.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    Dans ce cas, la définition du bit de poids faible (bit 0) n’a aucune signification et est ignorée. Toutefois, le bit 1 (0X2) indique que ce message électronique est marqué pour suivi, le paramètre de bit 4 (0x8) indique qu’un accusé de réception doit être envoyé à l’expéditeur lorsque le message électronique est arrivé à la boîte aux lettres du destinataire et que le paramètre bit 5 (0x10) spécifie qu’une confirmation de lecture doit être envoyée à l’expéditeur lorsque le destinataire ouvre le message. La définition des trois bits significatifs (0x1A) spécifie les trois conditions pour le message électronique.

## <a name="remarks"></a>Notes

Pour déterminer s’il faut utiliser les /  qualificateurs de valeurs de bitmap ou de  / **valeurs** ValueMap, déterminez si l’une des valeurs indiquées peut se produire simultanément. Si plusieurs valeurs simultanées peuvent exister, vous devez utiliser des / **bitvalues** bitmap. Si toutes les valeurs s’excluent mutuellement, vous devez utiliser les / qualificateurs de **valeurs** ValueMap.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ValueMap et qualificateurs de valeur](value-map.md)
</dt> </dl>

 

 



