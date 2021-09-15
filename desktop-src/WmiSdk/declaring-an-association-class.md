---
description: Une classe d’association est un type spécial de classe qui définit une relation entre deux autres classes.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Déclaration d’une classe d’association
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411572"
---
# <a name="declaring-an-association-class"></a>Déclaration d’une classe d’association

Une classe d’association est un type spécial de classe qui définit une relation entre deux autres classes.

La procédure suivante décrit comment créer une classe d’association à l’aide de code MOF.

**Pour créer une classe d’association à l’aide de code MOF**

1.  Assignez le qualificateur d' **Association** à votre classe.

    Bien qu’il soit possible de créer une classe avec des références à des objets ou des classes, le fait d’utiliser le qualificateur **Association** indique non seulement que votre classe est une classe d’association, mais, comme meilleure pratique, garantit que votre classe fonctionne pleinement comme une classe d’association.

2.  Créez deux références dans la classe décrivant les deux instances d’objet que vous souhaitez associer à l’aide du type **ref** .

    Les références lient les deux objets de l’Association en contenant les chemins d’accès aux objets. Bien que cela ne soit pas obligatoire, utilisez également les propriétés de référence en tant que propriétés de clé.

    Bien que vous puissiez créer des références relatives à l’espace de noms ou à des espaces de noms complets, WMI n’a qu’une prise en charge limitée des références entre espaces de noms. Plus précisément, seuls les objets définis statiquement peuvent faire référence les uns aux autres dans les limites de l’espace de noms. les objets pris en charge de manière dynamique ne peuvent pas faire référence mutuellement.

    Si nécessaire, utilisez les qualificateurs **HasClassRef** et **Classref** conjointement avec le type de référence d' **objet** pour référencer une classe.

    WMI prend en charge **l’utilisation** d’un point de référence de référence à une instance et l’autre référence d' **objet** à une classe. Dans ce cas, votre classe d’association décrirait une association qui lie des instances à des classes.

    L’exemple de code suivant décrit la syntaxe d’utilisation de **HasClassRef** et de **Classref** avec un type d' **objet** .

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    Dans l’exemple précédent, la référence **EP1** peut pointer vers les définitions de classe pour la classe **MyEndpoint** ou la classe **OtherContainer** . Notez que même si vous devez taper la classe de référence faiblement, vous ne pouvez pas taper le qualificateur **Classref** lui-même de façon faible ; cela réduirait gravement l’efficacité du moteur de requête WMI. Le typage faible consiste à créer une référence qui peut contenir n’importe quel type de données à l’aide du mot clé **Object** et du type de données **ref** . Pour pouvoir utiliser **HasClassRef**, vous devez définir les versions de qualificateur appropriées pour qu’elles se propagent à toutes les instances et sous-classes.

3.  Créez d’autres propriétés si nécessaire.

    L’exemple de code suivant montre que WMI ne prend actuellement pas en charge les classes d’association ayant moins ou plus de deux propriétés de référence.

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  Lorsque vous avez terminé, compilez votre code MOF avec le compilateur MOF.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

L’exemple de code à l’étape 3 définit la classe d’association **MyAssocClass** . La classe **MyAssocClass** définit une relation entre **ClassX** et **classy**. Les propriétés **PathToClassX** et **PathToClassY** contiennent des chemins d’accès aux instances des classes à associer. Le mot clé **ToInstance** est l’un des nombreux indicateurs de version que WMI définit pour fournir des informations sur l’utilisation d’un qualificateur. Le mot clé **ToInstance** indique que WMI doit propager le qualificateur d' **Association** à toutes les instances de la classe d’association. En vérifiant ce qualificateur d’instance, le logiciel client peut déterminer qu’une instance appartient à une classe d’association, sans avoir à récupérer la définition de classe pour rechercher le qualificateur d' **Association** . Pour plus d’informations, consultez [Description d’un qualificateur avec une version de qualificateur](describing-a-qualifier-with-a-qualifier-flavor.md) et des [références](references.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



