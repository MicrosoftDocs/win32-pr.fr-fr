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
ms.openlocfilehash: 49a6d61634475c3b921428529df69113c921b8c5bff8d1a65d5b08931a670fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037569"
---
# <a name="querying-auxiliary-audio-devices"></a>Interrogation des périphériques audio auxiliaires

Tous les systèmes multimédias n’ont pas de prise en charge audio auxiliaire. Vous pouvez utiliser la fonction [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) pour déterminer le nombre d’appareils auxiliaires contrôlable présents dans un système.

Pour obtenir des informations sur un périphérique audio auxiliaire particulier, utilisez la fonction [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) . Cette fonction remplit une structure [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) avec des informations sur les fonctionnalités d’un appareil spécifié. Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote d’appareil.

 

 