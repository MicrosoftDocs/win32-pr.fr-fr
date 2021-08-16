---
title: Définition de la sécurité au niveau du proxy d’interface
description: Parfois, le client a besoin d’un contrôle affiné sur la sécurité des appels à des interfaces particulières.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef969039dcfdc12449b7a8d0a3d63729ab5f84061ade1a743d21a1b6b34331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309094"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Définition de la sécurité au niveau du proxy d’interface

Parfois, le client a besoin d’un contrôle affiné sur la sécurité des appels à des interfaces particulières. Par exemple, la sécurité peut être définie à un niveau bas pour le processus, mais les appels à une interface particulière peuvent nécessiter un niveau d’authentification plus élevé, tel que le chiffrement. Les méthodes de l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) permettent au client de modifier les paramètres de sécurité associés aux appels à une interface particulière en contrôlant les paramètres de sécurité au niveau de l’interface-proxy.

Le client peut interroger un objet existant pour [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) , puis appeler la méthode [**IClientSecurity :: QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) pour connaître les paramètres de sécurité actuels pour un proxy d’interface particulier. La méthode [**IClientSecurity :: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) peut être utilisée pour modifier les paramètres de sécurité d’un proxy d’interface individuel sur l’objet avant d’appeler l’une des méthodes de l’interface. Les nouveaux paramètres s’appliquent à tous les appelants ultérieurs de cette interface particulière. La méthode [**IClientSecurity :: CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) permet au client de copier un proxy d’interface afin que les appels suivants à **SetBlanket** sur la copie n’affectent pas les appelants du proxy d’origine.

[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) est couramment utilisé pour élever le niveau d’authentification d’un proxy d’interface particulier à un niveau de protection de sécurité plus élevé. Toutefois, dans certaines situations, il peut également être utile de réduire le niveau d’authentification pour un proxy d’interface particulier. Par exemple, supposons que le niveau d’authentification par défaut pour le processus soit une valeur autre que le niveau d’authentification RPC \_ C \_ \_ \_ aucun et que le client et le serveur se trouvent dans des domaines distincts qui ne s’approuvent pas mutuellement. Dans ce cas, les appels au serveur échouent, à moins que le client n’appelle **SetBlanket** pour réduire le niveau d’authentification au niveau d’authentification RPC \_ C « aucun » \_ \_ \_ .

Les clients qui utilisent l’implémentation par défaut de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) fournie par le gestionnaire proxy peuvent appeler les fonctions d’assistance [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)et [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) au lieu d’appeler directement les méthodes **IClientSecurity** . Les fonctions d’assistance simplifient le code, mais sont légèrement moins efficaces que l’appel direct des méthodes **IClientSecurity** correspondantes.

L’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) est implémentée localement pour le client par le gestionnaire proxy. Certains objets marshalés personnalisés ne prennent peut-être pas en charge **IClientSecurity**.

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) fonctionne avec tous les services d’authentification pris en charge (actuellement NTLMSSP, Schannel et le protocole Kerberos V5).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 