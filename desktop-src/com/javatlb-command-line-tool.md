---
title: Utilitaire de Command-Line JavaTLB
description: Utilitaire de Command-Line JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675818"
---
# <a name="javatlb-command-line-tool"></a>Utilitaire de Command-Line JavaTLB

JavaTLB est un composant de Visual J++ 5,0. JavaTLB est une application de ligne de commande qui génère des fichiers de classe pour un objet COM. Les méthodes qui contiennent des types de données qui ne peuvent pas être représentés avec précision et en toute sécurité dans Java ne sont pas converties.

Contrairement à l' [Assistant bibliothèque de types Java](java-type-library-wizard.md), JavaTLB ne génère pas de fichier Résumé contenant les informations de la bibliothèque de types Java.

Pour générer des fichiers de classe Java pour un objet COM unique, à partir de l’invite de commandes, exécutez :

 *nom du fichier* JavaTLB

où *filename* est le nom du fichier qui contient la bibliothèque de types. Ce fichier peut avoir l’une des extensions de nom de fichier suivantes :. tlb,. olb,. ocx,. dll ou. exe.

Pour générer des fichiers de classe Java pour plusieurs objets COM, à partir de l’invite de commandes, exécutez :

**JavaTLB @ * * * TextFile*

où *TextFile* est le nom d’un fichier texte qui contient une liste des fichiers contenant les bibliothèques de types de l’objet com.

> [!Note]  
> Dans Visual J++ 6,0, l’outil en ligne de commande JavaTLB est remplacé par l' [outil JActiveX](jactivex-command-line-tool.md). Pour plus d’informations, consultez la documentation de Visual J++ 6,0.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en Java](translating-to-java.md)
</dt> </dl>

 

 




