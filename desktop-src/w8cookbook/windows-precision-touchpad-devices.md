---
title: Périphériques Windows Precision Touchpad
description: Périphériques Windows Precision Touchpad
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104381368"
---
# <a name="windows-precision-touchpad-devices"></a>Périphériques Windows Precision Touchpad

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
</dl>

## <a name="description"></a>Description

Le pavé tactile Windows Precision est une nouvelle classe d’appareils d’entrée qui fournit des fonctionnalités d’entrée et de mouvement de pointeur à haute précision. Par défaut, ces appareils génèrent des messages de roulette de défilement très haute précision pour la consommation des applications de bureau.

## <a name="manifestations"></a>Manifestations

Les applications qui ne sont pas conçues pour gérer les messages de roulette de défilement de haute précision peuvent se dérouler ou ne pas faire défiler correctement.

## <a name="mitigation"></a>Limitation des risques

Les développeurs d’applications doivent examiner le delta de défilement dans les messages de roulette de défilement de la souris et modifier leurs applications en conséquence ; Toutefois, dans l’intervalle, une application peut désactiver les messages de roulette de défilement ultra-haute précision (Delta = 1) et choisir de recevoir des messages de roulette de défilement à haute précision (Delta = 40) ou des messages de roulette de défilement standard (Delta = 120).

## <a name="solution"></a>Solution

Si l’application est en mesure de gérer des messages de roulette de défilement de très haute précision, rien ne doit être effectué, car il s’agit du message par défaut envoyé par les pavés tactiles Windows Precision.

Si l’application est en charge de gérer les messages de roulette de défilement à haute précision, mais pas les messages de roulette à très haute précision, ajoutez ce qui suit au manifeste d’application :


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Si l’application n’est pas capable de gérer des messages de roulette de défilement haute précision ou des messages de roulette de très haute précision, ajoutez ce qui suit au manifeste d’application pour indiquer que les messages de la roulette de défilement standard sont souhaités :


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




