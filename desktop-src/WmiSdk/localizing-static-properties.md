---
description: Vous pouvez localiser des propriétés statiques à l’aide de mappages de valeurs partielles.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localiser des propriétés statiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216676"
---
# <a name="localizing-static-properties"></a>Localiser des propriétés statiques

Vous pouvez localiser des propriétés statiques à l’aide de mappages de valeurs partielles.

La procédure suivante décrit comment les propriétés statiques peuvent être localisées à l’aide de mappages de valeurs partielles avec des expressions régulières.

**Pour utiliser des mappages de valeurs afin de localiser des propriétés statiques**

1.  Créez un fichier MOF maître (Mastervm. MOF).

    L’exemple de code suivant peut être utilisé pour créer un fichier MOF maître (Mastervm. MOF).

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  Créez les versions indépendantes de la langue et spécifiques à la langue du fichier MOF.

    Tapez la commande suivante à l’invite de commandes pour créer les versions indépendantes de la langue et de la langue du fichier MOF.

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    Le compilateur MOF génère les fichiers MOF propres au langage et aux langages, LnVm. mof et LsVm. mfl. Les valeurs de l’anglais américain pour la propriété [numbers](numbers.md) sont placées dans le fichier. MFL pour l’espace de noms anglais américain.

    L’exemple de code suivant affiche le contenu du fichier LsVm. mfl.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  Compilez les deux fichiers MOF et stockez les informations de classe dans le référentiel CIM.

    Tapez la commande suivante à l’invite de commandes pour compiler les deux fichiers MOF.

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  Localisez le fichier MFL pour d’autres paramètres régionaux.

    L’exemple de code suivant montre le contenu d’un fichier MFL pour l’espace de noms français.

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

Le résultat net est que le nom d’affichage et la valeur de la propriété [numbers](numbers.md) dépendent des paramètres régionaux de l’utilisateur connecté. Si l’utilisateur spécifie des paramètres régionaux qui n’ont pas été fournis, les données de qualificateur par défaut proviennent de l’espace de noms anglais (MS \_ 409).

L’implication de cette conception est que chaque valeur de chaîne est utilisée comme identificateur de recherche, qui ne peut pas être localisé. Lorsque vous définissez ce schéma, vous devez vous assurer que la valeur que le fournisseur place dans est indépendante des paramètres régionaux.

> [!Note]  
> WMI ne fournit pas actuellement la prise en charge au moment de l’exécution pour le mappage des valeurs aux chaînes définies par les qualificateurs. L’interprétation de la syntaxe suggérée est la responsabilité de l’application.

 

 

 



