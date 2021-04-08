---
title: Chaînes MOF
description: Une chaîne est un type de données qui contient une chaîne de caractères généralement conçue comme du texte explicite.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863794"
---
# <a name="mof-strings"></a>Chaînes MOF

Une chaîne est un type de données qui contient une chaîne de caractères généralement conçue comme du texte explicite. MOF décrit deux types de chaînes, qui utilisent pour contenir un ou plusieurs caractères. MOF comporte également une série de règles qui décrivent l’utilisation de guillemets dans une chaîne.

Le tableau suivant répertorie les types de données de chaîne pour MOF.



| Type de données  | Type Automation | Description                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **VT \_ I2**      | Caractère Unicode 16 bits unique au format UCS-2 (Universal Character Set 2)<br/> |
| **string** | **VT \_ BSTR**    | Chaîne de caractères Unicode<br/>                                                    |



 

Pour écrire des chaînes pour MOF, suivez les instructions suivantes :

-   Entourez les constantes à un caractère avec des guillemets simples.

    Si vous n’utilisez pas de guillemets simples avec des constantes à caractère unique, vous devez utiliser la représentation entière de la valeur du caractère Unicode. Si vous le souhaitez, vous pouvez spécifier le caractère littéralement avec la \\ séquence d’échappement x du American National Standards Institute (ANSI) C standard, comme indiqué ci-dessous :

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    Comme MOF est basé sur Unicode, vous pouvez également spécifier des valeurs 16 bits.

    Sachez que les constantes à caractère unique au format ANSI C sont entourées de guillemets doubles.

-   Entourez les chaînes de caractères avec des guillemets doubles.

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   Concaténer des chaînes de guillemets successifs avec un ou plusieurs espaces blancs.

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   Utilisez une séquence d’échappement commençant par une barre oblique inverse pour incorporer des guillemets dans une chaîne.

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

L’exemple suivant décrit comment initialiser des propriétés de chaîne et un paramètre de chaîne :

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




