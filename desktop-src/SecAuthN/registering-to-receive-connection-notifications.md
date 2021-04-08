---
description: Après avoir créé une DLL pour recevoir des notifications de connexion, vous devez l’inscrire auprès du système.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Inscription pour recevoir des notifications de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756423"
---
# <a name="registering-to-receive-connection-notifications"></a><span data-ttu-id="ffe14-103">Inscription pour recevoir des notifications de connexion</span><span class="sxs-lookup"><span data-stu-id="ffe14-103">Registering to Receive Connection Notifications</span></span>

<span data-ttu-id="ffe14-104">Après avoir créé une DLL pour recevoir des notifications de connexion, vous devez l’inscrire auprès du système.</span><span class="sxs-lookup"><span data-stu-id="ffe14-104">After you have created a DLL to receive connection notifications, you must register it with the system.</span></span> <span data-ttu-id="ffe14-105">Pour ce faire, ajoutez une valeur de la valeur **\_ \_ SZ reg Expand** sous le</span><span class="sxs-lookup"><span data-stu-id="ffe14-105">You do this by adding a **REG\_EXPAND\_SZ** value under the</span></span>

<span data-ttu-id="ffe14-106">**HKEY \_ \_** \\  \\  \\  \\  \\ **Notifications** de contrôles CurrentControlSet du système d’ordinateur local NetworkProvider</span><span class="sxs-lookup"><span data-stu-id="ffe14-106">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="ffe14-107">application.</span><span class="sxs-lookup"><span data-stu-id="ffe14-107">key.</span></span> <span data-ttu-id="ffe14-108">Cette valeur spécifie le chemin d’accès à la DLL qui implémente l' [API de notification de connexion](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="ffe14-108">This value specifies the path to the DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span>

<span data-ttu-id="ffe14-109">La valeur peut avoir n’importe quel nom.</span><span class="sxs-lookup"><span data-stu-id="ffe14-109">The value can have any name.</span></span> <span data-ttu-id="ffe14-110">Toutes les valeurs sous la clé **Notify** sont traitées comme des chemins d’accès aux dll qui sont avertis des événements de connexion.</span><span class="sxs-lookup"><span data-stu-id="ffe14-110">All values under the **Notifyees** key are treated as paths to DLLs that are notified of connection events.</span></span> <span data-ttu-id="ffe14-111">Il est recommandé d’utiliser un nom qui identifie votre DLL.</span><span class="sxs-lookup"><span data-stu-id="ffe14-111">It is recommended that you use a name that identifies your DLL.</span></span> <span data-ttu-id="ffe14-112">Cela réduit le risque d’un conflit de noms avec d’autres applications de notification de connexion.</span><span class="sxs-lookup"><span data-stu-id="ffe14-112">This lessens the chance of a name conflict with other connection notification applications.</span></span>

<span data-ttu-id="ffe14-113">Pour plus d’informations sur la création d’une application qui reçoit des notifications de connexion, consultez [réception de notifications de connexion](receiving-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ffe14-113">For more information about how to create an application that receives connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md).</span></span>

 

 



