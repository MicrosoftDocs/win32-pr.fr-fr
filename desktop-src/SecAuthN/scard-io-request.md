---
description: La structure des \_ demandes d’e/s en cicatrices \_ commence une structure d’informations de contrôle de protocole.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Structure SCARD_IO_REQUEST (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: 9a377643e794b679be593bb99b8750698c92dd3aa8abacd79bfdb1c478c9c7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918885"
---
# <a name="scard_io_request-structure"></a>Structure de \_ demande d’e/s en cicatrice \_

La structure des **\_ \_ demandes d’e/s en cicatrices** commence une structure d’informations de contrôle de protocole. Toutes les informations spécifiques au protocole suivent immédiatement cette structure. La longueur totale de la structure doit être alignée avec la taille de mot de l’architecture matérielle sous-jacente. Par exemple, dans Win32, la longueur de toutes les informations PCI doit être un multiple de quatre octets afin qu’il s’aligne sur une limite de 32 bits.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwProtocol**
</dt> <dd>

Protocole en cours d’utilisation.

</dd> <dt>

**cbPciLength**
</dt> <dd>

Longueur, en octets, de la structure de **\_ \_ demande d’e/s en cicatrices** plus les informations spécifiques au PCI suivantes.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Winsmcrd. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




