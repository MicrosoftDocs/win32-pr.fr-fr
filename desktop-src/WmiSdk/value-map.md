---
description: Une carte de valeur est un tableau lié à une propriété avec les qualificateurs value et ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: ValueMap et qualificateurs de valeur
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34b95b540a99dfaecefcbe0b87e817fd0c44c58606921046476b3411cdd256e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107378"
---
# <a name="valuemap-and-value-qualifiers"></a>ValueMap et qualificateurs de valeur

Une carte de valeur est un tableau lié à une propriété avec les qualificateurs **value** et **ValueMap** .

La propriété agit comme un index dans le tableau, en maintenant une valeur qui représente l’une des valeurs du tableau. À l’aide de code MOF, vous pouvez avoir les types de mappages de valeurs suivants :

-   Tableau mappé à un entier.

    Vous pouvez définir un tableau avec le qualificateur de **valeur** et lier le tableau directement à une propriété entière, comme indiqué dans l’exemple suivant :

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Dans cet exemple, la valeur de la propriété **Status** est un index dans le tableau de chaînes défini par **value**. La propriété ne peut prendre que des valeurs qui correspondent aux positions ordinales dans le tableau de **valeurs** moins 1. Par exemple, la définition de l' **État** sur « 1 » mappe à la valeur « erreur ». La propriété d’index ne peut prendre que des valeurs qui correspondent aux positions dans le tableau de **valeurs** . Par exemple, si le tableau comporte 10 entrées, la valeur de la propriété index peut être comprise entre 0 et 9, et non 30 ou 177.

-   Mappage d’un tableau à un autre tableau à un entier.

    Si vous souhaitez créer un index qui n’utilise pas de système ordinal de comptage, utilisez le qualificateur **ValueMap** . Le qualificateur **ValueMap** définit un autre tableau qui contient un système de numérotation d’index arbitraire, comme illustré dans l’exemple suivant :

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Bien que vous soyez tenu de placer les valeurs de **ValueMap** entre guillemets, WMI prend en compte les valeurs entières. Par conséquent, dans cet exemple, vous pouvez définir la propriété **Status** sur un entier dans l’ensemble **ValueMap** : 1, 3, 99 ou 0. WMI mappe chaque entier d’une position ordinale dans le tableau de chaînes **ValueMap** à une position correspondante dans le tableau de **valeurs** . Par exemple, la définition de l' **État** sur 0 correspond à « inconnu ».

-   Mappage d’un tableau à un autre tableau à une chaîne.

    Si vous ne souhaitez pas utiliser un entier pour indexer votre tableau, vous pouvez utiliser à la place une chaîne pour contenir l’une des valeurs possibles dans votre tableau. Pour ce faire, vous devez définir à la fois une **valeur** et un tableau **ValueMap** qui contiennent tous les deux des chaînes, comme illustré dans l’exemple suivant :

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Avec une propriété de type chaîne, les valeurs réelles autorisées de la propriété sont les entrées du tableau **ValueMap** . Par exemple, vous pouvez définir l' **État** sur « OK » ou « inconnu ».

Il revient à l’application de tirer parti des mappages de façon utile. Il revient au fournisseur d’appliquer une plage légale de valeurs.

## <a name="remarks"></a>Remarques

Pour déterminer s’il faut utiliser les / qualificateurs de **valeur** ValueMap ou de **bitmaps de bitmap** /  , déterminez si l’une des valeurs indiquées peut se produire simultanément. Si plusieurs valeurs simultanées peuvent exister, vous devez utiliser des / **bitvalues** bitmap. Si toutes les valeurs s’excluent mutuellement, vous devez utiliser les / qualificateurs de **valeur** ValueMap.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[BitMap et BitValue](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



