---
title: Fichiers de code pour l’exemple de fournisseur source
description: Fichiers de code pour l’exemple de fournisseur source
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- Windows Media Gestionnaire de périphériques, exemple de fournisseur de services
- Gestionnaire de périphériques, exemple de fournisseur de services
- fournisseurs de services, exemples
- exemples, fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100725"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="a0afc-109">Fichiers de code pour l’exemple de fournisseur source</span><span class="sxs-lookup"><span data-stu-id="a0afc-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="a0afc-110">L’exemple de projet de fournisseur source comprend les fichiers de code source suivants, avec des en-têtes associés :</span><span class="sxs-lookup"><span data-stu-id="a0afc-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="a0afc-111">Fichier</span><span class="sxs-lookup"><span data-stu-id="a0afc-111">File</span></span>                   | <span data-ttu-id="a0afc-112">Description</span><span class="sxs-lookup"><span data-stu-id="a0afc-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0afc-113">hdsppch. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-113">hdsppch.cpp</span></span>            | <span data-ttu-id="a0afc-114">Comprend des fichiers ATL standard.</span><span class="sxs-lookup"><span data-stu-id="a0afc-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="a0afc-115">Key. c</span><span class="sxs-lookup"><span data-stu-id="a0afc-115">key.c</span></span>                  | <span data-ttu-id="a0afc-116">Contient une clé d’authentification factice.</span><span class="sxs-lookup"><span data-stu-id="a0afc-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="a0afc-117">loghelp. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-117">loghelp.cpp</span></span>            | <span data-ttu-id="a0afc-118">Contient des fonctions qui journalisent l’activité et les erreurs à l’aide de la classe **WMDMLogger** , qui est implémentée dans le fichier système WMDMLOG.dll.</span><span class="sxs-lookup"><span data-stu-id="a0afc-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="a0afc-119">MDServiceProvider. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="a0afc-120">Implémente une classe, CMDServiceProvider, qui implémente les interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) et IComponentAuthenticate.</span><span class="sxs-lookup"><span data-stu-id="a0afc-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="a0afc-121">MDSP. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-121">mdsp.cpp</span></span>               | <span data-ttu-id="a0afc-122">Point d’entrée et code d’enregistrement de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a0afc-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="a0afc-123">MDSPDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="a0afc-124">Implémente une classe, CMDSPDevice, qui implémente les interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)et **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="a0afc-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="a0afc-125">MDSPEnumDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="a0afc-126">Implémente une classe, CMDSPEnumDevice, qui implémente l’interface [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .</span><span class="sxs-lookup"><span data-stu-id="a0afc-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="a0afc-127">MDSPEnumStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="a0afc-128">Implémente une classe, CMDSPEnumStorage, qui implémente l’interface [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="a0afc-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="a0afc-129">MDSPStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="a0afc-130">Implémente une classe, CMDSPStorage, qui implémente les interfaces [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)et [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .</span><span class="sxs-lookup"><span data-stu-id="a0afc-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="a0afc-131">MDSPStorageGlobals. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="a0afc-132">Implémente une classe, CMDSPStorageGlobals, qui implémente l’interface [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .</span><span class="sxs-lookup"><span data-stu-id="a0afc-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="a0afc-133">MDSPutil. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="a0afc-134">Contient diverses fonctions utilitaires pour la gestion des appareils et des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a0afc-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="a0afc-135">PropPage. cpp</span><span class="sxs-lookup"><span data-stu-id="a0afc-135">proppage.cpp</span></span>           | <span data-ttu-id="a0afc-136">Implémente une classe, CPropPage, qui hérite des classes ATL **IPropertyPageImpl** (pour implémenter IPropertyPage) et **CDialogImpl**, qui hérite de la classe ATL CDialogImpl (pour gérer les fenêtres et les messages).</span><span class="sxs-lookup"><span data-stu-id="a0afc-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a0afc-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0afc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0afc-138">**Exemple de fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="a0afc-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




