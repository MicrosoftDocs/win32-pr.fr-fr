---
description: 'Les constantes RENDBIND sont des indicateurs utilisés par la méthode ITDirectory :: bind pour indiquer les types d’authentification fournis.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525558"
---
# <a name="rendbind_-constants"></a>\_Constantes RENDBIND

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

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

 

 




