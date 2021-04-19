---
description: Les clients NLA peuvent enregistrer les informations de configuration du réseau à l’échelle du système, ce qui permet aux futures requêtes de retourner les informations de configuration spécifiées, que le réseau soit actif ou non.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Inscription d’une instance de service avec NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545809"
---
# <a name="registering-a-service-instance-with-nla"></a>Inscription d’une instance de service avec NLA

Les clients NLA peuvent enregistrer les informations de configuration du réseau à l’échelle du système, ce qui permet aux futures requêtes de retourner les informations de configuration spécifiées, que le réseau soit actif ou non. Cette fonctionnalité permet aux clients NLA d’affecter une expérience utilisateur d’informations réseau cohérente sur plusieurs applications.

## <a name="parameters"></a>Paramètres

Pour inscrire une instance de service auprès du fournisseur de service de reconnaissance d’emplacement réseau, utilisez la fonction [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) . Pour pouvoir inscrire correctement une instance de service, certains paramètres de la fonction **WSASetService** doivent être définis avec les informations appropriées, comme expliqué dans cette section. Pour référence rapide, la fonction **WSASetService** a la syntaxe suivante :

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Pour le paramètre *lpqsRegInfo* , fournissez une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) à partir d’un résultat de requête NLA SP ou construite conformément aux exigences d’une requête NLA SP, comme indiqué dans [interrogation NLA](querying-nla-2.md).

Les opérations prises en charge pour le paramètre *essOperation* sont les suivantes :

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>\_Registre RNRSERVICE
</dt> <dd>

Le réseau défini dans la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie dans *lpqsRegInfo* est rendu persistant pour l’utilisateur actif en stockant l’instance réseau dans la ruche du registre de l’utilisateur actuel, ce qui autorise l’emprunt d’identité.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ Supprimer
</dt> <dd>

Si le réseau défini dans la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie dans *lpqsRegInfo* est persistant, il sera supprimé.

</dd> </dl>

L’opération spécifiée dans le paramètre *essOperation* peut être modifiée par les options suivantes, qui peuvent être spécifiées avec binaire ou logique :

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nom convivial de l' \_ extension NLA
</dt> <dd>

Lorsqu’il est utilisé avec RNRSERVICE \_ Register, le champ *lpszComment* du réseau défini dans *lpqsRegInfo* est vérifié pour la validité et stocké de façon permanente. Lorsqu’il est utilisé avec RNRSERVICE \_ Delete et que le réseau défini a un nom convivial, le nom convivial est supprimé, mais l’entrée réseau reste intacte.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_réseau NLA ALLUSERS \_
</dt> <dd>

Lorsqu’elle est utilisée avec RNRSERVICE \_ Register, l’entrée est stockée de façon permanente sous HKEY \_ local \_ machine, ce qui la rend disponible pendant les requêtes à tous les utilisateurs sur l’ordinateur local. Lorsqu’il est utilisé avec RNRSERVICE \_ Delete, le réseau spécifié est supprimé de HKEY \_ local \_ machine. Une erreur est retournée si le réseau spécifié n’est pas présent. Pour supprimer un réseau de la ruche du registre de l’utilisateur actuel, cet indicateur ne doit pas être spécifié. Cet indicateur n’est valide que dans le contexte de sécurité d’un administrateur système local.

</dd> </dl>

NLA prend en charge les codes d’erreur suivants pour les appels de fonction [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :

| Error             | Signification                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Un appel réussi à la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) pour initialiser NLA n’a pas été effectué.                                                                  |
| WSAEACCESS        | \_ \_ Le réseau NLA AllUsers a été spécifié dans *dwControlFlags* alors qu’il n’est pas dans le contexte de sécurité d’un administrateur système local.                                                |
| WSAEALREADY       | Le réseau spécifié est déjà stocké de façon persistante de la manière demandée, et aucun indicateur n’a été spécifié dans *dwControlFlags* pour indiquer une mise à jour de l’entrée existante. |
| WSAEAFNOSUPPORT   | Une famille de protocoles a été spécifiée pour laquelle il n’existe pas de prise en charge. Seules les familles de protocole IP sont prises en charge dans NLA.                                                             |
| WSAEPFNOSUPPORT   | Un protocole a été spécifié pour lequel il n’existe pas de prise en charge. Seul le protocole IP est pris en charge dans NLA.                                                                              |



 

 

 



