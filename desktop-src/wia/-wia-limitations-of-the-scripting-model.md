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
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515668"
---
# <a name="limitations-of-the-scripting-model"></a>Limitations du modèle de script

> [!Note]  
> Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA). Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Le modèle de script WIA (Windows Image Acquisition) expose un sous-ensemble de fonctionnalités WIA. Le tableau suivant fournit une description des limitations du modèle de script. 

| Fonctionnalité WIA               | Limitation du modèle de script                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suppression de l’interface utilisateur  | Impossible de supprimer l’interface utilisateur pour la définition des propriétés de périphérique/transfert.                                                                                                                                                                                               |
| Définition de propriétés              | Impossible de définir (écrire) les propriétés d’un appareil ou d’un élément.                                                                                                                                                                                                                        |
| Inscription pour les événements de rappel | Peut uniquement recevoir une notification pour trois événements spécifiés : [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)et [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md). |
| Gestion des erreurs                 | Impossible de gérer les erreurs WIA.                                                                                                                                                                                                                                                |



 

 

 
