---
description: La fonction GetCaptureMacType retourne le type MAC d’une capture donnée.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: GetCaptureMacType, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4405d1b0c5618951360c8b22732796dffdffeb557849388159411c9a17924591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910799"
---
# <a name="getcapturemactype-function"></a>GetCaptureMacType fonction)

La fonction **GetCaptureMacType** retourne le type Mac d’une capture donnée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCapture* \[ dans\]
</dt> <dd>

Handle de la capture. Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **GetCaptureMacType** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est l’un des types MAC suivants.

-   \_type Mac \_ inconnu
-   MAC \_ type \_ Ethernet
-   \_type Mac \_ TOKENRING
-   \_type Mac \_ FDDI

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                              | Description                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**\_type Mac \_ NMERR \_ inconnu**</dt> </dl> | Moniteur réseau n’a pas pu trouver un type MAC connu.<br/> |



 

## <a name="remarks"></a>Remarques

Le descripteur de la capture peut être obtenu de plusieurs façons, en fonction de la personne qui effectue l’appel. Pour les experts, le descripteur est spécifié dans le membre **hCapture** de la structure [EXPERTSTARTUPINFO](expertstartupinfo.md) . Pour les analyseurs, le handle de capture peut être obtenu en appelant la fonction [GetFrameCaptureHandle](getframecapturehandle.md) .

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureMacType** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




