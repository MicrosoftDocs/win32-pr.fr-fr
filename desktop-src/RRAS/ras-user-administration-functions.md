---
title: Fonctions d’administration d’utilisateur RAS
description: Utilisez les fonctions suivantes pour gérer les utilisateurs d’accès à distance
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463586"
---
# <a name="ras-user-administration-functions"></a><span data-ttu-id="c74f7-103">Fonctions d’administration d’utilisateur RAS</span><span class="sxs-lookup"><span data-stu-id="c74f7-103">RAS User Administration Functions</span></span>

<span data-ttu-id="c74f7-104">Utilisez les fonctions suivantes pour gérer les utilisateurs d’accès à distance :</span><span class="sxs-lookup"><span data-stu-id="c74f7-104">Use the following functions to manage dial-up users:</span></span>

-   [<span data-ttu-id="c74f7-105">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="c74f7-105">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [<span data-ttu-id="c74f7-106">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="c74f7-106">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [<span data-ttu-id="c74f7-107">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="c74f7-107">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [<span data-ttu-id="c74f7-108">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="c74f7-108">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

<span data-ttu-id="c74f7-109">Pour obtenir la liste des utilisateurs actuels sur un domaine particulier, utilisez la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) .</span><span class="sxs-lookup"><span data-stu-id="c74f7-109">To obtain a list of current users on a particular domain, use the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function.</span></span> <span data-ttu-id="c74f7-110">Le prototype de cette fonction se trouve dans le fichier d’en-tête lmaccess. h.</span><span class="sxs-lookup"><span data-stu-id="c74f7-110">The prototype for this function is in the lmaccess.h header file.</span></span>

 

 