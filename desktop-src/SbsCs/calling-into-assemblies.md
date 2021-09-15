---
description: Lors d’un appel dans le entryPoints d’un assembly, il est recommandé d’utiliser le même contexte d’activation qui était actif lors de la recherche de l’assembly.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Appeler dans des assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238097"
---
# <a name="calling-into-assemblies"></a>Appeler dans des assemblys

Lors d’un appel dans le entryPoints d’un assembly, il est recommandé d’utiliser le même contexte d’activation qui était actif lors de la recherche de l’assembly. Au minimum, assurez-vous que le chargement du composant de l’assembly n’obtient pas accidentellement le contexte d’activation utilisé par votre application. La fuite du contexte d’activation entre les limites des DLL peut entraîner des dépendances inattendues. Ce n’est pas un problème si votre application compile la prise \_ en charge de l’isolation \_ activée, car dans ce cas, aucun contexte d’activation n’est actif par défaut. Si vous ne compilez pas avec la prise en charge de l’ISOLATION \_ \_ activée, vous devez activer le contexte d’activation **null** ou le même contexte d’activation qui a été utilisé pour charger l’assembly.

L’exemple suivant vérifie que la DLL hébergée s’exécute dans un contexte qu’elle reconnaît :

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



