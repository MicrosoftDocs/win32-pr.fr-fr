---
description: Après avoir déterminé les fonctionnalités d’un appareil téléphonique, une application doit ouvrir l’appareil pour pouvoir accéder aux fonctions sur ce téléphone.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: ouverture et fermeture des appareils Téléphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dacda3e98e96ed4a11334443a7b99b949e6d1b3823e42e1790c5a346b52dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012518"
---
# <a name="opening-and-closing-phone-devices"></a>ouverture et fermeture des appareils Téléphone

Après avoir déterminé les fonctionnalités d’un appareil téléphonique, une application doit ouvrir l’appareil pour pouvoir accéder aux fonctions sur ce téléphone. Une fois qu’un appareil téléphonique a été ouvert avec succès, l’application est retournée en tant que handle représentant le téléphone ouvert. Un appareil téléphonique peut être ouvert dans différents modes, fournissant ainsi un moyen structuré de partager un appareil téléphonique.

La fonction [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) ouvre l’appareil téléphonique spécifié pour permettre à l’application d’accéder aux fonctions sur le téléphone. Un appareil téléphonique est identifié comme **phoneOpen** à l’aide de son identificateur d’appareil, qui est passé comme paramètre *dwDeviceID* .

 

 



