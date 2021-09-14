---
description: la Windows Installer peut effectuer une installation administrative d’une application ou d’un produit sur un réseau pour une utilisation par un groupe de travail.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Installation administrative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3958bdc81ee43cd1a36e0d464f3e77032b4c2d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092777"
---
# <a name="administrative-installation"></a>Installation administrative

la Windows Installer peut effectuer une installation administrative d’une application ou d’un produit sur un réseau pour une utilisation par un groupe de travail. Une installation d’administration installe une image source de l’application sur le réseau qui est similaire à une image source sur un CD-ROM. Les utilisateurs d’un groupe de travail qui ont accès à cette image administrative peuvent alors installer le produit à partir de cette source. Un utilisateur doit d’abord installer le produit à partir du réseau pour exécuter l’application. L’utilisateur peut choisir d’exécuter à partir de la source lors de son installation et le programme d’installation utilise la majeure partie du fichier du produit directement à partir du réseau.

Les administrateurs peuvent exécuter une installation d’administration à partir de la ligne de commande à l’aide de l' [option de ligne de commande](command-line-options.md)/a.

L' [action d’administration](admin-action.md) est l’action de niveau supérieur utilisée pour lancer une installation administrative. Quand cette action est exécutée, le programme d’installation appelle les actions dans les tables [AdminExecuteSequence](adminexecutesequence-table.md) et [AdminUISequence](adminuisequence-table.md) pour effectuer l’installation administrative.

La propriété [**AdminProperties**](adminproperties.md) est une liste délimitée par des points-virgules des propriétés définies au moment de l’installation d’une administration. Le programme d’installation utilise ces propriétés lors de l’installation après administration de l’application à partir de l’image administrative.

Les utilisateurs qui ne disposent pas d’un accès continu au réseau peuvent installer une application à partir d’une image administrative et, à temps, s’appuyer sur des médias, tels que des disques CD-ROM, comme source de sauvegarde. Dans ce cas, la longueur des noms de fichiers dans l’image administrative et sur le support doit correspondre. Les deux doivent utiliser des noms de fichiers longs, ou les deux doivent utiliser des noms de fichiers courts. Par exemple, un CD-ROM qui prend uniquement en charge les noms de fichiers courts peut fournir à la fois le média d’origine pour l’installation de l’image administrative et une source de sauvegarde.

Si la propriété [**SHORTFILENAMES**](shortfilenames.md) est définie au cours d’une installation d’administration, vous devrez peut-être la redéfinir à nouveau par un utilisateur en appliquant ensuite un correctif à l’image administrative. lorsque vous utilisez Windows Installer pour appliquer le correctif, le programme d’installation définit automatiquement la propriété **SHORTFILENAMES** si l’image administrative utilise des noms de fichiers courts.

Si un administrateur utilise un package dont la propriété [**Résumé du nombre de mots**](word-count-summary.md) est 2 ou 3 pour effectuer une installation administrative, les utilisateurs de l’image administrative ne peuvent pas réinstaller automatiquement à partir de la source du média d’origine. Si l’image administrative devient indisponible, les utilisateurs qui ont installé à partir de l’image administrative ne peuvent pas revenir au support d’origine.

L’application de [*transformations*](t-gly.md) pendant la création d’une image administrative n’a aucun effet valide. Pour mettre à la disposition d’un groupe de travail une version personnalisée d’un produit, appliquez la transformation lors de l’installation du produit à partir de l’image administrative.

Pendant une installation administrative, le programme d’installation crée une image source pour toutes les fonctionnalités du produit, à l’exception de celles avec 0 dans la colonne niveau de la [table des fonctionnalités](feature-table.md).

 

 



