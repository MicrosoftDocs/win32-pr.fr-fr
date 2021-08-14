---
description: 'Les constantes RENDBIND sont des indicateurs utilisés par la méthode ITDirectory :: bind pour indiquer les types d’authentification fournis.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c618ed2cf5d9dda4c2ee14b331e3603f8021e9c5f4755e38ecfb5929b5f45c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760862"
---
# <a name="rendbind_-constants"></a>\_Constantes RENDBIND

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les constantes RENDBIND sont des indicateurs utilisés par la méthode [**ITDirectory :: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) pour indiquer les types d’authentification fournis.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**\_authentification RENDBIND**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Authentifier l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Utilisez le nom de domaine par défaut.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Utilisez le nom d’utilisateur par défaut.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Utilisez le mot de passe par défaut.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Les trois précédents, ensemble, pour des raisons pratiques.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>Rend. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory :: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




