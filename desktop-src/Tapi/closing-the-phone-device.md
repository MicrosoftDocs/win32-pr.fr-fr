---
description: La fonction phoneClose ferme l’appareil téléphonique spécifié.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Fermeture de l’appareil téléphonique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527232"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="05fdf-103">Fermeture de l’appareil téléphonique</span><span class="sxs-lookup"><span data-stu-id="05fdf-103">Closing the Phone Device</span></span>

<span data-ttu-id="05fdf-104">La fonction [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) ferme l’appareil téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="05fdf-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="05fdf-105">L’appareil téléphonique peut également être fermé de force une fois que l’utilisateur a modifié la configuration de ce téléphone ou de son pilote.</span><span class="sxs-lookup"><span data-stu-id="05fdf-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="05fdf-106">Si l’utilisateur souhaite que les modifications de configuration soient effectives immédiatement (par opposition à après le redémarrage du système suivant), et qu’elles affectent la vue actuelle de l’application de l’appareil (par exemple, une modification des fonctionnalités de l’appareil), un fournisseur de services peut forcer la fermeture de l’appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="05fdf-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="05fdf-107">Ces messages peuvent également être envoyés sans sollicitation à la suite de la récupération de l’appareil téléphonique d’une autre manière.</span><span class="sxs-lookup"><span data-stu-id="05fdf-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="05fdf-108">Une application doit donc être prête à gérer les messages de [**\_ fermeture de téléphone**](phone-close.md) non sollicités.</span><span class="sxs-lookup"><span data-stu-id="05fdf-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="05fdf-109">Au moment de la fermeture de l’appareil, les réponses asynchrones en suspens relatives à cet appareil sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="05fdf-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



