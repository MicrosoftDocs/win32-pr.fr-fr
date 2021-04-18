---
title: Comparaison de fonctions Windows 2000 et redistribuable RRAS
description: L’API RAS est distribuée en tant que fonctionnalité des systèmes d’exploitation Windows 2000 et versions ultérieures et est disponible en tant que redistribuable pour Windows NT 4,0 avec Service Pack 3 (SP3) et versions antérieures.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511852"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a>Comparaison de fonctions : Windows 2000 et le package redistribuable RRAS

L’API RAS est distribuée en tant que fonctionnalité des systèmes d’exploitation Windows 2000 et versions ultérieures et est disponible en tant que redistribuable pour Windows NT 4,0 avec Service Pack 3 (SP3) et versions antérieures. RAS offre les mêmes fonctionnalités dans ces deux formes, mais la Convention d’affectation de noms utilisée est différente pour les éléments de référence dans chaque version de l’API RAS.

Les fonctions RAS pour Windows NT 4,0 avec SP3 et les versions antérieures commencent généralement par le préfixe « RasAdmin ». Les fonctions analogues pour le service Routage et accès à distance (RRAS) commencent par le préfixe « MprAdmin ». Par exemple, RAS fournit une fonction appelée [**RasAdminPortGetInfo**](rasadminportgetinfo.md). La fonction analogue dans RRAS est appelée [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo). À titre d’exemple similaire, RAS fournit la fonction de rappel [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md). RRAS fournit une fonction de rappel similaire appelée [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser). Les exceptions à cette règle sont [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), qui sous RRAS est [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)et [**RasAdminFreeBuffer**](rasadminfreebuffer.md), qui sous RRAS est [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).

Le tableau suivant répertorie les fonctions RAS Windows NT 4,0 SP3 et les fonctions RRAS correspondantes.



| RAS Windows NT 4,0                                                                   | RRAS                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)                   | [**MprAdminAcceptNewConnection**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md) | [**MprAdminConnectionHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [**RasAdminFreeBuffer**](rasadminfreebuffer.md)                                     | [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [**RasAdminGetErrorString**](rasadmingeterrorstring.md)                             | [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)                   | [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)                   | [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [**RasAdminPortDisconnect**](rasadminportdisconnect.md)                             | [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [**RasAdminPortEnum**](rasadminportenum.md)                                         | [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [**RasAdminPortGetInfo**](rasadminportgetinfo.md)                                   | [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [**RasAdminReleaseIpAddress**](rasadminreleaseipaddress.md)                         | [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [**RasAdminUserGetInfo**](rasadminusergetinfo.md)                                   | [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [**RasAdminUserSetInfo**](rasadminusersetinfo.md)                                   | [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

Bien que les fonctions RRAS soient similaires à celles de Windows NT 4,0 avec SP3 et des équivalents RAS antérieurs dans les fonctionnalités, les fonctions RRAS utilisent souvent un ensemble de paramètres différent. Pour obtenir des informations complètes sur la liste de paramètres de cette fonction, consultez la page de référence pour une fonction particulière.

Le redistribuable RRAS pour Windows NT 4,0 avec SP3 et les versions antérieures ajoute les fonctions suivantes, qui n’ont pas d’équivalents RAS :

[**MprAdminAcceptNewLink**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[**MprAdminLinkHangupNotification**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Outre les fonctions précédentes, les systèmes d’exploitation Windows 2000 et versions ultérieures ajoutent les fonctions suivantes :

[**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[**MprAdminAcceptNewConnection2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[**MprAdminConnectionHangupNotification2**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




