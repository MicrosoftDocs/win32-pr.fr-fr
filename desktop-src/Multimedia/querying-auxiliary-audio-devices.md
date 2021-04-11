---
title: Interrogation des périphériques audio auxiliaires
description: Interrogation des périphériques audio auxiliaires
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- audio Wave, interrogation des périphériques audio auxiliaires
- audio auxiliaire, interrogation des appareils
- interface audio auxiliaire
- périphériques audio auxiliaires, interrogation
- interrogation des périphériques audio auxiliaires
- audio auxiliaire, interface
- audio auxiliaire, appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031121"
---
# <a name="querying-auxiliary-audio-devices"></a>Interrogation des périphériques audio auxiliaires

Tous les systèmes multimédias n’ont pas de prise en charge audio auxiliaire. Vous pouvez utiliser la fonction [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) pour déterminer le nombre d’appareils auxiliaires contrôlable présents dans un système.

Pour obtenir des informations sur un périphérique audio auxiliaire particulier, utilisez la fonction [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) . Cette fonction remplit une structure [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) avec des informations sur les fonctionnalités d’un appareil spécifié. Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote d’appareil.

 

 