---
description: Après avoir déterminé les fonctionnalités d’un appareil téléphonique, une application doit ouvrir l’appareil pour pouvoir accéder aux fonctions sur ce téléphone.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Ouverture et fermeture des appareils téléphoniques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544707"
---
# <a name="opening-and-closing-phone-devices"></a>Ouverture et fermeture des appareils téléphoniques

Après avoir déterminé les fonctionnalités d’un appareil téléphonique, une application doit ouvrir l’appareil pour pouvoir accéder aux fonctions sur ce téléphone. Une fois qu’un appareil téléphonique a été ouvert avec succès, l’application est retournée en tant que handle représentant le téléphone ouvert. Un appareil téléphonique peut être ouvert dans différents modes, fournissant ainsi un moyen structuré de partager un appareil téléphonique.

La fonction [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) ouvre l’appareil téléphonique spécifié pour permettre à l’application d’accéder aux fonctions sur le téléphone. Un appareil téléphonique est identifié comme **phoneOpen** à l’aide de son identificateur d’appareil, qui est passé comme paramètre *dwDeviceID* .

 

 



