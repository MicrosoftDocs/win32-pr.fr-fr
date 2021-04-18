---
description: L’acquisition d’images Windows (WIA) fournit des objets d’automatisation pour une utilisation dans les langages de script, tels que les logiciels de développement Microsoft JScript et Microsoft Visual Basic Scripting Edition (VBScript), ainsi que des langages de programmation de haut niveau tels que le système de développement Microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modèle de script WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519310"
---
# <a name="wia-scripting-model"></a><span data-ttu-id="88048-103">Modèle de script WIA</span><span class="sxs-lookup"><span data-stu-id="88048-103">WIA Scripting Model</span></span>

<span data-ttu-id="88048-104">L’acquisition d’images Windows (WIA) fournit des objets d’automatisation pour une utilisation dans les langages de script, tels que les logiciels de développement Microsoft JScript et Microsoft Visual Basic Scripting Edition (VBScript), ainsi que des langages de programmation de haut niveau tels que le système de développement Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="88048-104">Windows Image Acquisition (WIA) provides automation objects for use in scripting languages, such as Microsoft JScript and Microsoft Visual Basic Scripting Edition (VBScript) development software, and high-level programming languages such as Microsoft Visual Basic development system.</span></span>

> [!Note]  
> <span data-ttu-id="88048-105">Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="88048-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="88048-106">Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="88048-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="88048-107">Le tableau suivant décrit les objets de script WIA et leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="88048-107">The following table describes WIA scripting objects and how they are used.</span></span> 

| <span data-ttu-id="88048-108">Object</span><span class="sxs-lookup"><span data-stu-id="88048-108">Object</span></span>                                | <span data-ttu-id="88048-109">Description</span><span class="sxs-lookup"><span data-stu-id="88048-109">Description</span></span>                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88048-110">**WIA**</span><span class="sxs-lookup"><span data-stu-id="88048-110">**Wia**</span></span>](-wia-wia.md)               | <span data-ttu-id="88048-111">Objet de script WIA de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="88048-111">The top-level WIA scripting object.</span></span> <span data-ttu-id="88048-112">Utilisez l’objet [**WIA**](-wia-wia.md) pour énumérer et vous connecter à des appareils, et pour gérer des événements de périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="88048-112">Use the [**Wia**](-wia-wia.md) object to enumerate and connect to devices, and to handle hardware device events.</span></span>                                        |
| [<span data-ttu-id="88048-113">**DeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="88048-113">**DeviceInfo**</span></span>](-wia-deviceinfo.md) | <span data-ttu-id="88048-114">L’objet [**DeviceInfo**](-wia-deviceinfo.md) fournit l’accès aux informations sur les propriétés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88048-114">The [**DeviceInfo**](-wia-deviceinfo.md) object provides access to information about device properties.</span></span>                                                                                     |
| [<span data-ttu-id="88048-115">**Élément**</span><span class="sxs-lookup"><span data-stu-id="88048-115">**Item**</span></span>](-wia-item.md)             | <span data-ttu-id="88048-116">Cet objet représente les éléments de périphérique, de fichier et de dossier WIA.</span><span class="sxs-lookup"><span data-stu-id="88048-116">This object represents WIA device, file, and folder items.</span></span> <span data-ttu-id="88048-117">Un périphérique matériel WIA et ses images ou lits d’analyse sont représentés sous la forme d’une arborescence hiérarchique d’objets [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="88048-117">A WIA hardware device and its images or scanning beds is represented as a hierarchical tree of [**Item**](-wia-item.md) objects.</span></span> |



 

<span data-ttu-id="88048-118">L’objet [**DeviceInfo**](-wia-deviceinfo.md) et l’objet [**Item**](-wia-item.md) sont associés à des objets de collection.</span><span class="sxs-lookup"><span data-stu-id="88048-118">Both the [**DeviceInfo**](-wia-deviceinfo.md) object and the [**Item**](-wia-item.md) object are associated with collection objects.</span></span> <span data-ttu-id="88048-119">Pour plus d’informations sur l’utilisation des objets de collection, consultez Utilisation des objets de collection WIA.</span><span class="sxs-lookup"><span data-stu-id="88048-119">For information about using collection objects, see Using WIA Collection Objects.</span></span>

<span data-ttu-id="88048-120">Les rubriques suivantes couvrent des informations générales sur l’utilisation du modèle de script WIA :</span><span class="sxs-lookup"><span data-stu-id="88048-120">The following topics cover general information about using the WIA scripting model:</span></span>

-   [<span data-ttu-id="88048-121">Conventions de syntaxe</span><span class="sxs-lookup"><span data-stu-id="88048-121">Syntax Conventions</span></span>](-wia-syntax-conventions.md)
-   [<span data-ttu-id="88048-122">Utilisation d’objets de collection WIA</span><span class="sxs-lookup"><span data-stu-id="88048-122">Using WIA Collection Objects</span></span>](-wia-using-wia-collection-objects.md)
-   [<span data-ttu-id="88048-123">Définitions de constantes de propriété WIA</span><span class="sxs-lookup"><span data-stu-id="88048-123">WIA Property Constant Definitions</span></span>](-wia-wia-property-constant-definitions.md)

 

 
