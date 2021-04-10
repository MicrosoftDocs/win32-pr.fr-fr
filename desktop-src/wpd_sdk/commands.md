---
description: Commandes
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Commandes (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201380"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="8fe25-103">Commandes (API WPD)</span><span class="sxs-lookup"><span data-stu-id="8fe25-103">Commands (WPD API)</span></span>

<span data-ttu-id="8fe25-104">L’application cliente et le pilote communiquent à l’aide de commandes envoyées à partir du client (via l’API Windows Mobile Device) au pilote (via l’infrastructure de pilote User-Mode).</span><span class="sxs-lookup"><span data-stu-id="8fe25-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="8fe25-105">Une commande peut ou non inclure un paramètre et peut ou non retourner un résultat.</span><span class="sxs-lookup"><span data-stu-id="8fe25-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="8fe25-106">Un client peut envoyer une commande de manière explicite, en appelant la méthode [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) ou la méthode **IPortableDeviceService : SendCommand** , ou implicitement, en appelant l’une des méthodes des interfaces clientes.</span><span class="sxs-lookup"><span data-stu-id="8fe25-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="8fe25-107">Certaines commandes peuvent être envoyées uniquement de manière explicite ; celles-ci sont indiquées dans la documentation de la commande.</span><span class="sxs-lookup"><span data-stu-id="8fe25-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="8fe25-108">Les pages de référence de commande décrivent l’objectif d’une commande, ainsi que les paramètres qu’elle s’attend à recevoir et les paramètres qu’elle doit retourner.</span><span class="sxs-lookup"><span data-stu-id="8fe25-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="8fe25-109">Une commande est identifiée par une structure **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="8fe25-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="8fe25-110">Il se compose de deux parties : une partie GUID (le membre *fmtid* ) et une partie DWORD (le membre *PID* ).</span><span class="sxs-lookup"><span data-stu-id="8fe25-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="8fe25-111">La partie GUID est utilisée pour indiquer la catégorie à laquelle la commande appartient (les commandes associées appartiennent à la même catégorie et, par conséquent, ont le même *fmtid*).</span><span class="sxs-lookup"><span data-stu-id="8fe25-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="8fe25-112">La partie DWORD indique l’ID de commande et est utilisée pour distinguer les commandes individuelles au sein d’une catégorie de commande (les valeurs *PID* pour les commandes dans la même catégorie sont différentes).</span><span class="sxs-lookup"><span data-stu-id="8fe25-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="8fe25-113">Le tableau suivant répertorie les catégories de commandes que les appareils mobiles Windows définit.</span><span class="sxs-lookup"><span data-stu-id="8fe25-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="8fe25-114">Les fabricants de périphériques peuvent définir leurs propres commandes en créant leurs propres catégories de commandes et ID de commande.</span><span class="sxs-lookup"><span data-stu-id="8fe25-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="8fe25-115">Toutefois, un fabricant ne doit pas ajouter de commandes aux catégories répertoriées ci-dessous, car celles-ci sont réservées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fe25-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="8fe25-116">**Catégories de commandes**</span><span class="sxs-lookup"><span data-stu-id="8fe25-116">**Command Categories**</span></span>



| <span data-ttu-id="8fe25-117">Catégorie de commande</span><span class="sxs-lookup"><span data-stu-id="8fe25-117">Command category</span></span>                         | <span data-ttu-id="8fe25-118">Description</span><span class="sxs-lookup"><span data-stu-id="8fe25-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe25-119">**WPD, \_ catégorie \_ commune**</span><span class="sxs-lookup"><span data-stu-id="8fe25-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="8fe25-120">Les commandes qui sont communes à tous les objets et périphériques.</span><span class="sxs-lookup"><span data-stu-id="8fe25-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="8fe25-121">**indicateurs d’appareil de la \_ catégorie wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="8fe25-122">Commandes utilisées pour récupérer des informations facultatives sur l’appareil qui peuvent être utilisées pour améliorer l’expérience de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="8fe25-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="8fe25-123">**\_SMS de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="8fe25-124">Commandes utilisées pour les appareils qui prennent en charge la fonctionnalité SMS (Short Message Service), qui est généralement exposée sur les téléphones portables.</span><span class="sxs-lookup"><span data-stu-id="8fe25-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="8fe25-125">**\_capture d' \_ \_ image continue de catégorie \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="8fe25-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="8fe25-126">Commandes utilisées pour les appareils qui prennent en charge la capture d’images continues.</span><span class="sxs-lookup"><span data-stu-id="8fe25-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="8fe25-127">**\_stockage de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="8fe25-128">Commandes utilisées pour le stockage des objets fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="8fe25-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="8fe25-129">Les commandes spécifiques définies pour chacun de ces types sont présentées dans les tableaux suivants, organisés par type de commande.</span><span class="sxs-lookup"><span data-stu-id="8fe25-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="8fe25-130">**Catégorie \_ commune de la catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="8fe25-131">Commande</span><span class="sxs-lookup"><span data-stu-id="8fe25-131">Command</span></span>                                                                                | <span data-ttu-id="8fe25-132">Description</span><span class="sxs-lookup"><span data-stu-id="8fe25-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="8fe25-133">**\_appareil de \_ \_ réinitialisation commune de commande wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="8fe25-134">Réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8fe25-134">Resets the device.</span></span> |



 

<span data-ttu-id="8fe25-135">**\_Catégorie d' \_ indicateurs d’appareil de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="8fe25-136">Commande</span><span class="sxs-lookup"><span data-stu-id="8fe25-136">Command</span></span>                                                                                                              | <span data-ttu-id="8fe25-137">Description</span><span class="sxs-lookup"><span data-stu-id="8fe25-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="8fe25-138">**\_options d’appareil de commande wpd obtient l' \_ \_ \_ \_ emplacement du contenu \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="8fe25-139">Récupère les ID d’objet des dossiers qui peuvent contenir un objet d’un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="8fe25-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="8fe25-140">**Catégorie de stockage de \_ catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="8fe25-141">Commande</span><span class="sxs-lookup"><span data-stu-id="8fe25-141">Command</span></span>                                                                     | <span data-ttu-id="8fe25-142">Description</span><span class="sxs-lookup"><span data-stu-id="8fe25-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="8fe25-143">**\_éjection de \_ stockage de commande wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="8fe25-144">Éjecte un support de stockage qui peut être éjecté à distance par le pilote.</span><span class="sxs-lookup"><span data-stu-id="8fe25-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="8fe25-145">**\_format de \_ stockage des commandes wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="8fe25-146">Met en forme un objet fonctionnel de stockage sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8fe25-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="8fe25-147">**Catégorie des \_ SMS de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="8fe25-148">Commande</span><span class="sxs-lookup"><span data-stu-id="8fe25-148">Command</span></span>                                                         | <span data-ttu-id="8fe25-149">Description</span><span class="sxs-lookup"><span data-stu-id="8fe25-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="8fe25-150">**\_commande wpd \_ SMS \_ Send**</span><span class="sxs-lookup"><span data-stu-id="8fe25-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="8fe25-151">Lance l’envoi d’un message SMS par un objet fonctionnel SMS.</span><span class="sxs-lookup"><span data-stu-id="8fe25-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="8fe25-152">**\_Catégorie de \_ \_ capture d’image continue de catégorie wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="8fe25-153">Commande</span><span class="sxs-lookup"><span data-stu-id="8fe25-153">Command</span></span>                                                                                                   | <span data-ttu-id="8fe25-154">Description</span><span class="sxs-lookup"><span data-stu-id="8fe25-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="8fe25-155">**démarrage de la \_ \_ \_ capture d’image continue \_ de la commande wpd \_**</span><span class="sxs-lookup"><span data-stu-id="8fe25-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="8fe25-156">Lance une capture d’image continue par un objet fonctionnel d’image continue.</span><span class="sxs-lookup"><span data-stu-id="8fe25-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8fe25-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fe25-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fe25-158">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="8fe25-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



