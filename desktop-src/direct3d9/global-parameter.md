---
description: Chaque effet conforme à DXSAS doit définir au minimum un paramètre d’effet global unique avec la sémantique globale.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Paramètre global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516813"
---
# <a name="global-parameter"></a>Paramètre global

Chaque effet conforme à DXSAS doit définir au minimum un paramètre d’effet global unique avec la sémantique globale. Le paramètre global peut également utiliser une ou plusieurs annotations facultatives. La syntaxe est la suivante :


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



où :

-   NomVariable est un nom de variable de chaîne de texte ASCII spécifié par l’utilisateur.
-   SasGlobal est le mot clé sémantique qui identifie ce paramètre en tant que paramètre DXSAS global.
-   SasVersion est la seule annotation requise.
-   OptionalAnnotations peut inclure les éléments suivants :
    -   [SasEffectAuthor](#saseffectauthor)
    -   [SasEffectAuthoringSoftware](#saseffectauthoringsoftware)
    -   [SasEffectCategory](#saseffectcategory)
    -   [SasEffectCompany](#saseffectcompany)
    -   [SasEffectDescription](#saseffectdescription)
    -   [SasEffectHelp](#saseffecthelp)
    -   [SasEffectRevision](#saseffectrevision)

## <a name="sasversion"></a>SasVersion

La seule annotation requise est SasVersion. Elle est déclarée comme suit :


```
int3 SasVersion = { major, minor, revision };
```



où :

-   Major indique la version principale de DXSAS. Les versions majeures de DXSAS peuvent contenir des modifications de l’ensemble de la sémantique et des annotations définies. La sémantique et les annotations peuvent être ajoutées et supprimées et, en général, la compatibilité descendante avec les versions antérieures n’est pas garantie.
-   mineure indique la version mineure SAS. Les versions mineures de DXSAS peuvent inclure l’ajout de nouvelles sémantiques ou annotations. En outre, la sémantique et les annotations peuvent être marquées comme dépréciées dans la norme DXSAS. Les annotations et sémantiques déconseillées doivent toujours être prises en charge par les applications hôtes, mais elles peuvent émettre un diagnostic d’avertissement lorsqu’une telle sémantique ou annotation est utilisée. Les versions mineures sont à compatibilité descendante avec les versions précédentes.
-   la révision indique la révision DXSAS. Les révisions de DXSAS existent uniquement en tant que moyen de résoudre les bogues, de supprimer toute ambiguïté et d’affiner la norme. Les révisions du standard sont à compatibilité descendante avec les versions précédentes.

La version actuelle est 1.0.0. Il n’y a pas de valeur par défaut pour cette annotation.

## <a name="saseffectauthor"></a>SasEffectAuthor

Cela déclare la personne qui a créé l’effet. Elle est déclarée comme suit :


```
string SasEffectAuthor = "value";
```



où la valeur est une chaîne qui identifie l’auteur de l’effet. La valeur par défaut est une chaîne vide.

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

Cela déclare le logiciel sur lequel l’effet a été créé. Elle est déclarée comme suit :


```
string SasEffectAuthoringSoftware = "value";
```



où valeur est une chaîne qui identifie le logiciel de création d’effet. La valeur par défaut est une chaîne vide.

## <a name="saseffectcategory"></a>SasEffectCategory

Cela déclare la catégorie d’effet. Elle est déclarée comme suit :


```
string SasEffectCategory = "value";
```



où valeur est une chaîne qui identifie la catégorie d’effet. La valeur par défaut est une chaîne vide. La catégorie est exprimée via une valeur de type chemin d’accès utilisant la barre oblique comme séparateur. Les effets peuvent uniquement appartenir à une catégorie, car il n’existe aucune syntaxe pour exprimer l’inclusion dans plusieurs chemins d’accès au sein d’une seule valeur SasEffectCategory. La valeur de cette annotation n’est pas traitée comme respectant la casse par l’application hôte.

## <a name="saseffectcompany"></a>SasEffectCompany

Cela déclare la société qui a créé l’effet. Elle est déclarée comme suit :


```
string SasEffectCompany = "value";
```



où valeur est une chaîne qui identifie le nom de la société qui possède l’effet. La valeur par défaut est une chaîne vide.

## <a name="saseffectdescription"></a>SasEffectDescription

Cela décrit l’effet. Elle est déclarée comme suit :


```
string SasEffectDescription = "value";
```



où la valeur est une chaîne qui décrit l’effet. La valeur par défaut est une chaîne vide.

## <a name="saseffecthelp"></a>SasEffectHelp

Il s’agit d’une chaîne d’aide qui peut être affichée à l’utilisateur chaque fois que l’aide sur l’effet associé est demandée. Elle est déclarée comme suit :


```
string SasEffectHelp = "value";
```



où valeur est une chaîne qui peut être affichée si l’utilisateur demande de l’aide. La valeur par défaut est une chaîne vide.

## <a name="saseffectrevision"></a>SasEffectRevision

Cette annotation permet aux outils et aux utilisateurs d’enregistrer le numéro de révision du fichier d’effet associé. Par exemple, les utilisateurs peuvent insérer des mots clés appropriés dans la valeur de cette annotation pour appeler le remplacement de mot clé dans leur logiciel de contrôle de révision préféré. Elle est déclarée comme suit :


```
string SasEffectRevision = "value";
```



où la valeur est une chaîne qui identifie la révision de l’effet. La valeur par défaut est une chaîne vide.

## <a name="examples"></a>Exemples

Voici un exemple qui utilise uniquement l’annotation unique obligatoire :


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



Voici un exemple qui utilise l’annotation requise et plusieurs annotations facultatives :


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les annotations et sémantiques DirectX standard](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



