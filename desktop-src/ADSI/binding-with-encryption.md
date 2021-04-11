---
title: Liaison avec chiffrement
description: Les données sensibles échangées sur un réseau doivent être chiffrées.
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation, liaison avec chiffrement
- Liaison avec chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf19747a8356459f4ab50c0aa409f69b58eb224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939604"
---
# <a name="binding-with-encryption"></a>Liaison avec chiffrement

Les données sensibles échangées sur un réseau doivent être chiffrées. Pour ce faire, ADSI prend en charge deux types de chiffrement, Kerberos et SSL (Secure Sockets Layer) (SSL). Les deux types de chiffrement requièrent l’utilisation de [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) pour la liaison.

Les fonctions **GetObject** et [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ne peuvent pas être utilisées pour la liaison dans ce cas, car elles provoquent des requêtes LDAP utilisées par ADSI et des données retournées par le serveur d’annuaire à transmettre sur le réseau sous forme de texte en clair. À des fins de débogage, il est utile de désactiver le chiffrement afin que le Moniteur réseau puisse être utilisé pour afficher les demandes et les données LDAP entre le client et le serveur d’annuaire.

## <a name="kerberos-based-encryption"></a>Chiffrement basé sur Kerberos

Pour utiliser le chiffrement basé sur Kerberos, spécifiez l’indicateur d' **\_ \_ étanchéité d’utilisation ADS** lors de l’appel de [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). L’indicateur d' **\_ \_ étanchéité utiliser des publicités** peut également être utilisé pour vérifier l’intégrité des données, c’est-à-dire pour s’assurer que les données reçues sont les mêmes que celles envoyées. Si l’indicateur d' **\_ \_ étanchéité d’utilisation ADS** est spécifié, l’indicateur d’utilisation de la **\_ \_ signature ADS** est automatiquement spécifié. Les deux indicateurs requièrent l’authentification Kerberos, qui ne fonctionne que dans les conditions suivantes :

-   L’ordinateur client doit être connecté au domaine Windows ou à un domaine approuvé par un domaine Windows.
-   [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) doit être appelé avec des informations d’identification null ; autrement dit, les autres informations d’identification ne peuvent pas être spécifiées.

## <a name="ssl-based-encryption"></a>Chiffrement SSL

Pour utiliser le chiffrement SSL, spécifiez l’indicateur **\_ \_ SSL Use SSL** lors de l’appel de [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Si seule l' **indicateur \_ \_ SSL Use SSL** est spécifié, ADSI ouvre le port SSL 636, puis effectue une liaison simple sur ce canal SSL. Si l' **\_ \_ authentification sécurisée ADS** et les **publicités utilisent des indicateurs \_ \_ SSL** spécifiés, le comportement de liaison dépend du client à partir duquel l’appel est effectué. Sur les versions non prises en charge de Windows, ADSI a ouvert un canal SSL pour la première fois et effectue une liaison simple à l’aide du nom d’utilisateur et du mot de passe spécifiés ou du contexte de l’utilisateur actuel si le nom d’utilisateur et le mot de passe ont la valeur null. Sur les versions prises en charge de Windows, ADSI effectue une authentification sécurisée plutôt qu’une simple liaison.

Pour utiliser le chiffrement SSL lors de la communication avec Active Directory, Active Directory doit avoir activé l’infrastructure à clé publique (PKI). L’infrastructure à clé publique peut être activée en configurant une autorité de certification d’entreprise sur l’un des serveurs de Active Directory, y compris l’un des serveurs Active Directory eux-mêmes. Si vous configurez une autorité de certification d’entreprise, un serveur Active Directory obtient un certificat de serveur qui peut ensuite être utilisé pour effectuer un chiffrement SSL.

 

 




