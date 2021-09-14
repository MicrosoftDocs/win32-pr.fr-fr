---
description: Le modèle de sécurité utilisé dans le protocole SMB Microsoft est identique à celui utilisé par d’autres variantes de SMB et se compose de deux niveaux de sécurité&\# 8212 ; utilisateur et partage.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Authentification du protocole SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009912"
---
# <a name="microsoft-smb-protocol-authentication"></a>Authentification du protocole SMB Microsoft

Le modèle de sécurité utilisé dans le protocole SMB Microsoft est identique à celui utilisé par d’autres variantes de SMB et se compose de deux niveaux de sécurité : utilisateur et partage. Un partage est un fichier, un répertoire ou une imprimante accessible par les clients du protocole SMB Microsoft.

L’authentification au niveau de l’utilisateur indique que le client qui tente d’accéder à un partage sur un serveur doit fournir un nom d’utilisateur et un mot de passe. Une fois authentifié, l’utilisateur peut accéder à tous les partages sur un serveur qui n’est pas protégé par la sécurité au niveau du partage. Ce niveau de sécurité permet aux administrateurs système de déterminer spécifiquement les utilisateurs et les groupes qui peuvent accéder à un partage.

L’authentification au niveau du partage indique que l’accès à un partage est contrôlé par un mot de passe attribué à ce partage uniquement. Contrairement à la sécurité au niveau de l’utilisateur, ce niveau de sécurité ne nécessite pas de nom d’utilisateur pour l’authentification et aucune identité d’utilisateur n’est établie.

Dans ces deux niveaux de sécurité, le mot de passe est chiffré avant d’être envoyé au serveur. [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) et le chiffrement plus ancien de LAN Manager (LM) sont pris en charge par le protocole SMB Microsoft. Les deux méthodes de chiffrement utilisent l’authentification par stimulation-réponse, où le serveur envoie une chaîne aléatoire au client et le client retourne une chaîne de réponse calculée qui prouve que le client dispose d’informations d’identification suffisantes pour l’accès.

 

 
