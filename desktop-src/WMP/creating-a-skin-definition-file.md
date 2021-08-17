---
title: Création d’un fichier de définition d’apparence
description: Création d’un fichier de définition d’apparence
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Lecteur Windows Media Skins mobiles, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, création
- créer des apparences, à propos de
- création d’apparences, Lecteur Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bb18289a8ed124c820e983c37ccc9fff60c5c1c2b0794e4964a8e170c84909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341599"
---
# <a name="creating-a-skin-definition-file"></a>Création d’un fichier de définition d’apparence

Un fichier de définition d’apparence est un fichier texte qui définit une apparence et tous ses éléments composites. L’extension de nom de fichier doit être. skn.

Chaque fichier de définition d’apparence doit commencer par la ligne suivante, qui spécifie le numéro de version du fichier d’apparence. le tableau suivant répertorie les versions Lecteur Windows Media et la ligne de code qui doivent être utilisées pour identifier chacune d’elles dans un fichier de définition d’apparence. Bien que certains nombres dans les lignes de code ne soient pas conformes à vos attentes, ils sont corrects, comme indiqué dans le tableau suivant.



| version de Lecteur Windows Media | Première ligne du fichier de définition d’apparence |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Fichier d’apparence Pocket WMP v 1.0\]      |
| 1.2                          | \[Fichier d’apparence Pocket WMP v 1.2\]      |
| 7.0                          | \[Fichier d’apparence Pocket WMP v 2.0\]      |
| 7.1                          | \[Fichier d’apparence Pocket WMP v 8.0\]      |
| série 9                     | \[Fichier d’apparence Pocket WMP v 9.0.1\]    |
| Windows 10 Mobile                    | \[Fichier d’apparence Pocket WMP v 9.0.1\]    |
| 10,1 mobile                  | \[Fichier d’apparence Pocket WMP v 9.0.1\]    |



 

le numéro de version 9.0.1 est destiné aux apparences créées spécifiquement pour la série Lecteur Windows Media 9 ou version ultérieure. les enveloppes ayant un numéro de version antérieure sont ouvertes par Lecteur Windows Media série 9 ou ultérieurement en mode portrait, 96 points par pouce (DPI).

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
> N’utilisez pas d’onglets n’importe où dans le fichier ; Utilisez à la place des espaces supplémentaires. C’est très important, car l’utilisation de la touche TAB lors de l’écriture ou de la modification de votre fichier de définition d’apparence entraîne l’échec de la totalité de l’apparence. Chaque ligne doit être terminée et ne peut pas se poursuivre sur une deuxième ligne. en outre, la région et les Super valeurs sont dépréciées pour les habillages utilisés avec Lecteur Windows Media 10 Mobile ou version ultérieure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichier de définition d’apparence**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





