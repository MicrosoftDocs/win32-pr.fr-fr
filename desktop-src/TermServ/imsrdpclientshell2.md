---
title: Interface IMsRdpClientShell2
description: Expose les propriétés qui lancent le client Connexion Bureau à distance à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientShell2
- Services Bureau à distance de l’interface IMsRdpClientShell2, Description
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740549"
---
# <a name="imsrdpclientshell2-interface"></a>Interface IMsRdpClientShell2

Expose les propriétés qui lancent le client Connexion Bureau à distance à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.

Cette interface est implémentée par le contrôle Services Bureau à distance Accès web, qui est un wrapper autour du client Connexion Bureau à distance (MsTscAx.dll) et du proxy d’exécution des connexions aux programmes RemoteApp et aux services Bureau à reconnexion (Tswbprxy.exe).

## <a name="members"></a>Membres

L’interface **IMsRdpClientShell2** hérite de **IMsRdpClientShell**. **IMsRdpClientShell2** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientShell2** possède les propriétés suivantes.



| Propriété                                                                               | Type d’accès          | Description                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Lecture seule<br/> | Récupère un pointeur vers l’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , qui est utilisée pour gérer les informations d’identification et les connexions de connexions aux programmes RemoteApp et aux services Bureau à distance.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Lecture seule<br/> | Récupère une valeur qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.<br/>                                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 





