---
description: Si cette stratégie système par ordinateur est définie sur &\# 0034 ; 1&\# 0034 ;, le programme d’installation ne invite pas les utilisateurs lorsque les scripts d’une page Web utilisent l’interface d’automatisation du programme d’installation.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524957"
---
# <a name="safeforscripting"></a><span data-ttu-id="821c8-103">SafeForScripting</span><span class="sxs-lookup"><span data-stu-id="821c8-103">SafeForScripting</span></span>

<span data-ttu-id="821c8-104">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur « 1 », le programme d’installation ne invite pas les utilisateurs lorsque les scripts d’une page Web utilisent l' [interface d’automatisation](automation-interface.md)du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="821c8-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="821c8-105">Avant de définir cette stratégie, vous devez déterminer si l’invite de l’utilisateur doit être précitée pour fournir un niveau de sécurité approprié à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="821c8-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="821c8-106">Si cette stratégie n’est pas définie, lorsqu’un script hébergé par un navigateur Internet tente d’installer une application, le système avertit l’utilisateur et lui demande d’accepter ou de refuser l’installation.</span><span class="sxs-lookup"><span data-stu-id="821c8-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="821c8-107">La définition de SafeForScripting supprime cet avertissement et peut permettre l’installation d’applications sur le système sans la connaissance de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="821c8-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="821c8-108">Cette stratégie peut être utile pour une entreprise qui utilise des outils basés sur le Web pour distribuer des programmes.</span><span class="sxs-lookup"><span data-stu-id="821c8-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="821c8-109">Pour plus d’informations, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md) et [téléchargement d’une installation à partir d’Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="821c8-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="821c8-110">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="821c8-110">Registry Key</span></span>

<span data-ttu-id="821c8-111">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="821c8-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="821c8-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="821c8-112">Data Type</span></span>

<span data-ttu-id="821c8-113">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="821c8-113">**REG\_DWORD**</span></span>

 

 



