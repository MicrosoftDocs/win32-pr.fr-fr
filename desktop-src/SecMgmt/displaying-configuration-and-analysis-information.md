---
description: Votre extension de composant logiciel enfichable doit afficher les informations de configuration et d’analyse actuelles pour les utilisateurs.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Affichage des informations de configuration et d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527674"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="58775-103">Affichage des informations de configuration et d’analyse</span><span class="sxs-lookup"><span data-stu-id="58775-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="58775-104">Votre extension de composant logiciel enfichable doit afficher les informations de configuration et d’analyse actuelles pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="58775-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="58775-105">Pour afficher les informations, le nœud extension du composant logiciel enfichable d’attachement doit étendre les composants logiciels enfichables de configuration de sécurité à l’aide du nœud services.</span><span class="sxs-lookup"><span data-stu-id="58775-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="58775-106">Le nœud services est le composant logiciel enfichable MMC qui administre les services installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="58775-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="58775-107">Les types de nœuds pouvant être étendus sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="58775-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="58775-108">Services de configuration NodeType = {24a7f717-1f0c-11D1-AFFB-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="58775-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="58775-109">Services d’inspection NodeType = {678050c7-1ff8-11D1-AFFB-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="58775-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="58775-110">Lorsque le nœud services est développé, la console MMC avertit toutes les extensions de composant logiciel enfichable inscrites.</span><span class="sxs-lookup"><span data-stu-id="58775-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="58775-111">Chaque composant logiciel enfichable d’une pièce jointe doit s’insérer dans le nœud services et effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="58775-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="58775-112">Appelez **QueryInterface** pour obtenir un pointeur vers l’interface [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) exposée par les composants logiciels enfichables de configuration de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="58775-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="58775-113">Appelez [**ISceSvcAttachmentData :: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) pour informer les composants logiciels enfichables de configuration de sécurité que l’extension du composant logiciel enfichable est chargée et pour établir un contexte de communication.</span><span class="sxs-lookup"><span data-stu-id="58775-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="58775-114">Appelez [**ISceSvcAttachmentData :: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) pour récupérer les informations de configuration de la base de données.</span><span class="sxs-lookup"><span data-stu-id="58775-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="58775-115">Cette étape peut être effectuée lorsque l’extension du composant logiciel enfichable s’initialise lui-même ou lorsque l’utilisateur ouvre son nœud.</span><span class="sxs-lookup"><span data-stu-id="58775-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="58775-116">Pour plus d’informations, consultez [Ajout d’un nœud extension de composant logiciel enfichable d’une pièce jointe](adding-an-attachment-snap-in-extension-node.md).</span><span class="sxs-lookup"><span data-stu-id="58775-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



