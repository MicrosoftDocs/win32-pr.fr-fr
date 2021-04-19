---
description: 'Le WiaTransferParams est transmis à une application lors d’un transfert de données par le système d’exécution WIA (Windows Image Acquisition) à la méthode IWiaTransferCallback :: TransferCallback.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: WiaTransferParams, structure (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516883"
---
# <a name="wiatransferparams-structure"></a>WiaTransferParams, structure

Le **WiaTransferParams** est transmis à une application lors d’un transfert de données par le système d’exécution WIA (Windows Image Acquisition) à la méthode [**IWiaTransferCallback :: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>Membres

<dl> <dt>

**lMessage**
</dt> <dd>

Type : **long**

</dd> <dd>

Indique l’état du transfert de données.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_État du \_ message de transfert WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ fin \_ du flux de messages de transfert WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fin \_ du transfert du message \_ WIA Transfer**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**État de l’appareil de message de \_ transfert WIA \_ \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ page nouveau message de transfert WIA \_**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Type : **long**

</dd> <dd>

Indique la progression du transfert de données sous la forme d’un pourcentage.

</dd> <dt>

**ulTransferredBytes**
</dt> <dd>

Type : **ULONG64**

</dd> <dd>

Indique la quantité de données transférées.

</dd> <dt>

**hrErrorStatus**
</dt> <dd>

Type : **HRESULT**

</dd> <dd>

État ou état d’erreur de l’appareil défini par le pilote ; par exemple, « préchauffage ».

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




