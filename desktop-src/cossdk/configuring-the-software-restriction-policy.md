---
description: Configuration de la stratégie de restriction logicielle
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configuration de la stratégie de restriction logicielle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033757"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="13739-103">Configuration de la stratégie de restriction logicielle</span><span class="sxs-lookup"><span data-stu-id="13739-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="13739-104">Lorsque vous définissez explicitement les niveaux de confiance de la stratégie de restriction logicielle d’une application COM+, vous remplacez les paramètres par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="13739-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="13739-105">Cela est souvent nécessaire pour les applications serveur COM+, car le niveau de confiance du système est défini de façon identique pour toutes les applications serveur (car elles s’exécutent toutes dans le même fichier, dllhost.exe).</span><span class="sxs-lookup"><span data-stu-id="13739-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="13739-106">Toutefois, lorsque vous définissez le niveau de confiance de la stratégie de restriction logicielle d’une application de bibliothèque COM+, vous affectez la configuration du système pour cette application.</span><span class="sxs-lookup"><span data-stu-id="13739-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="13739-107">Pour plus d’informations sur l’utilisation de la stratégie de restriction logicielle dans COM+, consultez [utilisation de la stratégie de restriction logicielle dans com+](using-the-software-restriction-policy-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="13739-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="13739-108">**Pour définir la stratégie de restriction logicielle**</span><span class="sxs-lookup"><span data-stu-id="13739-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="13739-109">Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous définissez la stratégie de restriction logicielle, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="13739-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="13739-110">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="13739-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="13739-111">Sous **stratégie de restriction logicielle**, activez la case à cocher **appliquer la stratégie de restriction logicielle** . Cela vous permet de définir le niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="13739-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="13739-112">Si vous désactivez la case à cocher, COM+ utilise la configuration du système de la stratégie de restriction logicielle pour l’application.</span><span class="sxs-lookup"><span data-stu-id="13739-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="13739-113">Cette case à cocher correspond à la propriété SRPEnabled de la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="13739-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="13739-114">Dans la zone **niveau de restriction** , sélectionnez le niveau approprié.</span><span class="sxs-lookup"><span data-stu-id="13739-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="13739-115">Cette zone de liste déroulante correspond à la propriété SRPTrustLevel de la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="13739-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="13739-116">Les niveaux sont les suivants, classés du moins au plus fiable :</span><span class="sxs-lookup"><span data-stu-id="13739-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="13739-117">**Interdit**.</span><span class="sxs-lookup"><span data-stu-id="13739-117">**Disallowed**.</span></span> <span data-ttu-id="13739-118">L’application n’est pas autorisée à utiliser les privilèges complets de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13739-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="13739-119">Les composants avec n’importe quel niveau de confiance peuvent être chargés dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="13739-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="13739-120">Non **restreint**.</span><span class="sxs-lookup"><span data-stu-id="13739-120">**Unrestricted**.</span></span> <span data-ttu-id="13739-121">L’application dispose d’un accès illimité aux privilèges de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13739-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="13739-122">Seuls les composants avec un niveau de confiance non restreint peuvent être chargés dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="13739-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="13739-123">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="13739-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13739-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13739-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13739-125">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="13739-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="13739-126">Activation de l’authentification pour une application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="13739-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="13739-127">Définition d’un niveau d’authentification pour une application serveur</span><span class="sxs-lookup"><span data-stu-id="13739-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="13739-128">Définition d’un niveau d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="13739-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



