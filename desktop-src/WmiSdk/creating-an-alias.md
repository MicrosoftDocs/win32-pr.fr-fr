---
description: Un alias dans WMI est une référence symbolique dans une classe ou une instance de classe située ailleurs dans un fichier format MOF (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Création d’un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403880"
---
# <a name="creating-a-wmi-alias"></a>Création d’un alias WMI

Un [*alias*](gloss-a.md) dans WMI est une référence symbolique dans une classe ou une instance de classe située ailleurs dans un fichier format MOF (MOF). Le compilateur MOF utilise des alias pour établir des références entre les classes et les instances. Le compilateur résout les alias des classes auxquelles ils font référence. par conséquent, les noms d’alias ne sont pas disponibles dans le code compilé. Par conséquent, les applications clientes ne peuvent pas faire référence à des classes à l’aide d’alias.

> [!Note]  
> WMI prend en charge les alias de référence en avant, mais pas les alias circulaires.

 

Un alias a uniquement une portée dans le fichier MOF dans lequel vous déclarez l’alias. Par conséquent, vous utilisez généralement un alias comme raccourci vers un long chemin d’accès d’objet.

**Pour définir un alias**

1.  Ajoutez l’expression « As $*aliasname*» à la déclaration de classe ou d’instance.
2.  Les noms d’alias suivent les mêmes règles que les noms d’instance et de classe, sauf que les noms d’alias doivent commencer par un signe dollar ($). Les traits de soulignement peuvent apparaître dans un nom d’alias à la suite du caractère initial.

L’exemple de code suivant décrit comment utiliser un alias dans une définition de classe.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

Les exemples de code suivants décrivent comment utiliser un alias comme référence symbolique à un chemin d’accès à un objet. Ces exemples déclarent deux classes pour décrire un disque : la classe Disk pour indiquer la lettre de lecteur et la classe DiskRef pour indiquer le chemin d’accès au disque. Un alias est défini pour l’instance de classe de disque. Cet alias est utilisé comme valeur pour la propriété PathToDisk dans l’instance DiskRef.

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une classe](creating-a-class.md)
</dt> </dl>

 

 



