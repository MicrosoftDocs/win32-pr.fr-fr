---
description: L’énumération des ressources fournit une vue étroite et précise de l’activité d’instrumentation qui a lieu lorsqu’une application est en cours d’exécution.
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: À propos de l’énumération des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513117"
---
# <a name="about-resource-enumeration"></a>À propos de l’énumération des ressources

L’énumération des ressources fournit une vue étroite et précise de l’activité d’instrumentation qui a lieu lorsqu’une application est en cours d’exécution. Les informations d’instrumentation peuvent être abstraites et classées sous la forme d’un ensemble d’éléments spécifiques au processus dans le cadre du processus de débogage.

Les outils, tels que les débogueurs, requièrent souvent un accès aux informations d’instrumentation, mais il est possible qu’il ne soit pas disponible. Pour résoudre ce problème, la fonction [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) extrait ce type d’informations à partir d’applications afin de fournir de meilleures informations de contexte pour le problème en cours de débogage.

 

 



