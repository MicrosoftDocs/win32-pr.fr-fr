---
title: Compilation du balisage du ruban
description: pour que l’infrastructure du ruban Windows utilise le fichier de balisage du ruban, le fichier de balisage doit être compilé dans un fichier de ressources au format binaire.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows Ruban, compiler le balisage
- Ruban, compiler le balisage
- Windows Ruban, flux de travail du compilateur
- Ruban, flux de travail du compilateur
- Windows Ruban, compilateur de commandes d’interface utilisateur (UICC.exe)
- Ruban, compilateur de commandes d’interface utilisateur (UICC.exe)
- Compilateur de commandes d’interface utilisateur (UICC.exe)
- UICC.exe (compilateur de commandes d’interface utilisateur)
- compilation Windows balisage du ruban
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85534a05b3bde59cc2ec0eec482d8c3b47e898d39ad988c595fbac33eb5e9f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932562"
---
# <a name="compiling-ribbon-markup"></a>Compilation du balisage du ruban

pour que l’infrastructure du ruban Windows utilise le fichier de [balisage du ruban](windowsribbon-schema.md) , le fichier de balisage doit être compilé dans un fichier de ressources au format binaire. un compilateur de balisage dédié, le compilateur de commandes d’interface utilisateur (UICC), est inclus dans le kit de développement logiciel (SDK) Windows (7,0 ou version ultérieure) à cet effet. En plus de compiler la version binaire du balisage, UICC génère un fichier d’en-tête de définition d’ID (. h) qui expose tous les éléments de balisage à l’application hôte du ruban et un fichier de ressources (. RC) qui est utilisé pour lier des ressources d’image et de chaîne à l’application hôte au moment de la génération.

-   [Flux de travail du compilateur](#compiler-workflow)
-   [Syntaxe de la ligne de commande](#command-line-syntax)
    -   [Arguments et options](#arguments-and-options)
    -   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="compiler-workflow"></a>Flux de travail du compilateur

Le flux de travail du compilateur de balisage du ruban est illustré dans le diagramme suivant.

![Diagramme montrant le flux de travail du compilateur de balisage du ruban.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Syntaxe de ligne de commande

La syntaxe de la ligne de commande pour le compilateur de balisage du ruban est illustrée dans l’exemple suivant.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Arguments et options

Les arguments et les options de cet outil sont décrits dans le tableau suivant.

> [!Note]  
> Les options de ligne de commande indiquées doivent être spécifiées dans l’ordre indiqué.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/Header<headerFile></td>
<td>Générez un fichier d’en-tête appelé <headerFile> qui contient les symboles de ressource ID de commande de balisage. En cas d’omission, un fichier d’en-tête n’est pas généré.</td>
</tr>
<tr class="even">
<td>/res<resourceFile></td>
<td>Générez un fichier de ressources appelé <resourceFile> qui lie toutes les ressources d’image et de chaîne, le fichier de balisage binaire et le fichier d’en-tête à l’application hôte au moment de la génération. En cas d’omission, un fichier de ressources n’est pas généré.</td>
</tr>
<tr class="odd">
<td>/Name<ribbonName></td>
<td>Nom de la ressource pour le fichier de balisage binaire qui est enregistré dans le <resourceFile> . La valeur par défaut est APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtrer les messages d’événement en fonction de leur gravité. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Messages d'erreur uniquement.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Messages d’erreur et d’avertissement uniquement.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Par défaut. <br/> Messages d’erreur, d’avertissement et d’information.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser le compilateur de balisage du ruban pour générer un ensemble classique de fichiers de ressources pour une application de ruban.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](windowsribbon-schema.md)
</dt> <dt>

[Création d’une application de ruban](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





