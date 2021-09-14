---
title: Fusion
description: La fusion associe les valeurs R, G, B et A d’un fragment à celles stockées dans le trame à l’emplacement correspondant.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline de traitement OpenGL, fusion
- fusion de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110346"
---
# <a name="blending"></a>Fusion

La fusion associe les valeurs R, G, B et A d’un fragment à celles stockées dans le trame à l’emplacement correspondant. La fusion, qui est exécutée uniquement en mode RVBA, dépend de la valeur alpha du fragment et de celle du pixel actuellement stocké correspondant ; elle peut également dépendre des valeurs RVB. Vous contrôlez la fusion avec [**glBlendFunc**](glblendfunc.md), avec lequel vous indiquez les facteurs de fusion source et de destination.

 

 




