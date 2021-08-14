---
title: Entrée MouseWheel pour Windows 8.1
description: Entrée MouseWheel pour Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2285d2a0456376b01289ac7a4c2607117441384ebd13b0aaf0a162eac50fdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211382"
---
# <a name="mousewheel-input-for-windows-81"></a>Entrée MouseWheel pour Windows 8.1

## <a name="platform"></a>Plateforme

<dl> Clients-Windows 8.1  
serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

dans Windows 8.1, les événements mousewheel ne sont plus fournis en fonction du focus clavier, comme dans les versions précédentes de Windows. dans Windows 8.1, si la souris pointe sur une application du windows store, mousewheel sera remis à cette application. pour des raisons de compatibilité, toutefois, si la souris pointe sur une application de bureau, mousewheel continuera à être remis en fonction du focus clavier.

## <a name="manifestations"></a>Manifestations

Lorsque la souris pointe sur les applications du Windows Store, MouseWheel fait défiler tout le contenu applicable sans que l’utilisateur ne soit obligé de cliquer sur l’application du Windows Store. Cela s’applique également à l’écran d’accueil. cela permet de faire défiler par mousewheel une interaction plus simple dans Windows 8.1 que dans Windows 8.

## <a name="mitigation"></a>Limitation des risques

La plupart du temps, cette modification ne doit pas avoir d’impact sur les applications existantes. Si une application du Windows Store écoutait des événements MouseWheel uniquement après avoir inscrit un événement de clic de souris, cette application n’est pas susceptible de répondre à MouseWheel tant que l’utilisateur ne l’a pas activement cliqué. Par conséquent, l’inconvénient le plus probable est simplement qu’une application continue à fonctionner comme dans Windows 8. Pour les applications de bureau, le focus clavier ne donne plus à l’application un monopole sur l’entrée MouseWheel, mais cela n’entraîne pas non plus l’interruption de ces applications. Par conséquent, aucune atténuation à bref terme n’est requise.

## <a name="solution"></a>Solution

Les développeurs d’applications du Store doivent s’attendre à recevoir des événements MouseWheel sans événement de clic de souris précurseur. Ils ne doivent pas, par exemple, écouter les événements MouseWheel uniquement après l’inscription d’un clic de souris. De même, les applications de bureau ne doivent pas essayer de capturer les événements MouseWheel (par exemple, en définissant un raccordement de bas niveau) lorsqu’ils ont le focus clavier.

## <a name="tests"></a>Tests

les développeurs d’applications du Store doivent effectuer des tests sur Windows 8.1 pour vérifier que toutes les fonctionnalités de défilement fonctionnent chaque fois que la souris pointe sur l’application. les développeurs d’applications de bureau doivent effectuer des tests sur Windows 8.1 pour vérifier qu’ils ne capturent pas d’événements mousewheel (conformément aux instructions ci-dessus).

 

 




