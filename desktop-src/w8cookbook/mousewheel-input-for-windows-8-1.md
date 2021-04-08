---
title: Entrée MouseWheel pour Windows 8.1
description: Entrée MouseWheel pour Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839694"
---
# <a name="mousewheel-input-for-windows-81"></a>Entrée MouseWheel pour Windows 8.1

## <a name="platform"></a>Plateforme

<dl> Clients-Windows 8.1  
Serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Dans Windows 8.1, les événements MouseWheel ne sont plus fournis en fonction du focus clavier, comme dans les versions précédentes de Windows. Dans Windows 8.1, si la souris pointe sur une application du Windows Store, MouseWheel sera remis à cette application ; Toutefois, à des fins de compatibilité, si la souris pointe sur une application de bureau, MouseWheel continuera à être remis en fonction du focus clavier.

## <a name="manifestations"></a>Manifestations

Lorsque la souris pointe sur les applications du Windows Store, MouseWheel fait défiler tout le contenu applicable sans que l’utilisateur ne soit obligé de cliquer sur l’application du Windows Store. Cela s’applique également à l’écran d’accueil. Cela permet de faire défiler par MouseWheel une interaction plus simple dans Windows 8.1 que dans Windows 8.

## <a name="mitigation"></a>Limitation des risques

La plupart du temps, cette modification ne doit pas avoir d’impact sur les applications existantes. Si une application du Windows Store écoutait des événements MouseWheel uniquement après avoir inscrit un événement de clic de souris, cette application n’est pas susceptible de répondre à MouseWheel tant que l’utilisateur ne l’a pas activement cliqué. Par conséquent, l’inconvénient le plus probable est simplement qu’une application continue à fonctionner comme dans Windows 8. Pour les applications de bureau, le focus clavier ne donne plus à l’application un monopole sur l’entrée MouseWheel, mais cela n’entraîne pas non plus l’interruption de ces applications. Par conséquent, aucune atténuation à bref terme n’est requise.

## <a name="solution"></a>Solution

Les développeurs d’applications du Store doivent s’attendre à recevoir des événements MouseWheel sans événement de clic de souris précurseur. Ils ne doivent pas, par exemple, écouter les événements MouseWheel uniquement après l’inscription d’un clic de souris. De même, les applications de bureau ne doivent pas essayer de capturer les événements MouseWheel (par exemple, en définissant un raccordement de bas niveau) lorsqu’ils ont le focus clavier.

## <a name="tests"></a>Tests

Les développeurs d’applications du Store doivent effectuer des tests sur Windows 8.1 pour vérifier que toutes les fonctionnalités de défilement fonctionnent chaque fois que la souris pointe sur l’application. Les développeurs d’applications de bureau doivent effectuer des tests sur Windows 8.1 pour vérifier qu’ils ne capturent pas d’événements MouseWheel (conformément aux instructions ci-dessus).

 

 




