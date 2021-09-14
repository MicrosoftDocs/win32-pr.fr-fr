---
title: Appel de fonctions
description: Appel de fonctions
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Lecteur Windows Media des apparences, appel de fonctions dans JScript
- apparences, appeler des fonctions dans JScript
- appel de fonctions dans JScript
- fichiers JScript pour les apparences, appels de fonctions
- Lecteur Windows Media skins, attribut scriptFile dans JScript
- Skins, attribut scriptFile dans JScript
- attributs, scriptFile dans JScript
- attribut scriptFile dans JScript
- fichiers JScript pour les apparences, attribut scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852675"
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
> si vous avez plusieurs vues, seules les fonctions des fichiers chargés dans l’affichage actuel sont disponibles dans le XML et JScript code s’exécutant avec la vue actuelle. Les fichiers chargés dans d’autres vues ne sont pas dans la portée de l’affichage actuel.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de JScript**](using-jscript.md)
</dt> </dl>

 

 




