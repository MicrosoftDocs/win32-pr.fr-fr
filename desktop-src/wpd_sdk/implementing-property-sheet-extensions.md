---
description: Implémentation des extensions de feuille de propriétés
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: Implémentation des extensions de feuille de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a351678c2377aacdd73ec750841a32a81ad973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529465"
---
# <a name="implementing-property-sheet-extensions"></a><span data-ttu-id="32de0-103">Implémentation des extensions de feuille de propriétés</span><span class="sxs-lookup"><span data-stu-id="32de0-103">Implementing Property Sheet Extensions</span></span>

<span data-ttu-id="32de0-104">L’extension d’espace de noms WPD prend en charge les feuilles de propriétés extensibles.</span><span class="sxs-lookup"><span data-stu-id="32de0-104">The WPD Namespace Extension supports extensible property sheets.</span></span> <span data-ttu-id="32de0-105">Il s’agit des boîtes de dialogue de propriétés qui s’affichent lorsqu’un utilisateur clique avec le bouton droit sur un objet, tel qu’un fichier ou un dossier, et sélectionne des **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="32de0-105">These are the property dialogs that appear when a user right-clicks on an object, such as a file or a folder, and selects **Properties**.</span></span> <span data-ttu-id="32de0-106">Certaines applications WPD tirent parti de ces feuilles de propriétés extensibles pour afficher des propriétés pour le contenu côté appareil (ou les objets qui résident sur l’appareil).</span><span class="sxs-lookup"><span data-stu-id="32de0-106">Some WPD applications will take advantage of these extensible property sheets to display properties for device-side content (or objects that reside on the device).</span></span>

<span data-ttu-id="32de0-107">Les feuilles de propriétés extensibles sont prises en charge par les interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="32de0-107">Extensible property sheets are supported by the interfaces described in the following table.</span></span> <span data-ttu-id="32de0-108">Pour plus d’informations sur l’une de ces interfaces, consultez le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="32de0-108">For more information about any of these interfaces, see the Windows SDK.</span></span>



| <span data-ttu-id="32de0-109">Interface</span><span class="sxs-lookup"><span data-stu-id="32de0-109">Interface</span></span>           | <span data-ttu-id="32de0-110">Description</span><span class="sxs-lookup"><span data-stu-id="32de0-110">Description</span></span>                                                                  |
|---------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="32de0-111">IDataObject</span><span class="sxs-lookup"><span data-stu-id="32de0-111">IDataObject</span></span>         | <span data-ttu-id="32de0-112">Utilisé pour passer le tableau PIDL du menu contextuel au gestionnaire de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="32de0-112">Used to pass the context menu's PIDL array to the context menu handler.</span></span>      |
| <span data-ttu-id="32de0-113">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="32de0-113">IPropertySetStorage</span></span> | <span data-ttu-id="32de0-114">Cette interface est utilisée pour récupérer les propriétés WPD pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="32de0-114">This interface is used to retrieve WPD properties for the given object.</span></span>      |
| <span data-ttu-id="32de0-115">IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="32de0-115">IPropertyStorage</span></span>    | <span data-ttu-id="32de0-116">Cette interface est également utilisée pour récupérer les propriétés WPD pour l’objet donné.</span><span class="sxs-lookup"><span data-stu-id="32de0-116">This interface is also used to retrieve WPD properties for the given object.</span></span> |
| <span data-ttu-id="32de0-117">IShellExtInit</span><span class="sxs-lookup"><span data-stu-id="32de0-117">IShellExtInit</span></span>       | <span data-ttu-id="32de0-118">Initialise les extensions de l’interpréteur de commandes Windows Vista pour le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="32de0-118">Initializes the Windows Vista Shell extensions for the context menu.</span></span>         |
| <span data-ttu-id="32de0-119">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="32de0-119">IShellPropSheetExt</span></span>  | <span data-ttu-id="32de0-120">Prend en charge l’ajout d’extensions de feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="32de0-120">Supports addition of property sheet extensions.</span></span>                              |



 

<span data-ttu-id="32de0-121">Les feuilles de propriétés pour les API WPD sont implémentées comme toute autre feuille de propriétés dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32de0-121">Property sheets for WPD are implemented like any other property sheet in Windows Vista.</span></span> <span data-ttu-id="32de0-122">Si vous avez déjà implémenté un gestionnaire de feuilles de propriétés, vous pouvez modifier votre code existant afin qu’il prenne en charge le contenu côté appareil.</span><span class="sxs-lookup"><span data-stu-id="32de0-122">If you've already implemented a property sheet handler, you can modify your existing code so that it supports device-side content.</span></span> <span data-ttu-id="32de0-123">Si vous n’avez jamais créé de gestionnaire de menu contextuel, consultez la rubrique Création de gestionnaires de feuille de propriétés dans la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="32de0-123">If you've never created a context menu handler, see the Creating Property Sheet Handlers topic in the Windows SDK.</span></span>

<span data-ttu-id="32de0-124">Les deux points à partir desquels un gestionnaire de feuille de propriétés WPD diffère de tout autre gestionnaire se trouvent dans l’inscription du gestionnaire et la prise en charge du contenu côté appareil.</span><span class="sxs-lookup"><span data-stu-id="32de0-124">The two points at which a WPD property sheet handler differs from any other handler is in the handler registration and the support of device-side content.</span></span>

 

 



