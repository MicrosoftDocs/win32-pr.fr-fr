---
description: De nombreuses formes d’authentification sont basées sur l’idée qu’une entité peut prouver son identité si elle peut prouver qu’elle connaît une clé, telle qu’un mot de passe, que seul elle peut connaître.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Authentification par clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203178"
---
# <a name="key-authentication"></a><span data-ttu-id="e63ae-103">Authentification par clé</span><span class="sxs-lookup"><span data-stu-id="e63ae-103">Key Authentication</span></span>

<span data-ttu-id="e63ae-104">De nombreuses formes d’authentification sont basées sur l’idée qu’une entité peut prouver son identité si elle peut prouver qu’elle connaît une clé, telle qu’un mot de passe, que seul elle peut connaître.</span><span class="sxs-lookup"><span data-stu-id="e63ae-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="e63ae-105">Les techniques d’authentification qui reposent sur un secret, tel qu’un mot de passe, doivent avoir un moyen de faire en sorte que le secret ne devienne pas une connaissance publique.</span><span class="sxs-lookup"><span data-stu-id="e63ae-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="e63ae-106">Le propriétaire d’un mot de passe ne peut pas aller à une porte et fournir le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e63ae-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="e63ae-107">Une personne autre que le doorkeeper peut être à l’écoute ; ou il s’agit peut-être d’une mauvaise porte.</span><span class="sxs-lookup"><span data-stu-id="e63ae-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="e63ae-108">Afin de garder un secret, il doit exister un moyen de prouver qu’un utilisateur connaît le mot de passe sans révéler le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e63ae-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="e63ae-109">C’est l’idée qui sous-tend l’authentification par clé secrète, une méthode de vérification utilisée dans le [*protocole Kerberos*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e63ae-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="e63ae-110">Notez que le « secret » dans l’authentification par clé secrète est que le processus d’authentification a lieu « en secret », autrement dit, sans jamais révéler réellement le contenu de la clé.</span><span class="sxs-lookup"><span data-stu-id="e63ae-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="e63ae-111">Pour que l’authentification par clé secrète fonctionne, les deux parties à une transaction doivent partager une [*clé de session*](../secgloss/s-gly.md) de chiffrement qui est également secrète, connue uniquement de celles-ci et pour aucune autre.</span><span class="sxs-lookup"><span data-stu-id="e63ae-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="e63ae-112">La clé est [*symétrique*](../secgloss/s-gly.md); autrement dit, il s’agit d’une clé unique utilisée pour le chiffrement et le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="e63ae-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="e63ae-113">L’une des parties du processus d’authentification prouve sa connaissance de la clé en chiffrant un message.</span><span class="sxs-lookup"><span data-stu-id="e63ae-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="e63ae-114">L’autre partie prouve sa connaissance de la clé en déchiffrant le message.</span><span class="sxs-lookup"><span data-stu-id="e63ae-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
