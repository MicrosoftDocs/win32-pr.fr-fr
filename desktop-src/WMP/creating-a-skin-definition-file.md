---
title: Création d’un fichier de définition d’apparence
description: Création d’un fichier de définition d’apparence
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Mobile Skins, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, création
- créer des apparences, à propos de
- création d’apparences, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674014"
---
# <a name="creating-a-skin-definition-file"></a>Création d’un fichier de définition d’apparence

Un fichier de définition d’apparence est un fichier texte qui définit une apparence et tous ses éléments composites. L’extension de nom de fichier doit être. skn.

Chaque fichier de définition d’apparence doit commencer par la ligne suivante, qui spécifie le numéro de version du fichier d’apparence. Le tableau suivant présente les versions du lecteur Windows Media et la ligne de code qui doit être utilisée pour identifier chacune d’elles dans un fichier de définition d’apparence. Bien que certains nombres dans les lignes de code ne soient pas conformes à vos attentes, ils sont corrects, comme indiqué dans le tableau suivant.



| Version du lecteur Windows Media | Première ligne du fichier de définition d’apparence |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Fichier d’apparence Pocket WMP v 1.0\]      |
| 1.2                          | \[Fichier d’apparence Pocket WMP v 1.2\]      |
| 7.0                          | \[Fichier d’apparence Pocket WMP v 2.0\]      |
| 7.1                          | \[Fichier d’apparence Pocket WMP v 8.0\]      |
| série 9                     | \[Fichier d’apparence Pocket WMP v 9.0.1\]    |
| Windows 10 Mobile                    | \[Fichier d’apparence Pocket WMP v 9.0.1\]    |
| 10,1 mobile                  | \[Fichier d’apparence Pocket WMP v 9.0.1\]    |



 

Le numéro de version 9.0.1 est destiné aux apparences créées spécifiquement pour le lecteur Windows Media série 9 ou version ultérieure. Les enveloppes ayant un numéro de version antérieure sont ouvertes par le lecteur Windows Media série 9 ou une version ultérieure en mode portrait, 96 points par pouce (DPI).

Le fichier de définition d’apparence est constitué de plusieurs sections. Chaque section définit une zone particulière de l’apparence. Les sections doivent être placées dans l’ordre suivant :

1.  Description
2.  Images bitmap
3.  Vidéo
4.  Boutons
5.  Statut
6.  Texte
7.  Chapiteau
8.  Trackbars

Chaque section commence par le nom de la section entre crochets, par exemple :


```C++
[ Bitmaps ]

```



> [!Note]  
> Votre fichier de définition d’apparence n’est pas analysé correctement sauf si vous incluez des espaces entre les crochets et le nom de la section.

 

Ensuite, une ou plusieurs lignes définissent des images, des boutons et ainsi de suite. Par exemple, une section bitmaps peut inclure les éléments suivants :


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Il n’est pas nécessaire d’aligner les valeurs dans les colonnes, mais cela permet d’améliorer la lisibilité de votre code. Pour plus d’informations sur chaque section du fichier de définition d’apparence, consultez la référence de l' [apparence](skin-reference.md).

> [!Note]  
> N’utilisez pas d’onglets n’importe où dans le fichier ; Utilisez à la place des espaces supplémentaires. C’est très important, car l’utilisation de la touche TAB lors de l’écriture ou de la modification de votre fichier de définition d’apparence entraîne l’échec de la totalité de l’apparence. Chaque ligne doit être terminée et ne peut pas se poursuivre sur une deuxième ligne. En outre, la région et les super valeurs sont dépréciées pour les apparences utilisées avec le lecteur Windows Media 10 mobile ou version ultérieure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichier de définition d’apparence**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





