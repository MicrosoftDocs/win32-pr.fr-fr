---
title: Styles de sérialisation
description: Il existe trois styles que vous pouvez utiliser pour manipuler les descripteurs de sérialisation.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380149"
---
# <a name="serialization-styles"></a>Styles de sérialisation

Il existe trois styles que vous pouvez utiliser pour manipuler les descripteurs de sérialisation. Celles-ci sont les suivantes :

-   [Sérialisation de mémoire tampon fixe](fixed-buffer-serialization.md)
-   [Sérialisation de mémoire tampon dynamique](dynamic-buffer-serialization.md)
-   [Sérialisation incrémentielle](incremental-serialization.md)

Quel que soit le style que vous utilisez, vous devez créer un handle de sérialisation, sérialiser les données, puis libérer le handle. Le style est défini lorsque votre programme crée le descripteur et définit la façon dont une mémoire tampon est manipulée. Le handle gère le contexte approprié associé à chacun des trois styles de sérialisation.

 

 




