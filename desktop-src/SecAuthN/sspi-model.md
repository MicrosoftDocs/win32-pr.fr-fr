---
description: L’interface SSPI (Security Support Provider Interface) permet à une application d’utiliser différents modèles de sécurité disponibles sur un ordinateur ou un réseau sans modifier l’interface du système de sécurité.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modèle SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393352"
---
# <a name="sspi-model"></a><span data-ttu-id="e3a30-103">Modèle SSPI</span><span class="sxs-lookup"><span data-stu-id="e3a30-103">SSPI Model</span></span>

<span data-ttu-id="e3a30-104">L’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) permet à une application d’utiliser différents modèles de sécurité disponibles sur un ordinateur ou un réseau sans modifier l’interface du système de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e3a30-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) allows an application to use various security models available on a computer or network without changing the interface to the security system.</span></span> <span data-ttu-id="e3a30-105">SSPI n’établit pas les [*informations d’identification*](../secgloss/c-gly.md) de connexion, car il s’agit généralement d’une opération privilégiée gérée par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e3a30-105">SSPI does not establish logon [*credentials*](../secgloss/c-gly.md) because that is generally a privileged operation handled by the operating system.</span></span>

<span data-ttu-id="e3a30-106">Un [*fournisseur SSP (Security Support Provider*](../secgloss/s-gly.md) ) est contenu dans une [*bibliothèque de liens dynamiques*](../secgloss/d-gly.md) (dll) qui implémente l’interface SSPI en mettant un ou plusieurs [*packages de sécurité*](../secgloss/s-gly.md) à la disposition des applications.</span><span class="sxs-lookup"><span data-stu-id="e3a30-106">A [*security support provider*](../secgloss/s-gly.md) (SSP) is contained in a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements SSPI by making one or more [*security packages*](../secgloss/s-gly.md) available to applications.</span></span> <span data-ttu-id="e3a30-107">Chaque package de sécurité fournit des mappages entre les appels de fonction SSPI d’une application et les fonctions d’un modèle de sécurité réel.</span><span class="sxs-lookup"><span data-stu-id="e3a30-107">Each security package provides mappings between the SSPI function calls of an application and the functions of an actual security model.</span></span> <span data-ttu-id="e3a30-108">Les packages de sécurité prennent en charge des [*protocoles de sécurité*](../secgloss/s-gly.md) tels que l’authentification [*Kerberos*](../secgloss/k-gly.md) et le gestionnaire LAN.</span><span class="sxs-lookup"><span data-stu-id="e3a30-108">Security packages support [*security protocols*](../secgloss/s-gly.md) such as [*Kerberos*](../secgloss/k-gly.md) authentication and LAN Manager.</span></span>

<span data-ttu-id="e3a30-109">L’interface SSPI est disponible en mode noyau et en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3a30-109">The SSPI interface is available in kernel mode as well as user mode.</span></span> <span data-ttu-id="e3a30-110">Pour utiliser la fonctionnalité SSPI en mode noyau, vous devez installer le DDK du système de fichiers installable Windows.</span><span class="sxs-lookup"><span data-stu-id="e3a30-110">To use SSPI functionality in kernel mode, you must install the Windows Installable File System DDK.</span></span> <span data-ttu-id="e3a30-111">Le modèle appelant reste le même, mais les considérations en mode noyau sont indiquées sur les pages de référence de fonction.</span><span class="sxs-lookup"><span data-stu-id="e3a30-111">The calling model remains the same, but kernel mode considerations are noted on function reference pages.</span></span> <span data-ttu-id="e3a30-112">Pour plus d’informations, consultez [fonctions SSPI](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e3a30-112">For more information, see [SSPI Functions](authentication-functions.md).</span></span>

 

 
