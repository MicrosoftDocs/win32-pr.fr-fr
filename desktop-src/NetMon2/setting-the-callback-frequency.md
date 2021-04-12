---
description: Utilisez le code suivant pour définir la fréquence de rappel.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Définition de la fréquence de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318522"
---
# <a name="setting-the-callback-frequency"></a><span data-ttu-id="fb60b-103">Définition de la fréquence de rappel</span><span class="sxs-lookup"><span data-stu-id="fb60b-103">Setting the Callback Frequency</span></span>

<span data-ttu-id="fb60b-104">Utilisez le code suivant pour définir la fréquence de rappel :</span><span class="sxs-lookup"><span data-stu-id="fb60b-104">Use the following code to set the callback frequency:</span></span>

<span data-ttu-id="fb60b-105">**Valeur DWORD** Valeur = 1 ;</span><span class="sxs-lookup"><span data-stu-id="fb60b-105">**DWORD** Value = 1;</span></span>


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



<span data-ttu-id="fb60b-106">Ce fragment de code définit la fréquence de rappel sur 1 seconde (valeur minimale).</span><span class="sxs-lookup"><span data-stu-id="fb60b-106">This code fragment sets the callback frequency to 1 second (the minimum value).</span></span> <span data-ttu-id="fb60b-107">La valeur maximale doit être supérieure à 1.</span><span class="sxs-lookup"><span data-stu-id="fb60b-107">The maximum value must be much larger than 1.</span></span> <span data-ttu-id="fb60b-108">Si la mémoire tampon du fournisseur de paquets réseau (NPP) est pleine, le NPP rappelle le moniteur plus tôt.</span><span class="sxs-lookup"><span data-stu-id="fb60b-108">If the network packet provider (NPP) buffer is full, the NPP calls the monitor back sooner.</span></span>

 

 



