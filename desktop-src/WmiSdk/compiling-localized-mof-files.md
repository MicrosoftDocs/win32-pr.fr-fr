---
description: Vous devez compiler votre fichier MOF maître pour créer les fichiers MOF propres à une langue et spécifiques à une langue.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilation des fichiers MOF localisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d23c77fee8a745b6032848c124a24ffb8e7cf626b0ff3c87fecc7e05b14d372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556798"
---
# <a name="compiling-localized-mof-files"></a>Compilation des fichiers MOF localisés

Vous devez compiler votre fichier MOF maître pour créer les fichiers MOF propres à une langue et spécifiques à une langue.

Tapez la commande suivante à l’invite de commandes pour compiler un fichier MOF maître.

**mofcomp-MOF : Lnmof. mof-MFL : Lsmof. MFL-amendement : MS \_ 409 Mastermof. mof**

Lorsque vous exécutez cette commande, le compilateur MOF crée deux fichiers MOF à partir du fichier Mastermof. mof d’origine. Le compilateur MOF produit une version indépendante du langage, Lnmof. mof, dans laquelle tous les éléments spécifiques au langage sont supprimés. Une deuxième version propre à la langue, Lsmof. mof, est également créée. ce fichier contient uniquement les éléments qui ont été marqués avec la version de qualificateur [**modifiée**](qualifier-flavors.md) dans le fichier Mastermof. mof.

L’exemple de code suivant montre le contenu du fichier MOF indépendant du langage (Lnmof. MOF) qui est généré.

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

L’exemple de code suivant affiche le contenu du fichier MOF spécifique au langage (Lsmof. MFL) qui est généré.

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

La compilation d’un fichier MOF avec le qualificateur [**modifié**](qualifier-flavors.md) génère uniquement des fichiers MOF indépendants du langage et propres aux langages. le référentiel CIM n’est pas mis à jour avec les nouvelles informations de classe. Vous devez utiliser le compilateur MOF pour compiler les deux fichiers MOF générés par la première compilation avant que toutes les informations de classe ne soient disponibles pour WMI.

Quand vous compilez un fichier MOF maître, seuls les qualificateurs avec la version [**modifiée**](qualifier-flavors.md) sont déplacés vers le fichier MOF propre au langage. Les qualificateurs qui n’ont pas la version **modifiée** ne sont pas localisés et n’existent que dans la définition de la classe de base dans le fichier MOF indépendant du langage. Les qualificateurs non localisés peuvent être utilisés pour les descriptions par défaut si les descriptions localisées ne sont pas disponibles.

Vous pouvez utiliser la commande [pragma Amendement](pragma-amendment.md) [**au lieu de spécifier**](qualifier-flavors.md) Changed en tant que commutateur pour le compilateur MOF. L’une ou l’autre de ces options est équivalente à la demande de versions spécifiques à une langue et indépendantes du langage d’un fichier MOF. Si vous utilisez la commande pragma amendement ou l’option de ligne de commande **modifiée** , vous devez spécifier le nom des fichiers de sortie à l’aide des options **-MFL** et **-MOF** à l’invite de commandes.

> [!Note]  
> Le fichier MOF indépendant du langage généré par le compilateur MOF contient l’équivalent décimal de l’ID de paramètres régionaux, même si cette valeur a été entrée au format hexadécimal. Dans l’exemple ci-dessus, le compilateur a converti la valeur 0x40C en nombre décimal 1033 pour le fichier de sortie Lnmof. mof.

 

 

 



