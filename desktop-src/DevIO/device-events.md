---
description: Les applications, y compris les services, peuvent s’inscrire pour recevoir des notifications d’événements d’appareil.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Événements de l’appareil (IoEvent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114382"
---
# <a name="device-events-ioeventh"></a>Événements de l’appareil (IoEvent. h)

Les applications, y compris les services, peuvent s’inscrire pour recevoir des notifications d’événements d’appareil. Par exemple, un service de catalogue peut recevoir des notifications sur les volumes montés ou démontés pour qu’il puisse ajuster les chemins d’accès aux fichiers sur le volume. Le système notifie une application qu’un événement d’appareil s’est produit en envoyant à l’application un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) . Le système notifie un service qu’un événement d’appareil s’est produit en appelant la fonction du gestionnaire d’événements du service, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Pour recevoir des notifications d’événements d’appareil, appelez la fonction [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) avec une structure de [**handle de \_ diffusion \_ de développement**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) . Veillez à définir le **membre \_ handle dbch** sur le descripteur d’appareil obtenu à partir de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Définissez également le membre **dbch \_ DeviceType** sur le **\_ \_ descripteur DBT DEVTYP**. La fonction retourne un handle de notification de l’appareil. Notez que ce n’est pas le même que le descripteur de volume.

Lorsque votre application reçoit une notification, si le type d’événement est [DBT \_ CUSTOMEVENT](dbt-customevent.md), vous avez peut-être reçu l’un des événements d’appareil définis dans IoEvent. h. Pour déterminer si l’un de ces événements s’est produit, procédez comme suit.

1.  Traitez les données d’événement comme une structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Vérifiez que le membre **dbch \_ DeviceType** est défini sur **DBT \_ DEVTYP \_ handle**.
2.  Si **dbch \_ DeviceType** est **DBT \_ \_ handle DEVTYP**, les données d’événement sont en fait un pointeur vers une structure de [**handle de \_ diffusion \_ de développement**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .
3.  Comparez le membre **dbch \_ EventGuid** aux **GUID** indiqués dans le tableau suivant à l’aide de la fonction [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**\_ \_ \_ verrous exclusifs du CD-ROM du GUID \_**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



Le lecteur de CD-ROM a été verrouillé pour un accès exclusif.

**Windows Server 2003 et Windows XP :** La prise en charge de cette valeur nécessite IMAPi 2,0. Pour plus d’informations, consultez [API de mastérisation d’image](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO \_ cdrom \_ exclusif \_ déverrouillage**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Un lecteur de CD-ROM verrouillé pour un accès exclusif a été déverrouillé.

**Windows Server 2003 et Windows XP :** La prise en charge de cette valeur nécessite IMAPi 2,0. Pour plus d’informations, consultez [API de mastérisation d’image](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**le \_ périphérique d’e/s GUID \_ \_ devient \_ prêt**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



La rotation du média est en cours.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ \_ requête externe de l’appareil d’e/s GUID \_**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Il existe plusieurs causes possibles pour cet événement. Pour plus d’informations, reportez-vous à la spécification MMC T10 de la commande recevoir la NOTIFICATION d’état des événements, à l’adresse [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_arrivée du média d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Un support amovible a été ajouté à l’appareil. Le membre de **\_ données dbch** est un pointeur vers une structure de [**\_ \_ \_ contexte de modification**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) de la classe. Le membre **NewState** fournit des informations d’État. Par exemple, la valeur **MediaUnavailable** indique que le support n’est pas disponible (par exemple, en raison d’une session d’enregistrement active).

**Windows XP :** Le membre de **\_ données dbch** est une valeur **ULong** qui représente le nombre de fois où le média a été modifié depuis le démarrage du système.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_requête d' \_ éjection de média d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Le lecteur du support amovible a reçu une demande de la part de l’utilisateur d’éjecter l’emplacement ou le média spécifié.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID \_ - \_ Suppression de média e/s \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Le support amovible a été supprimé de l’appareil ou n’est pas disponible. Le membre de **\_ données dbch** est un pointeur vers une structure de [**\_ \_ \_ contexte de modification**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) de la classe. Le membre **NewState** fournit des informations d’État. Par exemple, la valeur **MediaUnavailable** indique que le support n’est pas disponible (par exemple, en raison d’une session d’enregistrement active).

**Windows XP :** Le membre de **\_ données dbch** est une valeur **ULong** qui représente le nombre de fois où le média a été modifié depuis le démarrage du système.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_modification du volume d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



Le nom du volume a changé.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_taille de \_ modification du volume e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



La taille du système de fichiers sur le volume a changé.

**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**démontage du \_ volume d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Une tentative de démontage du volume est en cours. Vous devez fermer tous les descripteurs des fichiers et des répertoires sur le volume. Cet événement ne sera pas nécessairement précédé d’un événement **de \_ \_ \_ verrouillage du volume e/s par GUID** .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_échec du \_ démontage du volume d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Une tentative de démontage d’un volume a échoué. Cela se produit souvent parce qu’un autre processus n’a pas pu répondre à l’avis de **\_ \_ \_ démontage du volume d’e/s GUID** en fermant ses Handles en suspens. En raison de l’échec du démontage, vous pouvez rouvrir tous les descripteurs sur le volume affecté.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**changement d’État du volume d' \_ e/s du \_ \_ FVE \_ \_**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



L’état du Chiffrement de lecteur BitLocker du volume a changé. Cet événement est signalé lorsque BitLocker est activé ou désactivé, ou lorsque le chiffrement commence, se termine, s’interrompt ou reprend.

**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_verrou du volume d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

50708874-c9af-11D1-8fef-00a0c9a06d32
</dt> <dt>



Un autre processus tente de verrouiller le volume. Vous devez fermer tous les descripteurs des fichiers et des répertoires sur le volume.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_échec du \_ verrouillage du volume d’e/s du \_ GUID \_**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Une tentative de verrouillage d’un volume a échoué. Cela se produit souvent parce qu’un autre processus n’a pas pu répondre à un événement de **\_ \_ \_ verrouillage du volume e/s par GUID** en fermant ses Handles en suspens. Étant donné que le verrou a échoué, vous pouvez rouvrir tous les descripteurs sur le volume affecté.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montage du volume d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Le volume a été monté par un autre processus. Vous pouvez y accéder à un ou plusieurs descripteurs.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_modification du \_ nom du volume e/s du \_ GUID \_**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



Le nom du volume a été modifié.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**le \_ volume d’e/s GUID a \_ \_ besoin de \_ chkdsk**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Un système de fichiers a détecté une altération sur le volume. L’application doit exécuter CHKDSK sur le volume ou en informer l’utilisateur.

**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_modification de \_ la \_ configuration physique du volume d' \_ e/s du GUID \_**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



La composition physique ou l’état physique actuel du volume a changé.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID du \_ volume d’e/s de \_ préparation d' \_ \_ éjection**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



Le système de fichiers prépare le disque à éjecter. Par exemple, le système de fichiers arrête une opération de mise en forme en arrière-plan ou ferme la session sur un média en écriture unique.

**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_changement d' \_ \_ ID unique \_ du volume d’e/s GUID \_**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



L’identificateur unique du volume a été modifié. Pour plus d’informations sur l’identificateur unique, consultez [**IOCTL \_ MOUNTDEV \_ query \_ unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** cette valeur n’est pas prise en charge jusqu’à Windows Server 2008 R2 et Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**déverrouillage du \_ volume d’e/s GUID \_ \_**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



Le volume a été déverrouillé par un autre processus. Vous pouvez y accéder à un ou plusieurs descripteurs.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID du \_ volume d’e/s du GUID \_ \_ \_**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



Le média est à l’usage. Cet événement est envoyé lorsqu’un système de fichiers détermine que le taux d’erreur sur un volume est trop élevé ou que son espace de remplacement de défauts est presque épuisé.

**Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Les événements du **\_ \_ \_ démontage** du volume d’e/s du GUID et du **\_ \_ \_ démontage \_** du volume d’e/s GUID sont liés, de même que le GUID du **\_ \_ \_ verrou d’e/** s du volume et l' **\_ \_ \_ \_ échec du verrouillage du volume** . Les événements de verrouillage du **\_ volume d’e/ \_ \_** s du volume et d' **\_ e/s \_ \_** GUID indiquent qu’une opération est tentée. Vous devez agir sur la notification d’événement et enregistrer l’action effectuée. Le **\_ démontage du volume d’e/s GUID \_ \_ \_ a échoué** et les événements du **verrou d' \_ e/s du \_ volume en \_ \_ échec** indiquent que l’opération tentée a échoué. Vous pouvez ensuite utiliser votre enregistrement pour annuler les actions que vous avez effectuées en réponse à l’opération.

Le membre **dbch \_ hdevnotify** de la structure de [**\_ \_ handle de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indique l’appareil affecté. Notez qu’il s’agit du handle de notification de l’appareil retourné par [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), et non pas d’un handle de volume. Pour effectuer des opérations sur le volume, mappez ce handle au handle de volume correspondant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>IoEvent. h</dt> </dl> |



 

