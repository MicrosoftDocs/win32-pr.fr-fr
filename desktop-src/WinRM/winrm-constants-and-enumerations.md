---
title: Constantes et énumérations WinRM
description: Windows La gestion à distance comporte des indicateurs binaires utilisés pour la création de sessions et d’énumérations, ainsi que pour les types d’accès et l’authentification à un serveur proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742935"
---
# <a name="winrm-constants-and-enumerations"></a>Constantes et énumérations WinRM

Windows La gestion à distance comporte des indicateurs binaires utilisés pour la création de sessions et d’énumérations, ainsi que pour les types d’accès et l’authentification à un serveur proxy. La liste suivante répertorie les différents indicateurs binaires.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Constantes de session](session-constants.md)
</dt> <dd>

Indicateurs utilisés dans le paramètre *Flags* des méthodes [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) .

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Constantes d’énumération**](enumeration-constants.md)
</dt> <dd>

Indicateurs utilisés dans le paramètre *Flags* de l’appel à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Indicateurs utilisés dans le paramètre *authenticationMechanism* de l’appel à [**IWSManConnectionOptionsEx2 :: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Indicateurs utilisés dans le paramètre *accessType* de l’appel à [**IWSManConnectionOptionsEx2 :: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Informations de référence sur la gestion à distance](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2 :: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




