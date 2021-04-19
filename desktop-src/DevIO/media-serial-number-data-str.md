---
description: Contient le numéro de série d’un périphérique USB. Elle est utilisée par le \_ Code de contrôle du numéro de série du support de stockage IOCTL \_ \_ \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Structure MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539788"
---
# <a name="media_serial_number_data-structure"></a>\_Structure de \_ données du numéro de série du support \_

Contient le numéro de série d’un périphérique USB. Elle est utilisée par le code de contrôle du [**\_ numéro de \_ \_ \_ série \_ du support de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**SerialNumberLength**
</dt> <dd>

Taille de la chaîne **SerialNumberData** , en octets.

</dd> <dt>

**Résultat**
</dt> <dd>

État de la demande.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**SerialNumberData**
</dt> <dd>

Numéro de série de l’appareil.

</dd> </dl>

## <a name="remarks"></a>Notes

Aucun fichier d’en-tête n’est disponible pour la structure de **données du numéro de série du support \_ \_ \_** . Incluez la définition de la structure en haut de cette page dans votre code source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>          |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_numéro de \_ série du support d’extraction du stockage IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




