---
title: Interface IMsRdpClientShell
description: Les paramètres client Connexion Bureau à distance (RDC) utilisés pour lancer le client à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, Description
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8593a890097bbfaf6d9c9876bb56d92794ce204f38f349c72beb73b8d28403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621029"
---
# <a name="imsrdpclientshell-interface"></a>Interface IMsRdpClientShell

Les paramètres client Connexion Bureau à distance (RDC) utilisés pour lancer le client à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.

## <a name="members"></a>Membres

L’interface **IMsRdpClientShell** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpClientShell** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClientShell** possède ces méthodes.



| Méthode                                                     | Description                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Récupère une propriété RDP unique.<br/>                  |
| [**Lancer**](imsrdpclientshell-launch.md)                 | Lance le contenu du fichier distant à partir du portail Web.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Définit une propriété RDP unique.<br/>                       |



 

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientShell** possède les propriétés suivantes.



| Propriété                                                                                              | Type d’accès           | Description                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Lecture seule<br/>  | Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp.<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lecture/écriture<br/> | Récupère si le mode public est activé.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lecture/écriture<br/> | Version de flux du fichier de configuration RDP.<br/>                                                  |



 

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

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

