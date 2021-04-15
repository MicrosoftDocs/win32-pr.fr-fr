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
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="5679e-103">Périphériques Windows Precision Touchpad</span><span class="sxs-lookup"><span data-stu-id="5679e-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="5679e-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="5679e-104">Platforms</span></span>

<dl> <span data-ttu-id="5679e-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5679e-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="5679e-106">Description</span><span class="sxs-lookup"><span data-stu-id="5679e-106">Description</span></span>

<span data-ttu-id="5679e-107">Le pavé tactile Windows Precision est une nouvelle classe d’appareils d’entrée qui fournit des fonctionnalités d’entrée et de mouvement de pointeur à haute précision.</span><span class="sxs-lookup"><span data-stu-id="5679e-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="5679e-108">Par défaut, ces appareils génèrent des messages de roulette de défilement très haute précision pour la consommation des applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="5679e-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="5679e-109">Manifestations</span><span class="sxs-lookup"><span data-stu-id="5679e-109">Manifestations</span></span>

<span data-ttu-id="5679e-110">Les applications qui ne sont pas conçues pour gérer les messages de roulette de défilement de haute précision peuvent se dérouler ou ne pas faire défiler correctement.</span><span class="sxs-lookup"><span data-stu-id="5679e-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="5679e-111">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="5679e-111">Mitigation</span></span>

<span data-ttu-id="5679e-112">Les développeurs d’applications doivent examiner le delta de défilement dans les messages de roulette de défilement de la souris et modifier leurs applications en conséquence ; Toutefois, dans l’intervalle, une application peut désactiver les messages de roulette de défilement ultra-haute précision (Delta = 1) et choisir de recevoir des messages de roulette de défilement à haute précision (Delta = 40) ou des messages de roulette de défilement standard (Delta = 120).</span><span class="sxs-lookup"><span data-stu-id="5679e-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="5679e-113">Solution</span><span class="sxs-lookup"><span data-stu-id="5679e-113">Solution</span></span>

<span data-ttu-id="5679e-114">Si l’application est en mesure de gérer des messages de roulette de défilement de très haute précision, rien ne doit être effectué, car il s’agit du message par défaut envoyé par les pavés tactiles Windows Precision.</span><span class="sxs-lookup"><span data-stu-id="5679e-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="5679e-115">Si l’application est en charge de gérer les messages de roulette de défilement à haute précision, mais pas les messages de roulette à très haute précision, ajoutez ce qui suit au manifeste d’application :</span><span class="sxs-lookup"><span data-stu-id="5679e-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="5679e-116">Si l’application n’est pas capable de gérer des messages de roulette de défilement haute précision ou des messages de roulette de très haute précision, ajoutez ce qui suit au manifeste d’application pour indiquer que les messages de la roulette de défilement standard sont souhaités :</span><span class="sxs-lookup"><span data-stu-id="5679e-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




