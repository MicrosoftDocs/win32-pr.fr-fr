---
description: 'En savoir plus sur : exemple de service complet'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Exemple de service complet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520087"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="5afa6-103">Exemple de service complet</span><span class="sxs-lookup"><span data-stu-id="5afa6-103">The Complete Service Sample</span></span>

<span data-ttu-id="5afa6-104">Les rubriques de cette section forment un exemple complet de service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="5afa6-105">[Sample.MC](sample-mc.md) (contient des messages d’erreur)</span><span class="sxs-lookup"><span data-stu-id="5afa6-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="5afa6-106">[SVC. cpp](svc-cpp.md) (contient le code de service)</span><span class="sxs-lookup"><span data-stu-id="5afa6-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="5afa6-107">[SvcConfig. cpp](svcconfig-cpp.md) (contient le code de configuration du service)</span><span class="sxs-lookup"><span data-stu-id="5afa6-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="5afa6-108">[SvcControl. cpp](svccontrol-cpp.md) (contient le code de contrôle du service)</span><span class="sxs-lookup"><span data-stu-id="5afa6-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="5afa6-109">Génération du service</span><span class="sxs-lookup"><span data-stu-id="5afa6-109">Building the Service</span></span>

<span data-ttu-id="5afa6-110">La procédure suivante décrit la génération du service et l’inscription de la DLL de message d’événement.</span><span class="sxs-lookup"><span data-stu-id="5afa6-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="5afa6-111">**Pour générer le service et inscrire la DLL de message d’événement**</span><span class="sxs-lookup"><span data-stu-id="5afa6-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="5afa6-112">Générez la DLL de message à partir de Sample.mc en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="5afa6-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="5afa6-113">**sample.mc MC-U**</span><span class="sxs-lookup"><span data-stu-id="5afa6-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="5afa6-114">**RC-r exemple. RC**</span><span class="sxs-lookup"><span data-stu-id="5afa6-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="5afa6-115">**Link-dll-NOENTRY -out:sample.dll Sample. res**</span><span class="sxs-lookup"><span data-stu-id="5afa6-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="5afa6-116">Générez Svc.exe, SvcConfig.exe et SvcControl.exe à partir de svc. cpp, SvcConfig. cpp et SvcControl. cpp, respectivement.</span><span class="sxs-lookup"><span data-stu-id="5afa6-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="5afa6-117">Créez la clé de Registre **HKEY \_ local \_ machine \\ System System \\ CurrentControlSet \\ services \\ EventLog \\ application \\ SvcName** et ajoutez les valeurs de Registre suivantes à cette clé.</span><span class="sxs-lookup"><span data-stu-id="5afa6-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="5afa6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5afa6-118">Value</span></span>                              | <span data-ttu-id="5afa6-119">Type</span><span class="sxs-lookup"><span data-stu-id="5afa6-119">Type</span></span>       | <span data-ttu-id="5afa6-120">Description</span><span class="sxs-lookup"><span data-stu-id="5afa6-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5afa6-121">**EventMessageFile**  =  *\_ chemin* de la dll</span><span class="sxs-lookup"><span data-stu-id="5afa6-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="5afa6-122">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="5afa6-122">REG\_SZ</span></span>    | <span data-ttu-id="5afa6-123">Chemin d’accès à la DLL de ressources uniquement qui contient des chaînes que le service peut écrire dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="5afa6-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="5afa6-124">**TypesSupported** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="5afa6-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="5afa6-125">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="5afa6-125">REG\_DWORD</span></span> | <span data-ttu-id="5afa6-126">Masque de bits qui spécifie les types d’événements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5afa6-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="5afa6-127">La valeur 0x000000007 indique que tous les types sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5afa6-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="5afa6-128">Test du service</span><span class="sxs-lookup"><span data-stu-id="5afa6-128">Testing the Service</span></span>

<span data-ttu-id="5afa6-129">La procédure suivante décrit comment tester le service.</span><span class="sxs-lookup"><span data-stu-id="5afa6-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="5afa6-130">**Pour tester le service**</span><span class="sxs-lookup"><span data-stu-id="5afa6-130">**To test the service**</span></span>

1.  <span data-ttu-id="5afa6-131">Dans le panneau de configuration, démarrez l’application **services** .</span><span class="sxs-lookup"><span data-stu-id="5afa6-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="5afa6-132">(Dans les étapes suivantes, utilisez la touche F5 pour actualiser l’affichage après l’exécution d’une commande qui modifie les informations de l’application **services** .)</span><span class="sxs-lookup"><span data-stu-id="5afa6-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="5afa6-133">Exécutez la commande suivante pour installer le service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="5afa6-134">**installation SVC**</span><span class="sxs-lookup"><span data-stu-id="5afa6-134">**svc install**</span></span>

    <span data-ttu-id="5afa6-135">Le service écrit « service correctement installé » sur la console si l’opération réussit ou un message d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5afa6-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="5afa6-136">Si l’installation du service a échoué, le service s’affiche dans l’application **services** .</span><span class="sxs-lookup"><span data-stu-id="5afa6-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="5afa6-137">Notez que le **nom** est défini sur « SvcName », que la **Description** et l' **État** sont vides, et que **type de démarrage** est défini sur « manuel ».</span><span class="sxs-lookup"><span data-stu-id="5afa6-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="5afa6-138">Exécutez la commande suivante pour démarrer le service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="5afa6-139">**svccontrol démarrer SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="5afa6-140">Si l’opération a échoué, le programme de contrôle des services écrit « démarrage du service en attente... » puis « service démarré correctement » sur la console.</span><span class="sxs-lookup"><span data-stu-id="5afa6-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="5afa6-141">Dans le cas contraire, le programme écrit un message d’erreur dans la console.</span><span class="sxs-lookup"><span data-stu-id="5afa6-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="5afa6-142">Si le service démarre correctement, l' **État** est défini sur « démarré ».</span><span class="sxs-lookup"><span data-stu-id="5afa6-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="5afa6-143">Le code de la fonction [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) est exécuté par le SCM.</span><span class="sxs-lookup"><span data-stu-id="5afa6-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="5afa6-144">Si une erreur se produit, le service écrit un message d’erreur dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="5afa6-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="5afa6-145">Ce message comprend le nom de la fonction qui a échoué et le code d’erreur qui a été retourné en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5afa6-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="5afa6-146">Exécutez la commande suivante pour mettre à jour la description du service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="5afa6-147">**svcconfig décrire SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="5afa6-148">Le programme de configuration de service écrit la description de service correctement mise à jour sur la console si l’opération réussit ou un message d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5afa6-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="5afa6-149">Si la mise à jour se déroule correctement, la **Description** est définie sur « il s’agit d’une description de test ».</span><span class="sxs-lookup"><span data-stu-id="5afa6-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="5afa6-150">Exécutez la commande suivante pour interroger la configuration du service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="5afa6-151">**svcconfig requête SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="5afa6-152">Le programme de configuration de service écrit les informations de configuration de service dans la console si l’opération a échoué ou un message d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5afa6-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="5afa6-153">Exécutez la commande suivante pour modifier la DACL de service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="5afa6-154">**svccontrol DACL SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="5afa6-155">Le programme de configuration de service écrit « la liste DACL du service a été mise à jour correctement » sur la console si l’opération réussit ou un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5afa6-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="5afa6-156">Exécutez la commande suivante pour désactiver le service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="5afa6-157">**svcconfig désactiver SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="5afa6-158">Le programme de configuration de service écrit « service correctement désactivé » sur la console si l’opération réussit ou un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5afa6-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="5afa6-159">Si le service est désactivé avec succès, le **type de démarrage** est défini sur « désactivé ».</span><span class="sxs-lookup"><span data-stu-id="5afa6-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="5afa6-160">Exécutez la commande suivante pour activer le service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="5afa6-161">**svcconfig activer SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="5afa6-162">Le programme de configuration de service écrit « service activé avec succès » sur la console si l’opération réussit ou un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5afa6-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="5afa6-163">Si le service est activé avec succès, le **type de démarrage** est défini sur « manuel ».</span><span class="sxs-lookup"><span data-stu-id="5afa6-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="5afa6-164">Exécutez la commande suivante pour arrêter le service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="5afa6-165">**svccontrol Stop SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="5afa6-166">Si l’opération échoue, le programme de contrôle des services écrit « arrêt du service en attente... » puis « Service arrêté correctement » sur la console.</span><span class="sxs-lookup"><span data-stu-id="5afa6-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="5afa6-167">Dans le cas contraire, le programme écrit un message d’erreur dans la console.</span><span class="sxs-lookup"><span data-stu-id="5afa6-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="5afa6-168">Si le service s’arrête correctement, l' **État** est vide.</span><span class="sxs-lookup"><span data-stu-id="5afa6-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="5afa6-169">En cas d’échec de l’arrêt du service, le programme de contrôle des services écrit un message d’erreur dans le journal des événements qui comprend le nom de la fonction qui a échoué et le code d’erreur qui a été retourné en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5afa6-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="5afa6-170">Exécutez la commande suivante pour supprimer le service :</span><span class="sxs-lookup"><span data-stu-id="5afa6-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="5afa6-171">**svcconfig supprimer SvcName**</span><span class="sxs-lookup"><span data-stu-id="5afa6-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="5afa6-172">Le programme de configuration de service écrit « Service supprimé avec succès » sur la console si l’opération réussit ou un message d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5afa6-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="5afa6-173">Si le service est correctement supprimé, il n’est plus affiché dans l’application **services** .</span><span class="sxs-lookup"><span data-stu-id="5afa6-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="5afa6-174">(Notez que si vous tentez de supprimer un service qui n’est pas arrêté, l’opération se déroule correctement, mais le **type de démarrage** est défini sur « désactivé » et l’entrée de service est supprimée lors du redémarrage du système ou lorsque le service est arrêté à l’aide du gestionnaire des tâches.)</span><span class="sxs-lookup"><span data-stu-id="5afa6-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5afa6-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5afa6-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5afa6-176">Utilisation des services</span><span class="sxs-lookup"><span data-stu-id="5afa6-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 
