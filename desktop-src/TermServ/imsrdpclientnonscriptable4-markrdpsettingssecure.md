---
title: IMsRdpClientNonScriptable4 propriété MarkRdpSettingsSecure
description: Spécifie si les paramètres de protocole RDP (Remote Desktop Protocol) (RDP) sont marqués comme sécurisés.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété MarkRdpSettingsSecure
- Services Bureau à distance de la propriété MarkRdpSettingsSecure, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété MarkRdpSettingsSecure
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508766"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a>IMsRdpClientNonScriptable4 :: MarkRdpSettingsSecure, propriété

Spécifie si les paramètres de [protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md) (RDP) sont marqués comme sécurisés. Cela indique que les paramètres appliqués au contrôle ont été signés par un éditeur tiers ou approuvé.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit si les paramètres RDP sont marqués comme sécurisés.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





