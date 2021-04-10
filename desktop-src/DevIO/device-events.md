---
description: Les applications, y compris les services, peuvent s’inscrire pour recevoir des notifications d’événements d’appareil.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Événements de l’appareil (IoEvent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200857"
---
# <a name="device-events-ioeventh"></a><span data-ttu-id="1eb61-103">Événements de l’appareil (IoEvent. h)</span><span class="sxs-lookup"><span data-stu-id="1eb61-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="1eb61-104">Les applications, y compris les services, peuvent s’inscrire pour recevoir des notifications d’événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="1eb61-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="1eb61-105">Par exemple, un service de catalogue peut recevoir des notifications sur les volumes montés ou démontés pour qu’il puisse ajuster les chemins d’accès aux fichiers sur le volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="1eb61-106">Le système notifie une application qu’un événement d’appareil s’est produit en envoyant à l’application un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="1eb61-107">Le système notifie un service qu’un événement d’appareil s’est produit en appelant la fonction du gestionnaire d’événements du service, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="1eb61-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="1eb61-108">Pour recevoir des notifications d’événements d’appareil, appelez la fonction [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) avec une structure de [**handle de \_ diffusion \_ de développement**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="1eb61-109">Veillez à définir le **membre \_ handle dbch** sur le descripteur d’appareil obtenu à partir de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="1eb61-110">Définissez également le membre **dbch \_ DeviceType** sur le **\_ \_ descripteur DBT DEVTYP**.</span><span class="sxs-lookup"><span data-stu-id="1eb61-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="1eb61-111">La fonction retourne un handle de notification de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1eb61-111">The function returns a device notification handle.</span></span> <span data-ttu-id="1eb61-112">Notez que ce n’est pas le même que le descripteur de volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="1eb61-113">Lorsque votre application reçoit une notification, si le type d’événement est [DBT \_ CUSTOMEVENT](dbt-customevent.md), vous avez peut-être reçu l’un des événements d’appareil définis dans IoEvent. h.</span><span class="sxs-lookup"><span data-stu-id="1eb61-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="1eb61-114">Pour déterminer si l’un de ces événements s’est produit, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="1eb61-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="1eb61-115">Traitez les données d’événement comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="1eb61-116">Vérifiez que le membre **dbch \_ DeviceType** est défini sur **DBT \_ DEVTYP \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="1eb61-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="1eb61-117">Si **dbch \_ DeviceType** est **DBT \_ \_ handle DEVTYP**, les données d’événement sont en fait un pointeur vers une structure de [**handle de \_ diffusion \_ de développement**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="1eb61-118">Comparez le membre **dbch \_ EventGuid** aux **GUID** indiqués dans le tableau suivant à l’aide de la fonction [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="1eb61-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**\_ \_ \_ verrous exclusifs du CD-ROM du GUID \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="1eb61-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-121">Le lecteur de CD-ROM a été verrouillé pour un accès exclusif.</span><span class="sxs-lookup"><span data-stu-id="1eb61-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="1eb61-122">**Windows Server 2003 et Windows XP :** La prise en charge de cette valeur nécessite IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="1eb61-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="1eb61-123">Pour plus d’informations, consultez [API de mastérisation d’image](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="1eb61-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO \_ cdrom \_ exclusif \_ déverrouillage**</span><span class="sxs-lookup"><span data-stu-id="1eb61-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="1eb61-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-126">Un lecteur de CD-ROM verrouillé pour un accès exclusif a été déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="1eb61-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="1eb61-127">**Windows Server 2003 et Windows XP :** La prise en charge de cette valeur nécessite IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="1eb61-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="1eb61-128">Pour plus d’informations, consultez [API de mastérisation d’image](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="1eb61-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**le \_ périphérique d’e/s GUID \_ \_ devient \_ prêt**</span><span class="sxs-lookup"><span data-stu-id="1eb61-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1eb61-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-131">La rotation du média est en cours.</span><span class="sxs-lookup"><span data-stu-id="1eb61-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ \_ requête externe de l’appareil d’e/s GUID \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1eb61-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-134">Il existe plusieurs causes possibles pour cet événement. Pour plus d’informations, reportez-vous à la spécification MMC T10 de la commande recevoir la NOTIFICATION d’état des événements, à l’adresse [https://www.t10.org/](https://www.t10.org/) .</span><span class="sxs-lookup"><span data-stu-id="1eb61-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_arrivée du média d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1eb61-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-137">Un support amovible a été ajouté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1eb61-137">Removable media has been added to the device.</span></span> <span data-ttu-id="1eb61-138">Le membre de **\_ données dbch** est un pointeur vers une structure de [**\_ \_ \_ contexte de modification**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) de la classe.</span><span class="sxs-lookup"><span data-stu-id="1eb61-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="1eb61-139">Le membre **NewState** fournit des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="1eb61-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="1eb61-140">Par exemple, la valeur **MediaUnavailable** indique que le support n’est pas disponible (par exemple, en raison d’une session d’enregistrement active).</span><span class="sxs-lookup"><span data-stu-id="1eb61-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="1eb61-141">**Windows XP :** Le membre de **\_ données dbch** est une valeur **ULong** qui représente le nombre de fois où le média a été modifié depuis le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="1eb61-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_requête d' \_ éjection de média d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1eb61-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-144">Le lecteur du support amovible a reçu une demande de la part de l’utilisateur d’éjecter l’emplacement ou le média spécifié.</span><span class="sxs-lookup"><span data-stu-id="1eb61-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID \_ - \_ Suppression de média e/s \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="1eb61-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-147">Le support amovible a été supprimé de l’appareil ou n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="1eb61-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="1eb61-148">Le membre de **\_ données dbch** est un pointeur vers une structure de [**\_ \_ \_ contexte de modification**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) de la classe.</span><span class="sxs-lookup"><span data-stu-id="1eb61-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="1eb61-149">Le membre **NewState** fournit des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="1eb61-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="1eb61-150">Par exemple, la valeur **MediaUnavailable** indique que le support n’est pas disponible (par exemple, en raison d’une session d’enregistrement active).</span><span class="sxs-lookup"><span data-stu-id="1eb61-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="1eb61-151">**Windows XP :** Le membre de **\_ données dbch** est une valeur **ULong** qui représente le nombre de fois où le média a été modifié depuis le démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="1eb61-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_modification du volume d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-153">7373654a-812a-11d0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="1eb61-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-154">Le nom du volume a changé.</span><span class="sxs-lookup"><span data-stu-id="1eb61-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_taille de \_ modification du volume e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span><span class="sxs-lookup"><span data-stu-id="1eb61-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-157">La taille du système de fichiers sur le volume a changé.</span><span class="sxs-lookup"><span data-stu-id="1eb61-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="1eb61-158">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1eb61-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**démontage du \_ volume d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1eb61-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-161">Une tentative de démontage du volume est en cours.</span><span class="sxs-lookup"><span data-stu-id="1eb61-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="1eb61-162">Vous devez fermer tous les descripteurs des fichiers et des répertoires sur le volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="1eb61-163">Cet événement ne sera pas nécessairement précédé d’un événement **de \_ \_ \_ verrouillage du volume e/s par GUID** .</span><span class="sxs-lookup"><span data-stu-id="1eb61-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_échec du \_ démontage du volume d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1eb61-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-166">Une tentative de démontage d’un volume a échoué.</span><span class="sxs-lookup"><span data-stu-id="1eb61-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="1eb61-167">Cela se produit souvent parce qu’un autre processus n’a pas pu répondre à l’avis de **\_ \_ \_ démontage du volume d’e/s GUID** en fermant ses Handles en suspens.</span><span class="sxs-lookup"><span data-stu-id="1eb61-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="1eb61-168">En raison de l’échec du démontage, vous pouvez rouvrir tous les descripteurs sur le volume affecté.</span><span class="sxs-lookup"><span data-stu-id="1eb61-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**changement d’État du volume d' \_ e/s du \_ \_ FVE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="1eb61-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-171">L’état du Chiffrement de lecteur BitLocker du volume a changé.</span><span class="sxs-lookup"><span data-stu-id="1eb61-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="1eb61-172">Cet événement est signalé lorsque BitLocker est activé ou désactivé, ou lorsque le chiffrement commence, se termine, s’interrompt ou reprend.</span><span class="sxs-lookup"><span data-stu-id="1eb61-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="1eb61-173">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1eb61-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_verrou du volume d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-175">50708874-c9af-11D1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1eb61-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-176">Un autre processus tente de verrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="1eb61-177">Vous devez fermer tous les descripteurs des fichiers et des répertoires sur le volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_échec du \_ verrouillage du volume d’e/s du \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1eb61-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-180">Une tentative de verrouillage d’un volume a échoué.</span><span class="sxs-lookup"><span data-stu-id="1eb61-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="1eb61-181">Cela se produit souvent parce qu’un autre processus n’a pas pu répondre à un événement de **\_ \_ \_ verrouillage du volume e/s par GUID** en fermant ses Handles en suspens.</span><span class="sxs-lookup"><span data-stu-id="1eb61-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="1eb61-182">Étant donné que le verrou a échoué, vous pouvez rouvrir tous les descripteurs sur le volume affecté.</span><span class="sxs-lookup"><span data-stu-id="1eb61-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montage du volume d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1eb61-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-185">Le volume a été monté par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="1eb61-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="1eb61-186">Vous pouvez y accéder à un ou plusieurs descripteurs.</span><span class="sxs-lookup"><span data-stu-id="1eb61-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_modification du \_ nom du volume e/s du \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-188">2de97f83-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="1eb61-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-189">Le nom du volume a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1eb61-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**le \_ volume d’e/s GUID a \_ \_ besoin de \_ chkdsk**</span><span class="sxs-lookup"><span data-stu-id="1eb61-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="1eb61-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-192">Un système de fichiers a détecté une altération sur le volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="1eb61-193">L’application doit exécuter CHKDSK sur le volume ou en informer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1eb61-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="1eb61-194">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1eb61-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_modification de \_ la \_ configuration physique du volume d' \_ e/s du GUID \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-196">2de97f84-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="1eb61-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-197">La composition physique ou l’état physique actuel du volume a changé.</span><span class="sxs-lookup"><span data-stu-id="1eb61-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID du \_ volume d’e/s de \_ préparation d' \_ \_ éjection**</span><span class="sxs-lookup"><span data-stu-id="1eb61-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="1eb61-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-200">Le système de fichiers prépare le disque à éjecter.</span><span class="sxs-lookup"><span data-stu-id="1eb61-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="1eb61-201">Par exemple, le système de fichiers arrête une opération de mise en forme en arrière-plan ou ferme la session sur un média en écriture unique.</span><span class="sxs-lookup"><span data-stu-id="1eb61-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="1eb61-202">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1eb61-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_changement d' \_ \_ ID unique \_ du volume d’e/s GUID \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="1eb61-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-205">L’identificateur unique du volume a été modifié.</span><span class="sxs-lookup"><span data-stu-id="1eb61-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="1eb61-206">Pour plus d’informations sur l’identificateur unique, consultez [**IOCTL \_ MOUNTDEV \_ query \_ unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span><span class="sxs-lookup"><span data-stu-id="1eb61-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="1eb61-207">**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur n’est pas prise en charge avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1eb61-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**déverrouillage du \_ volume d’e/s GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="1eb61-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-210">Le volume a été déverrouillé par un autre processus.</span><span class="sxs-lookup"><span data-stu-id="1eb61-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="1eb61-211">Vous pouvez y accéder à un ou plusieurs descripteurs.</span><span class="sxs-lookup"><span data-stu-id="1eb61-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1eb61-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID du \_ volume d’e/s du GUID \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1eb61-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb61-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="1eb61-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="1eb61-214">Le média est à l’usage. Cet événement est envoyé lorsqu’un système de fichiers détermine que le taux d’erreur sur un volume est trop élevé ou que son espace de remplacement de défauts est presque épuisé.</span><span class="sxs-lookup"><span data-stu-id="1eb61-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="1eb61-215">**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1eb61-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1eb61-216">Notes</span><span class="sxs-lookup"><span data-stu-id="1eb61-216">Remarks</span></span>

<span data-ttu-id="1eb61-217">Les événements du **\_ \_ \_ démontage** du volume d’e/s du GUID et du **\_ \_ \_ démontage \_** du volume d’e/s GUID sont liés, de même que le GUID du **\_ \_ \_ verrou d’e/** s du volume et l' **\_ \_ \_ \_ échec du verrouillage du volume** .</span><span class="sxs-lookup"><span data-stu-id="1eb61-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="1eb61-218">Les événements de verrouillage du **\_ volume d’e/ \_ \_** s du volume et d' **\_ e/s \_ \_** GUID indiquent qu’une opération est tentée.</span><span class="sxs-lookup"><span data-stu-id="1eb61-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="1eb61-219">Vous devez agir sur la notification d’événement et enregistrer l’action effectuée.</span><span class="sxs-lookup"><span data-stu-id="1eb61-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="1eb61-220">Le **\_ démontage du volume d’e/s GUID \_ \_ \_ a échoué** et les événements du **verrou d' \_ e/s du \_ volume en \_ \_ échec** indiquent que l’opération tentée a échoué.</span><span class="sxs-lookup"><span data-stu-id="1eb61-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="1eb61-221">Vous pouvez ensuite utiliser votre enregistrement pour annuler les actions que vous avez effectuées en réponse à l’opération.</span><span class="sxs-lookup"><span data-stu-id="1eb61-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="1eb61-222">Le membre **dbch \_ hdevnotify** de la structure de [**\_ \_ handle de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indique l’appareil affecté.</span><span class="sxs-lookup"><span data-stu-id="1eb61-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="1eb61-223">Notez qu’il s’agit du handle de notification de l’appareil retourné par [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), et non pas d’un handle de volume.</span><span class="sxs-lookup"><span data-stu-id="1eb61-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="1eb61-224">Pour effectuer des opérations sur le volume, mappez ce handle au handle de volume correspondant.</span><span class="sxs-lookup"><span data-stu-id="1eb61-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb61-225">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eb61-225">Requirements</span></span>



| <span data-ttu-id="1eb61-226">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eb61-226">Requirement</span></span> | <span data-ttu-id="1eb61-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eb61-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb61-228">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eb61-228">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb61-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1eb61-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="1eb61-230">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eb61-230">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb61-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1eb61-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="1eb61-232">En-tête</span><span class="sxs-lookup"><span data-stu-id="1eb61-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eb61-233"><dt>IoEvent. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb61-233"><dt>IoEvent.h</dt></span></span> </dl> |



 

