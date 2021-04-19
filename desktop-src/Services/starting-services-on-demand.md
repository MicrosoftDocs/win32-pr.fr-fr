---
description: L’utilisateur peut démarrer un service à l’aide de l’utilitaire panneau de configuration des services. L’utilisateur peut spécifier des arguments pour le service dans le champ paramètres de démarrage. Un programme de contrôle de service peut démarrer un service et spécifier ses arguments avec la fonction StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Démarrage des services à la demande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521949"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="99ed3-105">Démarrage des services à la demande</span><span class="sxs-lookup"><span data-stu-id="99ed3-105">Starting Services on Demand</span></span>

<span data-ttu-id="99ed3-106">L’utilisateur peut démarrer un service à l’aide de l’utilitaire panneau de configuration des services.</span><span class="sxs-lookup"><span data-stu-id="99ed3-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="99ed3-107">L’utilisateur peut spécifier des arguments pour le service dans le champ **paramètres de démarrage** .</span><span class="sxs-lookup"><span data-stu-id="99ed3-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="99ed3-108">Un programme de contrôle de service peut démarrer un service et spécifier ses arguments avec la fonction [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="99ed3-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="99ed3-109">Lorsque le service est démarré, le SCM effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="99ed3-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="99ed3-110">Récupérez les informations de compte stockées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="99ed3-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="99ed3-111">Connectez-vous au compte de service.</span><span class="sxs-lookup"><span data-stu-id="99ed3-111">Log on the service account.</span></span>
-   <span data-ttu-id="99ed3-112">Chargez le profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="99ed3-112">Load the user profile.</span></span>
-   <span data-ttu-id="99ed3-113">Créez le service dans l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="99ed3-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="99ed3-114">Attribuez le jeton d’ouverture de session au processus.</span><span class="sxs-lookup"><span data-stu-id="99ed3-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="99ed3-115">Autorisez l’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="99ed3-115">Allow the process to execute.</span></span>

 

 



