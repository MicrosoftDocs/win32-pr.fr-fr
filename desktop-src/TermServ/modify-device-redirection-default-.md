---
title: Modifier la valeur par défaut de la redirection de périphérique
description: Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840177"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="19cf9-103">Modifier la valeur par défaut de la redirection de périphérique</span><span class="sxs-lookup"><span data-stu-id="19cf9-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="19cf9-104">Étant donné que les serveurs de passerelle Bureau à distance tentent d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance, vous devrez peut-être désactiver ce paramètre par défaut dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="19cf9-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="19cf9-105">Sur Windows Server 2008 R2 et versions ultérieures, les serveurs de passerelle Bureau à distance tentent par défaut d’appliquer des stratégies de redirection de périphérique sécurisées avant de transmettre la connexion cliente à un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="19cf9-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="19cf9-106">Toutefois, cette fonctionnalité n’est pas prise en charge par certains serveurs.</span><span class="sxs-lookup"><span data-stu-id="19cf9-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="19cf9-107">Par exemple, cela n’est pas pris en charge pour les connexions aux sessions de la console Hyper-V et il peut être nécessaire de désactiver la valeur par défaut pour prendre en charge l’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="19cf9-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="19cf9-108">Dans ce cas, cette fonctionnalité peut être désactivée en créant la clé de Registre suivante pour autoriser les connexions à traverser.</span><span class="sxs-lookup"><span data-stu-id="19cf9-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="19cf9-109">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Terminal Server Gateway \\ preRDPDisableRegKey**</span><span class="sxs-lookup"><span data-stu-id="19cf9-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="19cf9-110">Lorsque cette clé existe, la passerelle Bureau à distance n’applique pas la redirection de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="19cf9-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 




