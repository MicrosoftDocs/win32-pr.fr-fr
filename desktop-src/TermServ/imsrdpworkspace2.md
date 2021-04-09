---
title: Interface IMsRdpWorkspace2
description: Expose une méthode qui associe Connexions aux programmes RemoteApp et aux services Bureau à distance informations d’identification à une connexion.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032787"
---
# <a name="imsrdpworkspace2-interface"></a>Interface IMsRdpWorkspace2

Expose une méthode qui associe Connexions aux programmes RemoteApp et aux services Bureau à distance informations d’identification à une connexion. Cette interface est implémentée par le contrôle Services Bureau à distance Accès web. Ce contrôle est un wrapper autour du client Connexion Bureau à distance (MsTscAx.dll) et du proxy d’exécution des connexions aux programmes RemoteApp et aux services Bureau à la connexion (Tswbprxy.exe).

## <a name="members"></a>Membres

L’interface **IMsRdpWorkspace** hérite de [**IMsRdpWorkspace**](imsrdpworkspace.md). **IMsRdpWorkspace2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpWorkspace** possède ces méthodes.



| Méthode                                                        | Description                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Associe les informations d’identification de l’utilisateur et les certificats à un ID de connexion. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 est défini en tant que 145D0622-04CF-4FC3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

