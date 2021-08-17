---
title: Fusion
description: La fusion associe les valeurs R, G, B et A d’un fragment à celles stockées dans le trame à l’emplacement correspondant.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline de traitement OpenGL, fusion
- fusion de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b38786d2320a646bd6cac096e535e4e1441df98522ac86a146836b929c0986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361433"
---
# <a name="blending"></a>Fusion

La fusion associe les valeurs R, G, B et A d’un fragment à celles stockées dans le trame à l’emplacement correspondant. La fusion, qui est exécutée uniquement en mode RVBA, dépend de la valeur alpha du fragment et de celle du pixel actuellement stocké correspondant ; elle peut également dépendre des valeurs RVB. Vous contrôlez la fusion avec [**glBlendFunc**](glblendfunc.md), avec lequel vous indiquez les facteurs de fusion source et de destination.

 

 




