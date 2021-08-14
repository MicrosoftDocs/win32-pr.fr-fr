---
description: Une autorité de certification Microsoft (CA) peut être configurée pour archiver et récupérer la clé privée associée à la clé publique envoyée dans la demande de certificat.
ms.assetid: c6535dbf-c3fe-4f70-9a70-02805253a651
title: Serveur de récupération de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a313ac46bf540d6d0f356f7e2c4910e31bee1f2a4268931ac6a942085505b423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903772"
---
# <a name="key-recovery-server"></a>Serveur de récupération de clé

Une autorité de certification Microsoft (CA) peut être configurée pour archiver et récupérer la clé privée associée à la clé publique envoyée dans la demande de certificat. La récupération est utile si une clé est perdue. Par défaut, seules les clés de chiffrement peuvent être archivées. Il n’est pas nécessaire d’archiver les clés destinées uniquement à la signature, car seule la clé publique est nécessaire pour vérifier une signature si la clé de signature privée est perdue.

Pour archiver une clé, l’autorité de certification doit être configurée pour émettre des certificats de l’agent de récupération de clé (KRA) et avoir déjà émis au moins un. Un agent de récupération de clé est un administrateur autorisé par une organisation à déchiffrer les clés privées. Pour améliorer la sécurité, nous recommandons que les rôles agent de récupération de clé et gestionnaire de certificat soient attribués à des personnes différentes, que le gestionnaire de certificats est autorisé à récupérer sans déchiffrer les clés archivées, et que l’agent de récupération de clé soit autorisé à déchiffrer les clés, mais pas à les récupérer.

## <a name="key-archival"></a>Archivage de clé

Un client demande généralement un certificat à l’aide d’un modèle. Si le modèle requiert l’archivage de la clé privée, les étapes suivantes sont effectuées par le client et l’autorité de certification :

1.  Le client récupère et valide le certificat d’échange d’autorité de certification pour déterminer s’il a été signé à l’aide de la même clé que celle utilisée pour signer le certificat de signature de l’autorité de certification. Cela garantit que la seule autorité de certification qui peut déchiffrer la clé privée est l’autorité de certification à partir de laquelle un certificat est demandé.
2.  La clé publique dans le certificat d’échange d’autorité de certification est utilisée pour chiffrer la clé privée associée à la demande de certificat et la demande est envoyée à l’autorité de certification.
3.  L’autorité de certification utilise la clé privée associée à son certificat Exchange pour déchiffrer la clé privée envoyée par le client et vérifie que les clés publique et privée de la demande sont liées.
4.  L’autorité de certification chiffre la clé privée à l’aide de la clé publique dans le certificat KRA. Si l’autorité de certification a émis plusieurs certificats KRA, elle chiffre la clé privée une seule fois avec chaque clé publique disponible afin que tout agent de récupération de clé autorisé puisse récupérer une clé. Les clés privées chiffrées sont stockées dans la base de données de certificats.
5.  L’autorité de certification libère toutes les références à la clé privée et libère en toute sécurité et met à zéro toute la mémoire qui contenait la clé. Cela permet de s’assurer que l’autorité de certification n’a plus accès à la clé au format texte clair.

> [!Note]  
> Seule une demande CMC peut être utilisée pour l’archivage de clé. Les demandes CMC sont représentées par l’interface [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .

 

## <a name="key-recovery"></a>Récupération de clé

La récupération de clé n’est pas directement prise en charge par les services de certificats Active Directory ou l’API d’inscription de certificats. Toutefois, Microsoft fournit les applications suivantes pour vous aider dans le processus :

-   Certutil.exe est un programme de ligne de commande qui peut être utilisé pour récupérer des informations de configuration de l’autorité de certification, vérifier les certificats, les paires de clés et les chaînes de certificats, et sauvegarder et restaurer des clés. il est inclus dans les systèmes d’exploitation serveur à partir de Windows server 2003.
-   Krecover.exe est un programme basé sur une boîte de dialogue qui permet la récupération de clés. il est inclus dans le Kit de ressources à partir de Windows Server 2003.

Les étapes suivantes sont effectuées pour récupérer une clé privée :

1.  Le gestionnaire de certificats localise les candidats potentiels à la récupération de clé dans la base de données de certificats à l’aide du nom du certificat, du demandeur ou de l’utilisateur. La commande **certutil** **-GetKey** peut être utilisée à cet effet.
2.  Une fois que le gestionnaire de certificats dispose d’une liste de certificats, la commande **-GetKey** est appelée à nouveau avec un numéro de série de certificat spécifique ou un curseur de défilement pour récupérer un \# fichier PKCS 7 contenant le certificat KRA, la chaîne de certificats utilisateur et la clé privée qui a été chiffrée au cours de l’archivage à l’aide de la clé publique de l’agent de récupération.
3.  Le gestionnaire de certificats passe le contrôle du processus à l’agent de récupération de clé dont la clé privée correspond à la clé publique contenue dans le certificat KRA.
4.  L’agent de récupération de clé déchiffre la clé privée archivée renvoyée dans le \# fichier PKCS 7 à l’aide de la clé privée Kra. Pour ce faire, vous pouvez utiliser la commande **certutil** **-recoverkey** qui place la clé dans un fichier PKCS 12 protégé par mot de passe \# . Le client doit recevoir le mot de passe via un mécanisme hors bande sécurisé.
5.  Le client importe le \# fichier PKCS 12 et utilise le mot de passe pour récupérer la clé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments PKI](about-pki-components.md)
</dt> </dl>

 

 



