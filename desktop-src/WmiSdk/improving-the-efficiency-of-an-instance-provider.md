---
description: Un fournisseur WMI à hautes performances augmente considérablement la vitesse à laquelle un client WMI peut obtenir des informations à partir d’un fournisseur d’instances WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Amélioration de l’efficacité d’un fournisseur d’instances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866885"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a><span data-ttu-id="17650-103">Amélioration de l’efficacité d’un fournisseur d’instances</span><span class="sxs-lookup"><span data-stu-id="17650-103">Improving the Efficiency of an Instance Provider</span></span>

<span data-ttu-id="17650-104">Un fournisseur WMI à hautes performances augmente considérablement la vitesse à laquelle un client WMI peut obtenir des informations à partir d’un fournisseur d’instances WMI.</span><span class="sxs-lookup"><span data-stu-id="17650-104">A WMI high-performance provider greatly increases the speed at which a WMI client can obtain information from a WMI instance provider.</span></span> <span data-ttu-id="17650-105">La principale modification est qu’un fournisseur à hautes performances s’exécute en tant que serveur in-process pour l’application cliente ou WMI.</span><span class="sxs-lookup"><span data-stu-id="17650-105">The main change is that a high-performance provider runs as an in-process server to either the client application or to WMI.</span></span> <span data-ttu-id="17650-106">En plaçant le fournisseur dans le processus client, vous pouvez accélérer l’interaction entre les deux.</span><span class="sxs-lookup"><span data-stu-id="17650-106">By placing the provider inside the client process, you can speed up the interaction between the two.</span></span>

<span data-ttu-id="17650-107">Pour plus d’informations sur la façon de faire de votre fournisseur d’instances un fournisseur à hautes performances, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17650-107">For more information about how to make your instance provider a high-performance provider, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

 

 



