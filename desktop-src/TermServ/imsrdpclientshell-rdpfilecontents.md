---
title: IMsRdpClientShell propriété RdpFileContents
description: Spécifie ou récupère le contenu du fichier protocole RDP (Remote Desktop Protocol) (RDP) à lancer à partir d’Bureau à distance Accès web (RD Accès web) ou d’un autre portail Web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RdpFileContents
- Services Bureau à distance de la propriété RdpFileContents, interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, propriété RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509932"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>IMsRdpClientShell :: RdpFileContents, propriété

Spécifie ou récupère le contenu du fichier protocole RDP (Remote Desktop Protocol) (RDP) à lancer à partir d’Bureau à distance Accès web (RD Accès web) ou d’un autre portail Web.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le contenu du fichier RDP à lancer à partir du portail Web.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





