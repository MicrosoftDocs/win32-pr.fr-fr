---
description: Lorsqu’un package de sécurité SSP/AP fonctionne comme un package d’authentification, il est chargé dans l’espace de processus de l’autorité de sécurité locale (LSA) et est dit en mode LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Mode LSA et mode utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8fadde30fe60c38a2b8ccb1f158d94ec7d5603
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035016"
---
# <a name="lsa-mode-vs-user-mode"></a><span data-ttu-id="32304-103">Mode LSA et mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="32304-103">LSA Mode vs. User Mode</span></span>

<span data-ttu-id="32304-104">Lorsqu’un [*package de sécurité*](../secgloss/s-gly.md) SSP/AP fonctionne comme un [*package d’authentification*](../secgloss/a-gly.md), il est chargé dans l’espace de processus de l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) et est dit en mode LSA.</span><span class="sxs-lookup"><span data-stu-id="32304-104">When an SSP/AP [*security package*](../secgloss/s-gly.md) is functioning as an [*authentication package*](../secgloss/a-gly.md), it is loaded into the process space of the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) and is said to be in LSA mode.</span></span> <span data-ttu-id="32304-105">Les applications de connexion accèdent à la fonctionnalité de package d’authentification à l’aide des [fonctions de connexion LSA](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="32304-105">Logon applications access authentication package functionality using the [LSA Logon Functions](authentication-functions.md).</span></span> <span data-ttu-id="32304-106">Les développeurs peuvent utiliser les fonctions de prise en charge LSA disponibles uniquement pour les packages de sécurité en mode LSA afin d’implémenter des packages d’authentification plus sophistiqués que ceux précédemment pris en charge.</span><span class="sxs-lookup"><span data-stu-id="32304-106">Developers can use LSA support functions available only to LSA-mode security packages to implement more sophisticated authentication packages than previously supported.</span></span>

<span data-ttu-id="32304-107">Lorsqu’un [*package de sécurité*](../secgloss/s-gly.md) fournit des services de sécurité à une application client/serveur, il est chargé dans les processus client et serveur et est dit en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32304-107">When a [*security package*](../secgloss/s-gly.md) provides security services to a client/server application, it is loaded into the client and server processes and is said to be in user mode.</span></span> <span data-ttu-id="32304-108">Les applications client/serveur accèdent aux services de support de sécurité du package de sécurité à l’aide de l’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32304-108">Client/server applications access the security package's security support services using Microsoft [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI).</span></span>

<span data-ttu-id="32304-109">La prise en charge LSA pour le fournisseur de services partagés/APs comprend des fonctions que les instances du mode LSA et du mode utilisateur d’un package de sécurité peuvent utiliser pour communiquer.</span><span class="sxs-lookup"><span data-stu-id="32304-109">LSA support for SSP/APs includes functions that the LSA-mode and user-mode instances of a security package can use to communicate.</span></span> <span data-ttu-id="32304-110">En outre, l’instance de mode utilisateur d’un package de sécurité peut déléguer des demandes d’informations sélectionnées à l’instance du package en mode LSA.</span><span class="sxs-lookup"><span data-stu-id="32304-110">Additionally, the user-mode instance of a security package can delegate selected requests for information to the LSA-mode instance of the package.</span></span>

<span data-ttu-id="32304-111">Pour plus d’informations sur la façon dont les packages de sécurité sont initialisés pour chaque mode, consultez [initialisation du mode LSA](lsa-mode-initialization.md) et [initialisation du mode utilisateur](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="32304-111">For details about how security packages are initialized for each mode, see [LSA-mode Initialization](lsa-mode-initialization.md) and [User-mode Initialization](user-mode-initialization.md).</span></span>

 

 
