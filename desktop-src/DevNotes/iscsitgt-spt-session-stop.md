---
description: Utilisé avec l' \_ IOCTL SCSI \_ miniport IOCTL et le \_ \_ \_ \_ Code de contrôle 0x101 (CTLCODE ISCSITGT SPT session end) pour arrêter une session.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: Structure ISCSITGT_SPT_SESSION_STOP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: dba4c54e6fbae3ef947ec5ac5f5c4b178434566d15cc0591104dd38a8e456fb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001479"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>\_Structure d' \_ arrêt de session SPT ISCSITGT \_

\[la structure suivante peut être utilisée dans Windows Server 2012 R2. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

Utilisé avec l' [**IOCTL \_ SCSI \_ miniport**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL et le \_ \_ \_ \_ Code de contrôle 0x101 (CTLCODE ISCSITGT SPT session end) pour arrêter une session.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>Membres

<dl> <dt>

**En-tête**
</dt> <dd>

En-tête obligatoire.

</dd> <dt>

**ITNexusHandle**
</dt> <dd>

Handle opaque représentant une session.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                               |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Transfert de cible iSCSI](/powershell/module/iscsi)
</dt> <dt>

[**\_contrôle d’e/s SRB \_**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
