---
title: Message ICM_GETINFO (VFW. h)
description: Le \_ message ICM GETINFO interroge un pilote de compression vidéo pour retourner une description de lui-même dans une structure ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- Message ICM_GETINFO Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511156"
---
# <a name="icm_getinfo-message"></a>\_Message ICM GETINFO

Le message **ICM \_ GETINFO** interroge un pilote de compression vidéo pour retourner une description de lui-même dans une structure [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*
</dt> <dd>

Pointeur vers une structure **ICINFO** pour contenir des informations.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de **ICINFO**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la taille, en octets, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ou zéro si une erreur se produit.

## <a name="remarks"></a>Notes

En règle générale, les applications envoient ce message pour afficher la liste des compresseurs installés.

Le pilote doit remplir tous les membres de la structure [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , à l’exception de **szDriver**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





