---
description: Le contrôleur de l’information est utilisé pour récupérer les données de l’appareil par défaut.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contextes de périphérique d’information
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528324"
---
# <a name="information-device-contexts"></a><span data-ttu-id="b8a53-103">Contextes de périphérique d’information</span><span class="sxs-lookup"><span data-stu-id="b8a53-103">Information Device Contexts</span></span>

<span data-ttu-id="b8a53-104">Le contrôleur de l’information est utilisé pour récupérer les données de l’appareil par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a53-104">The information DC is used to retrieve default device data.</span></span> <span data-ttu-id="b8a53-105">Par exemple, une application peut appeler la fonction [**Create**](/windows/desktop/api/Wingdi/nf-wingdi-createica) pour créer un contrôleur de contenu pour un modèle particulier d’imprimante, puis appeler les fonctions [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) et [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) pour récupérer les attributs de stylet ou de pinceau par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8a53-105">For example, an application can call the [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) function to create an information DC for a particular model of printer and then call the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions to retrieve the default pen or brush attributes.</span></span> <span data-ttu-id="b8a53-106">Étant donné que le système peut récupérer des informations sur les appareils sans créer les structures normalement associées aux autres types de contextes de périphérique, un contrôleur de réseau d’informations implique une surcharge beaucoup moins importante et est créé beaucoup plus rapidement que les autres types.</span><span class="sxs-lookup"><span data-stu-id="b8a53-106">Because the system can retrieve device information without creating the structures normally associated with the other types of device contexts, an information DC involves far less overhead and is created significantly faster than any of the other types.</span></span> <span data-ttu-id="b8a53-107">Une fois que l’application a terminé la récupération des données à l’aide d’un contrôleur de l’information, elle doit appeler la fonction [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="b8a53-107">After an application finishes retrieving data by using an information DC, it must call the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span>

 

 



