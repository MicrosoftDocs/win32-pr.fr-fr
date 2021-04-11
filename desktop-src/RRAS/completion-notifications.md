---
title: Notifications de saisie semi-automatique
description: Le gestionnaire de connexions d’accès à distance continue les notifications de progression jusqu’à ce que l’opération de connexion soit terminée.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029251"
---
# <a name="completion-notifications"></a><span data-ttu-id="4f8be-103">Notifications de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="4f8be-103">Completion Notifications</span></span>

<span data-ttu-id="4f8be-104">Le gestionnaire de connexions d’accès à distance continue les notifications de progression jusqu’à ce que l’opération de connexion soit terminée.</span><span class="sxs-lookup"><span data-stu-id="4f8be-104">The Remote Access Connection Manager continues progress notifications until the connection operation has been completed.</span></span> <span data-ttu-id="4f8be-105">Cela se produit dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f8be-105">This occurs in the following situations:</span></span>

-   <span data-ttu-id="4f8be-106">Le gestionnaire reçoit une \_ notification RASCS Connected ou RASCS \_ Disconnected.</span><span class="sxs-lookup"><span data-stu-id="4f8be-106">The handler receives a RASCS\_Connected, or RASCS\_Disconnected notification.</span></span> <span data-ttu-id="4f8be-107">L’application cliente RAS peut quitter sans rompre la connexion établie.</span><span class="sxs-lookup"><span data-stu-id="4f8be-107">The RAS client application can exit without breaking any established connection.</span></span>
-   <span data-ttu-id="4f8be-108">Une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="4f8be-108">An error occurs.</span></span> <span data-ttu-id="4f8be-109">Le gestionnaire reçoit une notification indiquant l’erreur et l’état de la connexion lorsque l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4f8be-109">The handler receives a notification indicating the error and the connection state when the error occurred.</span></span> <span data-ttu-id="4f8be-110">L’application cliente RAS peut se fermer.</span><span class="sxs-lookup"><span data-stu-id="4f8be-110">The RAS client application can exit.</span></span>

<span data-ttu-id="4f8be-111">L’application cliente RAS ne doit pas supposer que l’opération de connexion est terminée après l’appel de [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span><span class="sxs-lookup"><span data-stu-id="4f8be-111">The RAS client application should not assume the connection operation is complete after calling [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa).</span></span> <span data-ttu-id="4f8be-112">Il doit attendre l’une des conditions précédentes avant de quitter.</span><span class="sxs-lookup"><span data-stu-id="4f8be-112">It should wait for one of the preceding conditions before exiting.</span></span>

 

 




