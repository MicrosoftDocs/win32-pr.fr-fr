---
title: Énumération WMDM_SESSION_TYPE
description: Le type \_ d' \_ énumération de type de session WMDM définit le type de session.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4e3d3d774667ca0c7026caa05609efd69443e00c0c2e273a1e6ad0ac086aa9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055527"
---
# <a name="wmdm_session_type-enumeration"></a>\_Énumération des types de session WMDM \_

Le type d’énumération de **\_ \_ type de session WMDM** définit le type de session.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ session \_ None**
</dt> <dd>

La session n’est pas définie.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_transfert de la session WMDM \_ sur l' \_ \_ appareil**
</dt> <dd>

La session est définie comme transfert de données vers l’appareil.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ transfert de session WMDM \_ à partir de l' \_ appareil**
</dt> <dd>

La session est définie comme transfert de données à partir de l’appareil.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**suppression de la \_ session WMDM \_**
</dt> <dd>

La session est définie en tant que suppression de données.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_session WMDM \_ personnalisée**
</dt> <dd>

La session est définie en tant que session personnalisée.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> </dl>

 

 





