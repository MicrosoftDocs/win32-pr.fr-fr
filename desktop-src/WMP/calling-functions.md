---
title: Appel de fonctions
description: Appel de fonctions
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Apparences du lecteur Windows Media, appel de fonctions dans JScript
- apparences, appeler des fonctions dans JScript
- appel de fonctions dans JScript
- Fichiers JScript pour les apparences, appels de fonctions
- Apparences du lecteur Windows Media, attribut scriptFile en JScript
- Skins, attribut scriptFile dans JScript
- attributs, scriptFile en JScript
- attribut scriptFile dans JScript
- Fichiers JScript pour les apparences, attribut scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507442"
---
# <a name="calling-functions"></a>Appel de fonctions

Si vous devez appeler plus de quelques lignes de code, vous pouvez charger un fichier de script à l’aide de l’attribut **scriptFile** de l’élément **View** , puis appeler les fonctions dans le script. Vous pouvez charger plusieurs fichiers par vue :


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Une fois les fichiers de script chargés, vous pouvez appeler les fonctions qu’ils contiennent à partir de la section de votre vue. Par exemple, pour appeler une fonction appelée *MyFunction* quand un utilisateur clique sur un événement, tapez ce qui suit :


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Si vous avez plusieurs vues, seules les fonctions des fichiers chargés dans l’affichage actuel sont disponibles pour le code XML et JScript s’exécutant avec la vue actuelle. Les fichiers chargés dans d’autres vues ne sont pas dans la portée de l’affichage actuel.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de JScript**](using-jscript.md)
</dt> </dl>

 

 




