---
title: Interface IMsRdpPreferredRedirectionInfo
description: Fournit une propriété pour contrôler à l’aide d’un serveur de redirection.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpPreferredRedirectionInfo
- Services Bureau à distance de l’interface IMsRdpPreferredRedirectionInfo, Description
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464575"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a>Interface IMsRdpPreferredRedirectionInfo

Fournit une propriété pour contrôler à l’aide d’un serveur de redirection.

## <a name="members"></a>Membres

L’interface **IMsRdpPreferredRedirectionInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpPreferredRedirectionInfo** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpPreferredRedirectionInfo** possède les propriétés suivantes.



| Propriété                                                                                               | Type d’accès           | Description                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**UseRedirectionServerName**](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | Lecture/écriture<br/> | Obtient et définit s’il faut utiliser le nom du serveur de redirection.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpPreferredRedirectionInfo est défini en tant que FDD029F9-9574-4def-8529-64B521CCCAA4<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

