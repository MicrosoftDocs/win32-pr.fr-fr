---
description: Pour utiliser la sécurité basée sur les rôles dans votre application COM+, vous devez d’abord activer la vérification d’autorisation basée sur les rôles pour l’application.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Activation de la vérification d’autorisation Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033722"
---
# <a name="enabling-role-based-authorization-checking"></a><span data-ttu-id="c42c9-103">Activation de la vérification d’autorisation Role-Based</span><span class="sxs-lookup"><span data-stu-id="c42c9-103">Enabling Role-Based Authorization Checking</span></span>

<span data-ttu-id="c42c9-104">Pour utiliser la sécurité basée sur les rôles dans votre application COM+, vous devez d’abord activer la vérification d’autorisation basée sur les rôles pour l’application.</span><span class="sxs-lookup"><span data-stu-id="c42c9-104">To use role-based security in your COM+ application, you must first enable role-based authorization checking for the application.</span></span> <span data-ttu-id="c42c9-105">Cela garantit que les utilisateurs qui accèdent à l’application sont vérifiés pour le rôle auquel ils appartiennent avant qu’ils soient autorisés à faire quoi que ce soit dans l’application.</span><span class="sxs-lookup"><span data-stu-id="c42c9-105">This ensures that users who are accessing the application are checked for the role they belong to before they are authorized to do anything in the application.</span></span> <span data-ttu-id="c42c9-106">Si la vérification de l’autorisation basée sur les rôles n’est pas activée, la sécurité basée sur les rôles pour l’application n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="c42c9-106">If role-based authorization checking is not enabled, role-based security for the application is not used.</span></span>

<span data-ttu-id="c42c9-107">**Pour activer la vérification de l’autorisation basée sur les rôles**</span><span class="sxs-lookup"><span data-stu-id="c42c9-107">**To enable role-based authorization checking**</span></span>

1.  <span data-ttu-id="c42c9-108">Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous activez la vérification d’autorisation basée sur les rôles, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="c42c9-108">Right-click the COM+ application for which you are enabling role-based authorization checking, and then click **Properties**.</span></span>

2.  <span data-ttu-id="c42c9-109">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="c42c9-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="c42c9-110">Sous **autorisation**, activez la case à cocher **appliquer les vérifications d’accès pour cette application** . Si vous désactivez la case à cocher, la sécurité basée sur les rôles n’est pas utilisée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="c42c9-110">Under **Authorization**, select the **Enforce access checks for this application** check box; clearing the check box means that role-based security is not used for the application.</span></span>

4.  <span data-ttu-id="c42c9-111">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c42c9-111">Click **OK**.</span></span>

<span data-ttu-id="c42c9-112">Le paramètre d’autorisation sélectionné prend effet lors du prochain démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="c42c9-112">The selected authorization setting takes effect the next time the application is started.</span></span>

 

 



