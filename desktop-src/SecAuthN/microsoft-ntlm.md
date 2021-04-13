---
description: Le protocole de stimulation/réponse de Windows (NTLM) est le protocole d’authentification utilisé sur les réseaux qui incluent des systèmes exécutant le système d’exploitation Windows et sur des systèmes autonomes.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525863"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Le protocole de stimulation/réponse de Windows (NTLM) est le protocole d’authentification utilisé sur les réseaux qui incluent des systèmes exécutant le système d’exploitation Windows et sur des systèmes autonomes.

Le [*package de sécurité*](../secgloss/s-gly.md) Microsoft [*Kerberos*](../secgloss/k-gly.md) ajoute une sécurité supérieure à celle de NTLM pour les systèmes d’un réseau. Bien que Microsoft *Kerberos* soit le protocole de choix, NTLM est toujours pris en charge. NTLM doit également être utilisé pour l’authentification d’ouverture de session sur des systèmes autonomes. Pour plus d’informations sur Kerberos, consultez [Microsoft Kerberos](microsoft-kerberos.md).

Les informations d’identification NTLM sont basées sur les données obtenues pendant le processus d’ouverture de session interactive et se composent d’un nom de domaine, d’un nom d’utilisateur et d’un [*hachage*](../secgloss/h-gly.md) unidirectionnel du mot de passe de l’utilisateur. NTLM utilise un protocole de stimulation/réponse chiffré pour authentifier un utilisateur sans envoyer le mot de passe de l’utilisateur sur le réseau. Au lieu de cela, le système demandant l’authentification doit effectuer un calcul qui prouve qu’il a accès aux informations d’identification NTLM sécurisées.

L’authentification NTLM interactive sur un réseau implique généralement deux systèmes : un système client, où l’utilisateur demande l’authentification et un contrôleur de domaine, où les informations relatives au mot de passe de l’utilisateur sont conservées. Une authentification non interactive, qui peut être nécessaire pour autoriser un utilisateur déjà connecté à accéder à une ressource telle qu’une application serveur, implique généralement trois systèmes : un client, un serveur et un contrôleur de domaine qui effectue les calculs d’authentification pour le compte du serveur.

Les étapes suivantes présentent un aperçu de l’authentification non interactive NTLM. La première étape fournit les informations d’identification NTLM de l’utilisateur et se produit uniquement dans le cadre du processus d’authentification interactive (ouverture de session).

1.  (Authentification interactive uniquement) Un utilisateur accède à un ordinateur client et fournit un nom de domaine, un nom d’utilisateur et un mot de passe. Le client calcule un [*hachage*](../secgloss/h-gly.md) de chiffrement du mot de passe et ignore le mot de passe réel.
2.  Le client envoie le nom d’utilisateur au serveur (en [*texte en clair*](../secgloss/p-gly.md)).
3.  Le serveur génère un nombre aléatoire de 16 octets, appelé *défi* ou [*nonce*](../secgloss/n-gly.md), et l’envoie au client.
4.  Le client chiffre cette stimulation avec le hachage du mot de passe de l’utilisateur et renvoie le résultat au serveur. C’est ce que l’on appelle la *réponse*.
5.  Le serveur envoie les trois éléments suivants au contrôleur de domaine :

    -   Nom d’utilisateur
    -   Stimulation envoyée au client
    -   Réponse reçue du client

6.  Le contrôleur de domaine utilise le nom d’utilisateur pour récupérer le hachage du mot de passe de l’utilisateur dans la base de données du gestionnaire de comptes de sécurité. Elle utilise ce hachage de mot de passe pour chiffrer la demande.
7.  Le contrôleur de domaine compare le Challenge chiffré qu’il a calculé (à l’étape 6) à la réponse calculée par le client (à l’étape 4). S’ils sont identiques, l’authentification réussit.

Votre application ne doit pas accéder directement au [*package de sécurité*](../secgloss/s-gly.md) NTLM. au lieu de cela, il doit utiliser le package de sécurité [*Negotiate*](../secgloss/n-gly.md) . Negotiate permet à votre application de tirer parti de [*protocoles de sécurité*](../secgloss/s-gly.md) plus avancés s’ils sont pris en charge par les systèmes impliqués dans l’authentification. Actuellement, le package de sécurité Negotiate choisit entre [*Kerberos*](../secgloss/k-gly.md) et NTLM. Negotiate sélectionne Kerberos, sauf s’il ne peut pas être utilisé par l’un des systèmes impliqués dans l’authentification.

 

 
