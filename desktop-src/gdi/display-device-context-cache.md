---
description: Le système gère un cache de l’affichage des contextes de périphérique qu’il utilise pour les contextes de périphérique communs, parents et de fenêtre.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Afficher le cache du contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991265"
---
# <a name="display-device-context-cache"></a><span data-ttu-id="0fc80-103">Afficher le cache du contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="0fc80-103">Display Device Context Cache</span></span>

<span data-ttu-id="0fc80-104">Le système gère un cache de l’affichage des contextes de périphérique qu’il utilise pour les contextes de périphérique communs, parents et de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0fc80-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="0fc80-105">Le système récupère un contexte de périphérique (Device Context) à partir du cache chaque fois qu’une application appelle la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . le système retourne le contrôleur de réseau dans le cache lorsque l’application appelle ensuite la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) ou [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="0fc80-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="0fc80-106">Il n’existe aucune limite prédéterminée sur la quantité de contextes de périphérique qu’un cache peut contenir ; le système crée un contexte de périphérique d’affichage pour le cache si aucun n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="0fc80-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="0fc80-107">Dans ce contexte, une application peut avoir plus de cinq contextes de périphérique actifs du cache à la fois.</span><span class="sxs-lookup"><span data-stu-id="0fc80-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="0fc80-108">Toutefois, l’application doit continuer à libérer ces contextes de périphérique après utilisation.</span><span class="sxs-lookup"><span data-stu-id="0fc80-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="0fc80-109">Étant donné que de nouveaux contextes de périphérique d’affichage pour le cache sont alloués dans l’espace du tas de l’application, le fait de ne pas libérer les contextes de périphérique finit par consommer tout l’espace disponible du tas.</span><span class="sxs-lookup"><span data-stu-id="0fc80-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="0fc80-110">Le système indique cet échec en renvoyant une erreur lorsqu’il ne peut pas allouer de l’espace pour le nouveau contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0fc80-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="0fc80-111">D’autres fonctions non liées au cache peuvent également renvoyer des erreurs.</span><span class="sxs-lookup"><span data-stu-id="0fc80-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 



