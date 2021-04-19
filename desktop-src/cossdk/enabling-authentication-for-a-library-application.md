---
description: Activation de l’authentification pour une application de bibliothèque
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Activation de l’authentification pour une application de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536102"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="bdae1-103">Activation de l’authentification pour une application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdae1-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="bdae1-104">Étant donné que les applications de bibliothèque COM+ sont hébergées par d’autres processus, leurs exigences de sécurité peuvent être différentes de celles des applications serveur.</span><span class="sxs-lookup"><span data-stu-id="bdae1-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="bdae1-105">Si l’application de bibliothèque doit être hébergée par un navigateur, il peut être nécessaire de recevoir des rappels non authentifiés.</span><span class="sxs-lookup"><span data-stu-id="bdae1-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="bdae1-106">Pour répondre à ce besoin, vous pouvez désactiver l’authentification afin que le processus d’hébergement n’effectue pas de vérifications de sécurité pour les appelants de l’application de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="bdae1-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="bdae1-107">Lorsque vous désactivez l’authentification, les appels à l’application de la bibliothèque ne sont pas authentifiés, mais tous les appels à ce dernier sont correctement effectués.</span><span class="sxs-lookup"><span data-stu-id="bdae1-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="bdae1-108">Pour plus d’informations, consultez [bibliothèque de sécurité des applications](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="bdae1-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="bdae1-109">**Pour activer (ou désactiver) l’authentification pour une application de bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="bdae1-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="bdae1-110">Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous activez ou désactivez l’authentification, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="bdae1-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="bdae1-111">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="bdae1-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="bdae1-112">Sous **authentification**, activez la case à cocher **activer l’authentification** pour activer l’authentification. la désactivation de la case à cocher désactive l’authentification.</span><span class="sxs-lookup"><span data-stu-id="bdae1-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="bdae1-113">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdae1-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdae1-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdae1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdae1-115">Définition d’un niveau d’authentification pour une application serveur</span><span class="sxs-lookup"><span data-stu-id="bdae1-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



