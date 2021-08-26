---
title: Préparation de votre application pour l’Windows 64 bits
description: Il existe plusieurs fonctionnalités qui facilitent le développement d’applications qui s’exécutent à la fois sur les Windows 32 et 64 bits. La plupart de ces types de données, tels que les nouveaux types de données, sont décrits dans préparation à la Windows de 64 bits.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-bit toolkit 64-bit Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6c8d31b685e6f545aca4bdaac341fe25a3c96f458048808536899a8416120a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071619"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Préparation de votre application pour l’Windows 64 bits

Il existe plusieurs fonctionnalités qui facilitent le développement d’applications qui s’exécutent à la fois sur les Windows 32 et 64 bits. La plupart de ces types de données, tels que les nouveaux types de données, sont décrits dans [préparation à la Windows de 64 bits](getting-ready-for-64-bit-windows.md).

la boîte à outils 64 bits fournie avec le SDK Windows inclut un compilateur MIDL 64 bits, Midl.exe, pour générer des stubs 64 bits natifs, ainsi que des stubs 32 bits. Utilisez le commutateur **/env Win64** pour générer uniquement des stubs 64 bits. La valeur par défaut consiste à générer deux stubs qui s’exécutent sur les deux plateformes.

Notez que le MIDL 64 bits ne prend en charge que les modes d’optimisation [**/Oicf**](/windows/desktop/Midl/-oi) et [**/OS**](/windows/desktop/Midl/-os) .

 

 