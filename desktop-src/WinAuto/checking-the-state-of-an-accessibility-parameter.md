---
title: Vérification de l’état d’un paramètre d’accessibilité
description: Le fragment de code suivant utilise la fonction GetSystemMetrics pour vérifier le paramètre son texte. Si GetSystemMetrics retourne la valeur TRUE, l’application doit présenter toutes les informations importantes sous forme visuelle.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031331"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a><span data-ttu-id="80cb6-104">Vérification de l’état d’un paramètre d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="80cb6-104">Checking the State of an Accessibility Parameter</span></span>

<span data-ttu-id="80cb6-105">Le fragment de code suivant utilise la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) pour vérifier le paramètre son texte.</span><span class="sxs-lookup"><span data-stu-id="80cb6-105">The following code fragment uses the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to check the ShowSounds parameter.</span></span> <span data-ttu-id="80cb6-106">Si **GetSystemMetrics** retourne la **valeur true**, l’application doit présenter toutes les informations importantes sous forme visuelle.</span><span class="sxs-lookup"><span data-stu-id="80cb6-106">If **GetSystemMetrics** returns **TRUE**, the application should present all important information in visual form.</span></span>


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 