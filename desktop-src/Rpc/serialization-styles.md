---
title: Styles de sérialisation
description: Il existe trois styles que vous pouvez utiliser pour manipuler les descripteurs de sérialisation.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfaa7cd3198245441a27990d331bcd9f0bd0396b5075d9985b13da58012147d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925385"
---
# <a name="serialization-styles"></a>Styles de sérialisation

Il existe trois styles que vous pouvez utiliser pour manipuler les descripteurs de sérialisation. Celles-ci sont les suivantes :

-   [Sérialisation de mémoire tampon fixe](fixed-buffer-serialization.md)
-   [Sérialisation de mémoire tampon dynamique](dynamic-buffer-serialization.md)
-   [Sérialisation incrémentielle](incremental-serialization.md)

Quel que soit le style que vous utilisez, vous devez créer un handle de sérialisation, sérialiser les données, puis libérer le handle. Le style est défini lorsque votre programme crée le descripteur et définit la façon dont une mémoire tampon est manipulée. Le handle gère le contexte approprié associé à chacun des trois styles de sérialisation.

 

 




