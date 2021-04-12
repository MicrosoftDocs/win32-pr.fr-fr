---
title: Préparation de votre application pour Windows 64 bits
description: Il existe plusieurs fonctionnalités qui facilitent le développement d’applications qui s’exécutent à la fois sur les versions 32 et 64 bits de Windows. La plupart de ces types de données, tels que les nouveaux types de données, sont décrits dans préparation pour Windows 64 bits.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-bit Toolkit, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199348"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Préparation de votre application pour Windows 64 bits

Il existe plusieurs fonctionnalités qui facilitent le développement d’applications qui s’exécutent à la fois sur les versions 32 et 64 bits de Windows. La plupart de ces types de données, tels que les nouveaux types de données, sont décrits dans [préparation pour Windows 64 bits](getting-ready-for-64-bit-windows.md).

La boîte à outils 64 bits fournie avec le SDK Windows inclut un compilateur MIDL 64 bits, Midl.exe, pour générer des stubs 64 bits natifs, ainsi que des stubs 32 bits. Utilisez le commutateur **/env Win64** pour générer uniquement des stubs 64 bits. La valeur par défaut consiste à générer deux stubs qui s’exécutent sur les deux plateformes.

Notez que le MIDL 64 bits ne prend en charge que les modes d’optimisation [**/Oicf**](/windows/desktop/Midl/-oi) et [**/OS**](/windows/desktop/Midl/-os) .

 

 