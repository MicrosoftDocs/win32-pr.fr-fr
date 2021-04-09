---
description: Décrit les données de l’objet récepteur d’affichage incluses dans une notification ou un résultat de notification.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Structure WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864809"
---
# <a name="wfd_display_sink_object_header-structure"></a>\_Structure d' \_ \_ \_ en-tête d’objet récepteur WFD

La structure d' **\_ \_ \_ \_ en-tête d’objet du récepteur d’affichage WFD** décrit les données de l’objet récepteur d’affichage incluses dans une notification ou un résultat de notification.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Type de l’objet récepteur d’affichage. Vous pouvez utiliser le type d' **objet récepteur d’affichage WFD identifiant le \_ \_ \_ \_ \_ paramètre par défaut** , qui est défini comme valeur 1.

</dd> <dt>

**Faisant**
</dt> <dd>

Version de révision de l’objet récepteur d’affichage. Vous pouvez utiliser la révision de l’objet récepteur de l’identificateur **WFD, \_ \_ \_ \_ \_ version \_ 1** , qui est définie comme valeur 1.

</dd> <dt>

**Durée**
</dt> <dd>

Longueur des données dans la notification ou le résultat de la notification.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl> |



 

 




