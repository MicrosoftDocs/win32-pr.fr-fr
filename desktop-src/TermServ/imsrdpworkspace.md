---
title: Interface IMsRdpWorkspace
description: Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpWorkspace
- Services Bureau à distance de l’interface IMsRdpWorkspace, Description
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1489690632b0ef1bf05a529d84ed5c96afb6c442c82744f964c9a89e9286299d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125529"
---
# <a name="imsrdpworkspace-interface"></a>Interface IMsRdpWorkspace

Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance. Cette interface est implémentée par le contrôle Services Bureau à distance Accès web. Ce contrôle est un wrapper autour du client Connexion Bureau à distance (MsTscAx.dll) et du proxy d’exécution des connexions aux programmes RemoteApp et aux services Bureau à la connexion (Tswbprxy.exe).

## <a name="members"></a>Membres

L’interface **IMsRdpWorkspace** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpWorkspace** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpWorkspace** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | Supprime les informations d’identification de l’utilisateur associées à l’ID de connexion spécifié.<br/>                                                                                  |
| [**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | Déconnecte toutes les connexions existantes associées à l’ID de connexion spécifié et supprime les informations d’identification de l’utilisateur correspondant de la Banque d’informations d’identification.<br/> |
| [**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | Détermine si les informations d’identification de l’utilisateur existent pour l’ID de connexion spécifié.<br/>                                                                                 |
| [**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | Détermine si l’authentification unique (SSO) est activée pour Connexions aux programmes RemoteApp et aux services Bureau à distance.<br/>                                                                   |
| [**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | Marque l’authentification des informations d’identification de l’utilisateur pour l’ID de connexion, puis affiche la notification de connexion dans la zone de notification de la barre des tâches. <br/>     |
| [**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | Associe les informations d’identification de l’utilisateur et les certificats à un ID de connexion.<br/>                                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace est défini en tant que 145D0621-04CF-4FC2-A766-A81A9069CDF8<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

