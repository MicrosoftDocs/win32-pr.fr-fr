---
description: Format MOF (MOF) est le langage utilisé pour décrire les classes Common Information Model (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539124"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="3502f-103">Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="3502f-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="3502f-104">Format MOF (MOF) est le langage utilisé pour décrire les classes [*Common Information Model (CIM)*](gloss-c.md) .</span><span class="sxs-lookup"><span data-stu-id="3502f-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="3502f-105">La méthode recommandée pour les fournisseurs WMI pour implémenter les nouvelles classes WMI est dans les fichiers MOF qui sont compilés à l’aide de [**Mofcomp.exe**](mofcomp.md) dans le [*référentiel WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="3502f-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="3502f-106">Il est également possible de créer et de manipuler des classes et des instances CIM à l’aide [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3502f-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="3502f-107">Un fournisseur WMI se compose normalement d’un fichier MOF, qui définit les classes de données et d’événements pour lesquelles le fournisseur retourne des données, ainsi qu’un fichier DLL qui contient le code qui fournit des données.</span><span class="sxs-lookup"><span data-stu-id="3502f-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="3502f-108">Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3502f-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="3502f-109">Les applications et les scripts du client WMI peuvent rechercher des instances de classes MOF du fournisseur ou s’abonner pour recevoir des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="3502f-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="3502f-110">Vous pouvez effectuer les tâches suivantes avec MOF :</span><span class="sxs-lookup"><span data-stu-id="3502f-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="3502f-111">Compilation des fichiers MOF</span><span class="sxs-lookup"><span data-stu-id="3502f-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="3502f-112">Création d’une classe</span><span class="sxs-lookup"><span data-stu-id="3502f-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="3502f-113">Création d’une instance</span><span class="sxs-lookup"><span data-stu-id="3502f-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="3502f-114">Création d’une méthode</span><span class="sxs-lookup"><span data-stu-id="3502f-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="3502f-115">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="3502f-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="3502f-116">Création d’un commentaire</span><span class="sxs-lookup"><span data-stu-id="3502f-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="3502f-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3502f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3502f-118">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="3502f-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



