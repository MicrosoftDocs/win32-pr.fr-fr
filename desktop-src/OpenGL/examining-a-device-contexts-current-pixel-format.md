---
title: Examen d’un format de pixel actuel de contextes de périphérique
description: Utilisez les fonctions GetPixelFormat et DescribePixelFormat pour examiner le format de pixel actuel d’un contexte de périphérique, comme indiqué dans le fragment de code suivant.
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- OpenGL sur Windows, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea36f0f25b2cf76a6fb2ffb3159a4f2763a95af3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413681"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>Examen d’un format de pixel actuel de contextes de périphérique

Utilisez les fonctions [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) et [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) pour examiner le format de pixel actuel d’un contexte de périphérique, comme indiqué dans le fragment de code suivant.


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 




