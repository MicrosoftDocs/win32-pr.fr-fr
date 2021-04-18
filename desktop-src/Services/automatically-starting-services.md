---
description: Lors du démarrage du système, le SCM démarre tous les services à démarrage automatique et les services dont ils dépendent. Par exemple, si un service à démarrage automatique dépend d’un service de démarrage à la demande, le service de démarrage à la demande est également démarré automatiquement.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Démarrage automatique des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522665"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="e8e56-104">Démarrage automatique des services</span><span class="sxs-lookup"><span data-stu-id="e8e56-104">Automatically Starting Services</span></span>

<span data-ttu-id="e8e56-105">Lors du démarrage du système, le SCM démarre tous les services à démarrage automatique et les services dont ils dépendent.</span><span class="sxs-lookup"><span data-stu-id="e8e56-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="e8e56-106">Par exemple, si un service à démarrage automatique dépend d’un service de démarrage à la demande, le service de démarrage à la demande est également démarré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e8e56-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="e8e56-107">L’ordre de chargement est déterminé par les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e8e56-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="e8e56-108">L’ordre des groupes dans la liste des groupes d’ordre de chargement.</span><span class="sxs-lookup"><span data-stu-id="e8e56-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="e8e56-109">Ces informations sont stockées dans la valeur **ServiceGroupOrder** de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="e8e56-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="e8e56-110">**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**</span><span class="sxs-lookup"><span data-stu-id="e8e56-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="e8e56-111">Pour spécifier le groupe de commandes de charge pour un service, utilisez le paramètre *lpLoadOrderGroup* de la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="e8e56-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="e8e56-112">Ordre des services au sein d’un groupe spécifié dans le vecteur d’ordre des balises.</span><span class="sxs-lookup"><span data-stu-id="e8e56-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="e8e56-113">Ces informations sont stockées dans la valeur **GroupOrderList** de la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="e8e56-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="e8e56-114">**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**</span><span class="sxs-lookup"><span data-stu-id="e8e56-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="e8e56-115">Les dépendances listées pour chaque service.</span><span class="sxs-lookup"><span data-stu-id="e8e56-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="e8e56-116">Une fois le démarrage terminé, le système exécute le programme de vérification de démarrage spécifié par la valeur **BootVerificationProgram** de la clé de Registre suivante : **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**.</span><span class="sxs-lookup"><span data-stu-id="e8e56-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="e8e56-117">Par défaut, cette valeur n'est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e8e56-117">By default, this value is not set.</span></span> <span data-ttu-id="e8e56-118">Le système signale simplement que le démarrage a réussi après que le premier utilisateur s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="e8e56-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="e8e56-119">Vous pouvez fournir un programme de vérification de démarrage qui vérifie le système à la recherche de problèmes et signale l’état de démarrage au SCM à l’aide de la fonction [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="e8e56-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="e8e56-120">Après un démarrage réussi, le système enregistre un clone de la base de données dans la dernière configuration connue (correcte connue).</span><span class="sxs-lookup"><span data-stu-id="e8e56-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="e8e56-121">Le système peut restaurer cette copie de la base de données si les modifications apportées à la base de données active entraînent l’échec du redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="e8e56-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="e8e56-122">Voici la clé de registre de cette base de données :</span><span class="sxs-lookup"><span data-stu-id="e8e56-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="e8e56-123">**HKEY \_ local \_ machine \\ System \\ ControlSet *xxx* \\ services**</span><span class="sxs-lookup"><span data-stu-id="e8e56-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="e8e56-124">où *xxx* est la valeur enregistrée dans la valeur de Registre suivante : **HKEY \_ local \_ machine \\ System \\ Select \\ LastKnownGood**.</span><span class="sxs-lookup"><span data-stu-id="e8e56-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="e8e56-125">Si un service à démarrage automatique avec une erreur de SERVICE de niveau de contrôle d’erreur \_ \_ critique ne démarre pas, le SCM redémarre l’ordinateur à l’aide de la configuration correcte connue.</span><span class="sxs-lookup"><span data-stu-id="e8e56-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="e8e56-126">Si la configuration correcte connue est déjà utilisée, le démarrage échoue.</span><span class="sxs-lookup"><span data-stu-id="e8e56-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="e8e56-127">Un service à démarrage automatique peut être configuré en tant que service à démarrage automatique retardé en appelant la fonction [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) avec \_ les \_ informations de démarrage automatique différé de la configuration du service \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e8e56-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="e8e56-128">Cette modification prend effet après le prochain démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="e8e56-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="e8e56-129">Pour plus d’informations, [**consultez \_ \_ \_ \_ informations sur le démarrage automatique retardé du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span><span class="sxs-lookup"><span data-stu-id="e8e56-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



