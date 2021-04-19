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
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="78228-103">Limitations du modèle de script</span><span class="sxs-lookup"><span data-stu-id="78228-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="78228-104">Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="78228-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="78228-105">Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="78228-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="78228-106">Le modèle de script WIA (Windows Image Acquisition) expose un sous-ensemble de fonctionnalités WIA.</span><span class="sxs-lookup"><span data-stu-id="78228-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="78228-107">Le tableau suivant fournit une description des limitations du modèle de script.</span><span class="sxs-lookup"><span data-stu-id="78228-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="78228-108">Fonctionnalité WIA</span><span class="sxs-lookup"><span data-stu-id="78228-108">WIA Functionality</span></span>               | <span data-ttu-id="78228-109">Limitation du modèle de script</span><span class="sxs-lookup"><span data-stu-id="78228-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78228-110">Suppression de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="78228-110">Suppressing the user interface</span></span>  | <span data-ttu-id="78228-111">Impossible de supprimer l’interface utilisateur pour la définition des propriétés de périphérique/transfert.</span><span class="sxs-lookup"><span data-stu-id="78228-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="78228-112">Définition de propriétés</span><span class="sxs-lookup"><span data-stu-id="78228-112">Setting properties</span></span>              | <span data-ttu-id="78228-113">Impossible de définir (écrire) les propriétés d’un appareil ou d’un élément.</span><span class="sxs-lookup"><span data-stu-id="78228-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="78228-114">Inscription pour les événements de rappel</span><span class="sxs-lookup"><span data-stu-id="78228-114">Registering for callback events</span></span> | <span data-ttu-id="78228-115">Peut uniquement recevoir une notification pour trois événements spécifiés : [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)et [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="78228-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="78228-116">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="78228-116">Handling errors</span></span>                 | <span data-ttu-id="78228-117">Impossible de gérer les erreurs WIA.</span><span class="sxs-lookup"><span data-stu-id="78228-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 
