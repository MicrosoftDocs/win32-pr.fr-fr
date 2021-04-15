---
description: 'L’extension de composant logiciel enfichable pièce jointe n’a aucun moyen d’interroger directement la base de données de sécurité afin de récupérer des informations. Au lieu de cela, il doit interroger ces informations à partir des composants logiciels enfichables de configuration de sécurité à l’aide de ISceSvcAttachmentData :: GetData.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Obtention de données à partir des composants logiciels enfichables de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529638"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a><span data-ttu-id="508a4-104">Obtention de données à partir des composants logiciels enfichables de configuration</span><span class="sxs-lookup"><span data-stu-id="508a4-104">Getting Data from the Configuration Snap-ins</span></span>

<span data-ttu-id="508a4-105">L’extension de composant logiciel enfichable pièce jointe n’a aucun moyen d’interroger directement la base de données de sécurité afin de récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="508a4-105">The attachment snap-in extension has no way to directly query the security database to retrieve information.</span></span> <span data-ttu-id="508a4-106">Au lieu de cela, il doit interroger ces informations à partir des composants logiciels enfichables de configuration de sécurité à l’aide de [**ISceSvcAttachmentData :: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="508a4-106">Instead, it must query this information from the Security Configuration snap-ins using [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

<span data-ttu-id="508a4-107">Le composant logiciel enfichable d’une pièce jointe peut récupérer toutes les données lorsqu’il s’initialise lui-même, ou il peut récupérer des informations lorsque son nœud est ouvert.</span><span class="sxs-lookup"><span data-stu-id="508a4-107">The attachment snap-in can retrieve all of the data when it initializes itself, or it can retrieve information when its node is opened.</span></span>

> [!Note]  
> <span data-ttu-id="508a4-108">Vous devez utiliser la méthode [**ISceSvcAttachmentData :: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) pour libérer la mémoire tampon allouée par la méthode de composant logiciel enfichable Configuration de la sécurité [**ISceSvcAttachmentData :: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="508a4-108">You must use the [**ISceSvcAttachmentData::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) method to free the buffer allocated by the Security Configuration snap-in method [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

 

 

 



