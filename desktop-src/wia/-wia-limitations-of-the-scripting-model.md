---
description: 'En savoir plus sur : limitations du modèle de script'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitations du modèle de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4a1b2dc25c1ea73fd9d793e4d3de1bff7c8193b04aadbe00796ca4a021791886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208061"
---
# <a name="limitations-of-the-scripting-model"></a>Limitations du modèle de script

> [!Note]  
> ce système de script a été remplacé par la couche d’automatisation d’acquisition d’images Windows (WIA). consultez [Windows couche automatisation](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)de l’Acquisition d’images.

 

le modèle de script wia (Windows Image Acquisition) expose un sous-ensemble de fonctionnalités wia. Le tableau suivant fournit une description des limitations du modèle de script. 

| Fonctionnalité WIA               | Limitation du modèle de script                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suppression de l’interface utilisateur  | Impossible de supprimer l’interface utilisateur pour la définition des propriétés de périphérique/transfert.                                                                                                                                                                                               |
| Définition de propriétés              | Impossible de définir (écrire) les propriétés d’un appareil ou d’un élément.                                                                                                                                                                                                                        |
| Inscription pour les événements de rappel | Peut uniquement recevoir une notification pour trois événements spécifiés : [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)et [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md). |
| Gestion des erreurs                 | Impossible de gérer les erreurs WIA.                                                                                                                                                                                                                                                |



 

 

 
