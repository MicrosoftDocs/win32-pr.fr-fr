---
description: À l’instar de nombreuses autres techniques en format MOF (MOF), l’application d’un qualificateur à votre code est un processus relativement simple.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Application d’un qualificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760779"
---
# <a name="applying-a-qualifier"></a>Application d’un qualificateur

À l’instar de nombreuses autres techniques en format MOF (MOF), l’application d’un qualificateur à votre code est un processus relativement simple.

Les conventions d’affectation de noms appliquées par WMI sont les suivantes :

-   Un qualificateur peut décrire une classe, une instance, une propriété, une méthode ou un paramètre de méthode.
-   Les noms de qualificateurs ne peuvent pas avoir de traits de soulignement de début ou de fin.
-   Un nom de qualificateur ne peut pas commencer par un chiffre.
-   Un nom de qualificateur ne peut pas contenir de caractères spéciaux tels que & \* @ ! ~ \\ /.
-   Tous les noms de qualificateurs ne respectent pas la casse.
-   Vous ne pouvez pas redéfinir les qualificateurs WMI standard ou les qualificateurs décrits dans la spécification CIM DMTF.
-   Les types de qualificateurs ne sont pas explicitement déclarés.

    Si vous ne déclarez pas de type de qualificateur, WMI suppose que le type est booléen avec la valeur **true**. Sinon, les qualificateurs de type WMI sont basés sur les valeurs de qualificateur que vous déclarez.

-   Lorsque vous créez vos propres qualificateurs, vous devez faire précéder le nom de votre schéma d’un nom de qualificateur.

    L’objectif de cette règle est d’éviter toute confusion avec les nouveaux qualificateurs.

-   Vous pouvez créer des tableaux homogènes de qualificateurs.

    L’exemple de code suivant montre comment les tableaux de qualificateurs sont spécifiés à l’aide d’accolades qui entourent les valeurs.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI ne prend pas en charge les types Automation non listés dans la référence, tels que VT \_ null. Pour plus d’informations, consultez [types de données MOF](mof-data-types.md).

La procédure suivante vous aide à utiliser C++ pour ajouter un qualificateur à une propriété.

**Pour appliquer un qualificateur à l’aide de C++**

-   Appliquez le qualificateur avec un appel à la méthode [**IWbemQualifierSet ::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    Vous pouvez utiliser d’autres méthodes de [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) pour récupérer ou supprimer des qualificateurs existants.

La procédure suivante vous permet d’appliquer un qualificateur dans les fichiers MOF.

**Pour décrire un mot clé ou un identificateur avec un qualificateur à l’aide de MOF**

-   Placez un qualificateur entre crochets avant le mot clé ou l’identificateur décrit par le qualificateur.

    L’exemple de code suivant montre comment les qualificateurs sont utilisés.

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    L’exemple suivant décrit le positionnement correct des qualificateurs.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



