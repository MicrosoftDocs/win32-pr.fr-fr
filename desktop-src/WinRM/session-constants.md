---
title: Constantes de session
description: Les constantes de session dans l' \_ \_ énumération WSManSessionFlags spécifient l’authentification et d’autres informations pour les appels WSMan. CreateSession ou IWSMan CreateSession qui se connectent à un ordinateur distant.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584eb15c4b235a006b52551de8f9999ddb65459412af68db81f0500a0828888b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743224"
---
# <a name="session-constants"></a>Constantes de session

Les constantes de session dans l’énumération **\_ \_ WSManSessionFlags** spécifient l’authentification et d’autres informations pour les appels [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) qui se connectent à un ordinateur distant. Ces constantes sont également étroitement liées aux commutateurs de l’outil en ligne de commande **WinRM** .

## <a name="using-session-constants"></a>Utilisation de constantes de session

Vous pouvez définir les indicateurs de session pour l’appel à [**WSMan. CreateSession**](wsman-createsession.md) de deux façons différentes. L’un est plus rapide et plus simple. La méthode la plus longue, comme indiqué dans l’exemple suivant, consiste à localiser la valeur de l’indicateur que vous souhaitez utiliser et à créer dans votre script une constante avec cette valeur. La constante est ensuite utilisée pour définir la valeur du paramètre *IFlags* .

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

La méthode recommandée, comme indiqué dans l’exemple suivant, consiste à utiliser la méthode d’objet [**WSMan**](wsman.md) associée à l’indicateur.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes d’authentification**](authentication-constants.md)
</dt> <dd>

Spécifiez la méthode d’authentification et la manière de gérer les serveurs de certificats.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Autres constantes de session**](other-session-constants.md)
</dt> <dd>

Spécifiez l’encodage, le chiffrement et le port du nom de principal du service.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes et énumérations WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Authentification des connexions à distance](authentication-for-remote-connections.md)
</dt> </dl>

 

 




