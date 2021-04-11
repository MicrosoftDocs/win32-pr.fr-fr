---
description: Le modèle de sécurité utilisé dans le protocole SMB Microsoft est identique à celui utilisé par d’autres variantes de SMB et se compose de deux niveaux de sécurité&\# 8212 ; utilisateur et partage.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Authentification du protocole SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862470"
---
# <a name="microsoft-smb-protocol-authentication"></a><span data-ttu-id="41244-103">Authentification du protocole SMB Microsoft</span><span class="sxs-lookup"><span data-stu-id="41244-103">Microsoft SMB Protocol Authentication</span></span>

<span data-ttu-id="41244-104">Le modèle de sécurité utilisé dans le protocole SMB Microsoft est identique à celui utilisé par d’autres variantes de SMB et se compose de deux niveaux de sécurité : utilisateur et partage.</span><span class="sxs-lookup"><span data-stu-id="41244-104">The security model used in Microsoft SMB Protocol is identical to the one used by other variants of SMB, and consists of two levels of security—user and share.</span></span> <span data-ttu-id="41244-105">Un partage est un fichier, un répertoire ou une imprimante accessible par les clients du protocole SMB Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41244-105">A share is a file, directory, or printer that can be accessed by Microsoft SMB Protocol clients.</span></span>

<span data-ttu-id="41244-106">L’authentification au niveau de l’utilisateur indique que le client qui tente d’accéder à un partage sur un serveur doit fournir un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="41244-106">User-level authentication indicates that the client attempting to access a share on a server must provide a user name and password.</span></span> <span data-ttu-id="41244-107">Une fois authentifié, l’utilisateur peut accéder à tous les partages sur un serveur qui n’est pas protégé par la sécurité au niveau du partage.</span><span class="sxs-lookup"><span data-stu-id="41244-107">When authenticated, the user can then access all shares on a server not also protected by share-level security.</span></span> <span data-ttu-id="41244-108">Ce niveau de sécurité permet aux administrateurs système de déterminer spécifiquement les utilisateurs et les groupes qui peuvent accéder à un partage.</span><span class="sxs-lookup"><span data-stu-id="41244-108">This security level allows system administrators to specifically determine which users and groups can access a share.</span></span>

<span data-ttu-id="41244-109">L’authentification au niveau du partage indique que l’accès à un partage est contrôlé par un mot de passe attribué à ce partage uniquement.</span><span class="sxs-lookup"><span data-stu-id="41244-109">Share-level authentication indicates that access to a share is controlled by a password assigned to that share only.</span></span> <span data-ttu-id="41244-110">Contrairement à la sécurité au niveau de l’utilisateur, ce niveau de sécurité ne nécessite pas de nom d’utilisateur pour l’authentification et aucune identité d’utilisateur n’est établie.</span><span class="sxs-lookup"><span data-stu-id="41244-110">Unlike user-level security, this security level does not require a user name for authentication and no user identity is established.</span></span>

<span data-ttu-id="41244-111">Dans ces deux niveaux de sécurité, le mot de passe est chiffré avant d’être envoyé au serveur.</span><span class="sxs-lookup"><span data-stu-id="41244-111">Under both of these security levels, the password is encrypted before it is sent to the server.</span></span> <span data-ttu-id="41244-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) et le chiffrement plus ancien de LAN Manager (LM) sont pris en charge par le protocole SMB Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41244-112">[NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) and the older LAN Manager (LM) encryption are supported by Microsoft SMB Protocol.</span></span> <span data-ttu-id="41244-113">Les deux méthodes de chiffrement utilisent l’authentification par stimulation-réponse, où le serveur envoie une chaîne aléatoire au client et le client retourne une chaîne de réponse calculée qui prouve que le client dispose d’informations d’identification suffisantes pour l’accès.</span><span class="sxs-lookup"><span data-stu-id="41244-113">Both encryption methods use challenge-response authentication, where the server sends the client a random string and the client returns a computed response string that proves the client has sufficient credentials for access.</span></span>

 

 
