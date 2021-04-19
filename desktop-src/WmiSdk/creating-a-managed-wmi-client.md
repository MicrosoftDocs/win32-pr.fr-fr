---
description: WMI ne prend pas actuellement en charge le code managé sur WMI, mais il est pris en charge sur MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Création d’un client WMI géré
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531873"
---
# <a name="creating-a-managed-wmi-client"></a><span data-ttu-id="be8cc-103">Création d’un client WMI géré</span><span class="sxs-lookup"><span data-stu-id="be8cc-103">Creating a Managed WMI Client</span></span>

<span data-ttu-id="be8cc-104">La version actuelle de WMI contient l’espace de noms System. Management, qui expose un certain nombre d’API qui interagissent avec WMI.</span><span class="sxs-lookup"><span data-stu-id="be8cc-104">The current release of WMI does contain the System.Management namespace, which exposes a number of API's that interact with WMI.</span></span> <span data-ttu-id="be8cc-105">Toutefois, il n’est pas recommandé d’utiliser cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="be8cc-105">However, it is not recommended that you use this namespace.</span></span>

<span data-ttu-id="be8cc-106">Si vous souhaitez créer un client WMI géré, il est recommandé d’utiliser l’infrastructure de gestion Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="be8cc-106">If you wish to create a managed WMI client, it is recommended that you use the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="be8cc-107">MI est la version de la nouvelle génération de WMI et contient la prise en charge complète du code managé.</span><span class="sxs-lookup"><span data-stu-id="be8cc-107">MI is the next-generation version of WMI, and contains full support for managed code.</span></span> <span data-ttu-id="be8cc-108">Pour plus d’informations, consultez [comment implémenter un client mi géré](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span><span class="sxs-lookup"><span data-stu-id="be8cc-108">For more information, see [How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).</span></span>

 

 
