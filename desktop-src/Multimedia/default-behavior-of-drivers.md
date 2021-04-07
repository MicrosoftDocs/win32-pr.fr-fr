---
title: Comportement par défaut des pilotes
description: Comportement par défaut des pilotes
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726564"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="7ae3e-103">Comportement par défaut des pilotes</span><span class="sxs-lookup"><span data-stu-id="7ae3e-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="7ae3e-104">Dans de nombreux cas, les spécifications de commande MCI définissent les valeurs et le comportement par défaut des pilotes d’un type d’appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="7ae3e-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="7ae3e-105">Étant donné que les périphériques multimédias peuvent avoir un large éventail de fonctionnalités (et limitations), il peut y avoir des zones de comportement non définies.</span><span class="sxs-lookup"><span data-stu-id="7ae3e-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="7ae3e-106">En outre, les pilotes peuvent gérer les exceptions différemment, en fonction des fonctionnalités de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ae3e-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="7ae3e-107">Par exemple, considérez les commandes suivantes envoyées à un pilote Wave-audio à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="7ae3e-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="7ae3e-108">La commande d' [**enregistrement**](record.md) renvoie une valeur « paramètre hors limites » et arrête la lecture démarrée par la commande de [**lecture**](play.md) précédente.</span><span class="sxs-lookup"><span data-stu-id="7ae3e-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="7ae3e-109">On peut s’attendre à ce que le pilote valide la commande d’enregistrement avant d’arrêter la lecture, mais le pilote arrête d’abord la lecture.</span><span class="sxs-lookup"><span data-stu-id="7ae3e-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 