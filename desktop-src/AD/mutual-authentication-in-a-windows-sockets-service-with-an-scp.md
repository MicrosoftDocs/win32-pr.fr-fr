---
title: Authentification mutuelle dans un service Windows Sockets avec SCP
description: Les rubriques de cette section incluent des exemples de code qui montrent comment effectuer une authentification mutuelle avec un service qui se publie lui-même à l’aide d’un point de connexion de service (SCP).
ms.assetid: f730464c-95ac-4285-960c-18862f6f7852
ms.tgt_platform: multiple
keywords:
- Authentification mutuelle dans un service Windows Sockets avec une publicité SCP
- Active Directory, utilisation de, authentification mutuelle, service Windows Sockets avec un SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527715c4a35dc15cd67f5820e6fa891b56452399
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842061"
---
# <a name="mutual-authentication-in-a-windows-sockets-service-with-scp"></a>Authentification mutuelle dans un service Windows Sockets avec SCP

Les rubriques de cette section incluent des exemples de code qui montrent comment effectuer une authentification mutuelle avec un service qui se publie lui-même à l’aide d’un point de connexion de service (SCP). Les exemples sont basés sur un service Microsoft Windows Sockets qui utilise un package SSPI pour gérer la négociation de l’authentification mutuelle entre un client et le service. Utilisez les procédures suivantes pour implémenter l’authentification mutuelle dans ce scénario.

**Pour inscrire des noms de principal du service dans un répertoire lors de l’installation d’un service**

1.  Appelez la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour composer des noms de principal du service (SPN) pour le service.
2.  Appelez la fonction [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) pour enregistrer les noms de principal du service sur le compte de service ou le compte d’ordinateur dans le contexte duquel le service s’exécutera. Cette étape doit être effectuée par un administrateur de domaine. une exception est qu’un service s’exécutant sous le compte LocalSystem peut inscrire son SPN sous la forme « <service class> / <host> » sur le compte d’ordinateur de l’hôte de service.

**Pour vérifier la configuration au démarrage du service**

-   Vérifiez que les SPN appropriés sont enregistrés sur le compte sous lequel le service est en cours d’exécution. Pour plus d’informations, consultez [tâches de maintenance de compte d’ouverture de session](logon-account-maintenance-tasks.md).

**Pour authentifier le service au démarrage du client**

1.  Récupérez les données de connexion du point de connexion de service du service.
2.  Établissez une connexion au service.
3.  Appelez la fonction [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) pour composer un SPN pour le service. Composez le nom de principal du service à partir de la chaîne de classe de service connue et les données récupérées à partir du point de connexion de service. Ces données incluent le nom d’hôte du serveur sur lequel le service est en cours d’exécution. N’oubliez pas que le nom d’hôte doit être un nom DNS.
4.  Utilisez un package de sécurité SSPI pour effectuer l’authentification :
    1.  Appelez la fonction [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) pour obtenir les informations d’identification du client.
    2.  Transmettez les informations d’identification du client et le SPN à la fonction [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) pour générer un objet blob de sécurité à envoyer au service à des fins d’authentification. Définissez l’indicateur d’authentification **\_ \_ mutuelle \_ d’ISC req** pour demander l’authentification mutuelle.
    3.  Échangez des objets BLOB avec le service jusqu’à ce que l’authentification soit terminée.
5.  Vérifiez le masque des fonctionnalités renvoyées pour l’indicateur d’authentification **\_ \_ mutuelle \_ req req** pour vérifier que l’authentification mutuelle a été effectuée.
6.  Si l’authentification a réussi, échangez le trafic avec le service authentifié. Utilisez la signature numérique pour vous assurer que les messages entre le client et le service n’ont pas été falsifiés. À moins que les exigences en matière de performances ne soient graves, utilisez le chiffrement. Pour plus d’informations et pour obtenir un exemple de code qui montre comment utiliser les fonctions [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)et [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) dans un package SSPI, consultez [garantie de l’intégrité des communications pendant l’échange de messages](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

**Pour authentifier le client par le service lorsqu’un client se connecte**

1.  Chargez un package de sécurité SSPI qui prend en charge l’authentification mutuelle.
2.  Lorsqu’un client se connecte, utilisez le package de sécurité pour effectuer l’authentification :
    1.  Appelez la fonction [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) pour obtenir les informations d’identification du service.
    2.  Transmettez les informations d’identification du service et l’objet blob de sécurité reçues du client à la fonction [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) pour générer un objet blob de sécurité à renvoyer au client.
    3.  Échangez des objets BLOB avec le client jusqu’à ce que l’authentification soit terminée.
3.  Vérifiez le masque des fonctionnalités renvoyées pour l’indicateur d’authentification **\_ \_ mutuelle \_ ASC RET** afin de vérifier que l’authentification mutuelle a été effectuée.
4.  Si l’authentification a réussi, échangez le trafic avec le client authentifié. Utilisez la signature numérique et le chiffrement, sauf si les performances sont un problème.

Pour plus d’informations et pour obtenir un exemple de code pour ce scénario d’authentification mutuelle, consultez :

-   [Comment un client authentifie un service Windows Sockets SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md)
-   [Composition et inscription de SPN pour un service Windows Sockets SCP](composing-and-registering-spns-for-an-scp-based-windows-sockets-service.md)
-   [Comment un service Windows Sockets authentifie un client](how-a-windows-sockets-service-authenticates-a-client.md)

Pour plus d’informations, consultez :

-   [Publication avec des points de connexion de service](publishing-with-service-connection-points.md)
-   [Documentation SSPI](/windows/desktop/SecAuthN/sspi)
-   [Documentation Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)

 

 