---
description: Les deux modes de mappage définis par l’application (MM \_ isotropes et mm \_ anisotrope) sont fournis pour les modes de mappage spécifiques à l’application.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Modes de mappage Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991292"
---
# <a name="application-defined-mapping-modes"></a>Modes de mappage Application-Defined

Les deux modes de mappage définis par l’application (MM \_ isotropes et mm \_ anisotrope) sont fournis pour les modes de mappage spécifiques à l’application. Le \_ mode mm isotrope garantit que les unités logiques de l’axe x et de l’axe y sont égales, tandis que le \_ mode anisotrope mm permet aux unités de différer. Une application de CAO ou de dessin peut tirer parti du \_ mode de mappage isotrope de mm, mais elle peut avoir besoin de spécifier des unités logiques qui correspondent aux incréments de l’échelle d’un ingénieur (1/64 pouces). Ces unités seraient difficiles à obtenir avec les modes de mappage prédéfinis (MM \_ HIENGLISH ou mm \_ HIMETRIC); Toutefois, elles peuvent être facilement obtenues en sélectionnant le \_ mode mm isotrope (ou mm \_ anisotrope). L’exemple suivant montre comment définir des unités logiques sur 1/64 pouce :


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



