---
description: Essayez-vous de trouver plus d’informations sur les objets Direct3D pendant le débogage ? Par exemple, la capture d’écran suivante montre ce que vous voyez généralement lorsque vous examinez une interface Direct3D dans la fenêtre Espion.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Activation des informations de débogage Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88851c144c2e651e920d870618f66a38028207bc5503f513f45fb053e16bd2e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730158"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Activation des informations de débogage Direct3D (Direct3D 9)

Essayez-vous de trouver plus d’informations sur les objets Direct3D pendant le débogage ? Par exemple, la capture d’écran suivante montre ce que vous voyez généralement lorsque vous examinez une interface Direct3D dans la fenêtre Espion.

![capture d’écran d’une interface Direct3D dans la fenêtre Espion](images/d3d-debug-info1.png)

Vous pouvez activer les objets de débogage de base afin qu’un objet mis en miroir qui contient toutes les propriétés de l’objet puisse être affiché dans la fenêtre Espion. Incluez simplement la \# définition suivante dans votre code avant le fichier d3d9. h :


```
#define D3D_DEBUG_INFO
```



Pour activer les informations de débogage, la \# définition doit être générée avant le fichier d3d9. h (tout programme qui utilise DXUT active automatiquement les \_ informations de débogage D3D \_ lorsque le programme est compilé pour le débogage). Si vous exécutez un exemple du kit de développement logiciel (SDK), vous pouvez le voir dans DXStdAfx. h (ce qui affecte tous les exemples C++). Vous devez également exécuter le runtime Direct3D de débogage (qui peut être activé à partir du panneau de configuration, si nécessaire).

Voici un exemple d’utilisation de l' [exemple BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Ajoutez la \# définition au fichier Dxstdafx. h avant la ligne 37.
2.  Générez un projet de débogage.
3.  Définir un point d’arrêt à la ligne 307 dans BasicHLSL. cpp
4.  Exécutez le débogueur.

La capture d’écran suivante montre le type d’informations détaillées que vous pouvez obtenir à propos d’un objet de texture Direct3D dans la fenêtre Espion.

![capture d’écran d’un objet de texture Direct3D dans la fenêtre Espion](images/d3d-debug-info2.png)

> [!Note]
>
> Les noms des propriétés de l’objet sont visibles et les valeurs sont correctes uniquement lorsque le runtime de débogage est activé. En cas d’exécution sur le runtime de vente au détail, les valeurs ne sont pas valides.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Utiliser la pile des appels pour le débogage étendu

Lorsque le débogage Direct3D est activé, vous pouvez également examiner une pile des appels chaque fois qu’un objet est créé. Cela rend votre application très lente, mais peut être utilisée pour vérifier les fuites de ressources. Pour écrire la pile des appels, affectez la valeur 1 à la clé de Registre suivante :


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



La génération de votre application avec le débogage activé vous donne accès à cette variable supplémentaire :


```
  LPCWSTR CreationCallStack;
```



Cette variable stockera la pile des appels chaque fois qu’un objet sera créé. Cela rend votre application très lente, mais peut être utilisée pour déboguer les fuites de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Astuces de programmation](programming-tips.md)
</dt> </dl>

 

 



