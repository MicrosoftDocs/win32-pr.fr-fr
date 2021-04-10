---
description: Une application serveur COM+ peut être créée en tant que service pour démarrer automatiquement au démarrage du système ou manuellement par des activations.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configuration d’une application serveur COM+ en tant qu’application de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860853"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="6c2a4-103">Configuration d’une application serveur COM+ en tant qu’application de service</span><span class="sxs-lookup"><span data-stu-id="6c2a4-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="6c2a4-104">Une application serveur COM+ peut être créée en tant que service pour démarrer automatiquement au démarrage du système ou manuellement par des activations.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="6c2a4-105">Si le service ne démarre pas, l’option de gestion des erreurs spécifie la gravité de l’erreur et détermine l’action à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="6c2a4-106">L’option permettant de configurer un service pour qu’il s’exécute en tant que compte système local est également disponible, ainsi que l’option permettant d’affecter un compte d’utilisateur spécifique pour lequel l’application serveur COM+ s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="6c2a4-107">Vous pouvez également sélectionner des dépendances dans une liste de services inscrits sur l’ordinateur à l’aide des services de composants.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="6c2a4-108">Cela permet de déterminer les services qui doivent être exécutés avant le démarrage de ce service.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="6c2a4-109">**Pour configurer une application COM+ pour qu’elle s’exécute en tant que service**</span><span class="sxs-lookup"><span data-stu-id="6c2a4-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="6c2a4-110">Dans l’arborescence de la console de l’outil d’administration Services de composants, localisez l’application serveur COM+ que vous souhaitez exécuter en tant que service.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="6c2a4-111">Cliquez avec le bouton droit sur l’application serveur COM+, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="6c2a4-112">Dans la boîte de dialogue **Propriétés** , cliquez sur l’onglet **activation** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="6c2a4-113">Dans la zone **type d’activation** , activez la case à cocher exécuter l' **application en tant que service NT** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="6c2a4-114">La case à cocher **exécuter l’application en tant que service NT** est activée uniquement pour les applications serveur et est désactivée pour les applications de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="6c2a4-115">Cliquez sur le bouton **configurer un nouveau service** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="6c2a4-116">Dans la zone **type de démarrage** de la boîte de dialogue nom du **service** , sélectionnez **automatique** ou **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="6c2a4-117">Facultatif Pour spécifier l’action à entreprendre pour une erreur particulière, sélectionnez **Ignorer**, **normal**, **grave** ou **critique** dans la zone **gestion des erreurs** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="6c2a4-118">Le comportement associé à chaque option est le suivant :</span><span class="sxs-lookup"><span data-stu-id="6c2a4-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="6c2a4-119">**Ignorer**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-119">**Ignore**.</span></span> <span data-ttu-id="6c2a4-120">Le programme de démarrage consigne l’erreur, mais poursuit l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="6c2a4-121">**Normal**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-121">**Normal**.</span></span> <span data-ttu-id="6c2a4-122">L’erreur est consignée, une boîte de message s’affiche et le programme de démarrage continue l’opération de démarrage.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="6c2a4-123">**Grave**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-123">**Severe**.</span></span> <span data-ttu-id="6c2a4-124">L’erreur est journalisée et le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="6c2a4-125">S’il s’agit de la dernière configuration correcte connue qui est démarrée lorsque l’erreur est journalisée, l’opération de démarrage se poursuit.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="6c2a4-126">**Critique**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-126">**Critical**.</span></span> <span data-ttu-id="6c2a4-127">L’erreur est journalisée et le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="6c2a4-128">S’il s’agit de la dernière configuration correcte connue qui est démarrée lorsque l’erreur est journalisée, l’opération de démarrage échoue.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="6c2a4-129">Facultatif Pour définir d’autres services comme dépendants, sélectionnez les services dépendants dans la liste de la zone **dépendances** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="6c2a4-130">Facultatif Pour indiquer que le service doit être autorisé à interagir avec le bureau, activez la case à cocher **autoriser le service à interagir avec le bureau** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="6c2a4-131">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-131">Click **Create**.</span></span>

11. <span data-ttu-id="6c2a4-132">Facultatif Pour affecter le service à un compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="6c2a4-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="6c2a4-133">Sous l’onglet **identité** , sélectionnez **cet utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="6c2a4-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="6c2a4-134">Pour sélectionner l’utilisateur, entrez le nom d’utilisateur dans la zone **utilisateur** ou cliquez sur le bouton **Parcourir** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="6c2a4-135">Entrez le mot de passe du compte d’utilisateur dans la zone **mot de passe** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="6c2a4-136">Entrez le même mot de passe dans la zone **confirmer le mot de passe** .</span><span class="sxs-lookup"><span data-stu-id="6c2a4-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



