---
description: Crée un fichier de catalogue non signé, qui contient les hachages d’un ensemble de fichiers, ainsi que les attributs associés de chaque fichier du jeu. Un fichier catalogue permet à l’utilisateur de signer un fichier (le catalogue) au lieu de signer de nombreux fichiers individuels.
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: Utilisation de MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127417661"
---
# <a name="using-makecat"></a>Utilisation de MakeCat

L’outil [MakeCat](makecat.md) crée un fichier catalogue non signé, qui contient les [*hachages*](../secgloss/h-gly.md) d’un ensemble de fichiers, ainsi que les attributs associés de chaque fichier du jeu. Un fichier catalogue permet à l’utilisateur de signer un fichier (le catalogue) au lieu de signer de nombreux fichiers individuels.

Une fois que le fichier de catalogue non signé est signé et transmis, le destinataire peut comparer les hachages des fichiers d’origine avec les hachages contenus dans le fichier catalogue et vérifier que les fichiers ne sont pas falsifiés.

Avant d’utiliser l’outil [MakeCat](makecat.md) , l’utilisateur doit préparer un fichier de définition de catalogue (. CDF) à l’aide de n’importe quel éditeur de texte. Le fichier. CDF contient la liste des fichiers et les attributs des fichiers à cataloguer (les spécifications sont répertoriées ci-dessous). L’outil MakeCat analyse le fichier. CDF, vérifie la liste des attributs de chaque fichier répertorié, ajoute les attributs répertoriés au catalogue lui-même, hache chacun des fichiers répertoriés et stocke les hachages de chaque fichier dans le fichier catalogue. Le hachage et les attributs de chaque fichier sont stockés séparément dans le catalogue. Ce fichier de catalogue peut ensuite être signé et transmis. Le destinataire peut ensuite comparer le hachage de chaque fichier au sein du catalogue avec le hachage des fichiers d’origine pour prouver que le contenu d’origine est exempt de falsification. MakeCat ne modifie pas le fichier. CDF.

Les exemples suivants utilisent des commandes [MakeCat](makecat.md) .

-   Générez un fichier catalogue à partir du fichier Good. CDF.

    **MakeCat-v Good. CDF**

Un fichier, Good. CDF, produit un fichier catalogue, Good.cat, en analysant les fichiers UnsignedPE.exe, UnsignedDOS.exe, Unsigned.cab, unsigned. Class et SignedPE.exe. Les fichiers analysés, ainsi que Good. CDF et les Good.cat récemment générés, se trouvent tous dans le même répertoire.

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> La dernière entrée dans le fichier. CDF doit toujours avoir un caractère de saut de ligne explicite à la fin de la ligne.

 

 

 
