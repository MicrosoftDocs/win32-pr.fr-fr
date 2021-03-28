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
# <a name="information-device-contexts"></a>Contextes de périphérique d’information

Le contrôleur de l’information est utilisé pour récupérer les données de l’appareil par défaut. Par exemple, une application peut appeler la fonction [**Create**](/windows/desktop/api/Wingdi/nf-wingdi-createica) pour créer un contrôleur de contenu pour un modèle particulier d’imprimante, puis appeler les fonctions [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) et [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) pour récupérer les attributs de stylet ou de pinceau par défaut. Étant donné que le système peut récupérer des informations sur les appareils sans créer les structures normalement associées aux autres types de contextes de périphérique, un contrôleur de réseau d’informations implique une surcharge beaucoup moins importante et est créé beaucoup plus rapidement que les autres types. Une fois que l’application a terminé la récupération des données à l’aide d’un contrôleur de l’information, elle doit appeler la fonction [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .

 

 



