---
description: La création de définitions de classe localisées est un processus en trois étapes.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Création de définitions de classes localisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d7cb5f2970c3696de7cdd1bdb9d61d6eed5e86dc60c8941eec475d15145dd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374769"
---
# <a name="creating-localized-class-definitions"></a>Création de définitions de classes localisées

La création de définitions de classe localisées est un processus en trois étapes. Vous commencez par écrire du code MOF qui définit les classes, y compris tous les qualificateurs qui doivent être localisés. Ce fichier d’origine est appelé le fichier « Master MOF », car il contient tous les qualificateurs et propriétés qui définissent la classe.

Ensuite, utilisez le [compilateur MOF](mofcomp.md) pour créer les versions indépendantes du langage et de la langue du fichier MOF. Le compilateur MOF place la description de la classe de base dans un nouveau fichier MOF et crée une version localisée du fichier MOF qui contient uniquement les propriétés et les qualificateurs qui doivent être localisés. Bien que les versions propres aux langages et aux langues indépendantes du fichier MOF puissent avoir le même nom de fichier, vous devez utiliser une extension de nom de fichier. MFL pour indiquer que le fichier contient des informations localisées. Vous pouvez localiser le fichier. MFL avec d’autres paramètres régionaux, si nécessaire. Le stockage des définitions de classe dans le référentiel CIM nécessite une étape supplémentaire de l’utilisation du compilateur MOF pour compiler à la fois les fichiers MOF de langue neutre et les fichiers MOF spécifiques à une langue.

Les étapes suivantes décrivent comment créer et stocker une définition de classe localisée.

**Pour créer et stocker une définition de classe localisée**

1.  Créez le fichier MOF maître qui définit les classes que vous souhaitez localiser.

    Enregistrez ce code MOF dans un fichier appelé Mastermof. mof.

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  Créez des versions indépendantes de la langue et de la langue du fichier MOF en compilant le fichier MasterMOF. mof.

    Tapez la commande suivante à l’invite de commandes pour compiler le fichier MasterMOF. mof.

    **mofcomp-MOF : Lnmof. mof-MFL : Lsmof. MFL-amendement : MS \_ 409 Mastermof. mof**

3.  Compilez les fichiers indépendants du langage (Lnmof. MOF) et les fichiers spécifiques à la langue (Lsmof. MFL) et stockez les informations de classe dans le référentiel CIM.

    Tapez les commandes suivantes à l’invite de commandes pour stocker les informations de classe dans le référentiel CIM.

    **Mofcomp Lnmof. mof**

    **Mofcomp Lsmof. MFL**

    Une fois que vous avez compilé ces fichiers, vous aurez une définition de classe indépendante du langage dans l' \\ espace de noms de test racine et une définition de classe localisée dans l' \\ espace de \\ noms MS 409 de test racine \_ . Pour plus d’informations sur la compilation des fichiers MOF localisés, consultez [compilation des fichiers MOF localisés](compiling-localized-mof-files.md).

 

 



