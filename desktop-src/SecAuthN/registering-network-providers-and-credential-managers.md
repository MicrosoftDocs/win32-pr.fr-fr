---
description: Une fois que vous avez créé votre fournisseur réseau ou le gestionnaire d’informations d’identification, vous devez l’inscrire auprès du système.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203175"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="239c0-103">Inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="239c0-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="239c0-104">Une fois que vous avez créé votre fournisseur réseau ou le gestionnaire d’informations d’identification, vous devez l’inscrire auprès du système.</span><span class="sxs-lookup"><span data-stu-id="239c0-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="239c0-105">Cela est nécessaire pour que le MPR sache quels fournisseurs de réseau sont installés.</span><span class="sxs-lookup"><span data-stu-id="239c0-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="239c0-106">Au démarrage de MPR, il vérifie le registre et charge tous les fournisseurs de réseau ou gestionnaires d’informations d’identification qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="239c0-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="239c0-107">Étant donné que les fournisseurs de réseau et les gestionnaires d’informations d’identification sont liés, ils sont inscrits dans les mêmes sous-clés du Registre.</span><span class="sxs-lookup"><span data-stu-id="239c0-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="239c0-108">En fait, les dll de fournisseur réseau peuvent également être des gestionnaires d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="239c0-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="239c0-109">Pour obtenir des informations détaillées sur les clés de registre que vous devez créer pour votre fournisseur réseau ou le gestionnaire d’informations d’identification, consultez [clés de registre d’authentification](authentication-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="239c0-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



