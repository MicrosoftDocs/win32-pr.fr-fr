---
description: Contient les paramètres de configuration EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Structure EAPOL_INTF_PARAMS (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537036"
---
# <a name="eapol_intf_params-structure"></a>Structure de \_ paramètres EAPOL INTF \_

\[**EAPOL \_ Les \_ paramètres INTF** ne sont plus pris en charge à partir de Windows Vista et windows Server 2008. Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires. Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

Contient les paramètres de configuration EAPOL.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Version de l’appelant. La valeur par défaut est 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Réservé pour un usage futur.

</dd> <dt>

**dwEapFlags**
</dt> <dd>

Non utilisé.

</dd> <dt>

**dwEapType**
</dt> <dd>

Type d’extension EAP à utiliser. Définissez sur 0x00000013 pour EAP-TLS et 0x00000026 pour PEAP.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Taille de l’identificateur réseau.

</dd> <dt>

**bSSID**
</dt> <dd>

Identificateur réseau.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fichier d’en-tête wzcsapi. h n’est pas disponible dans le SDK Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                       |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




