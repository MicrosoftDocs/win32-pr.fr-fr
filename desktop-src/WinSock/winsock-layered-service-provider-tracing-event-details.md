---
description: Détails du suivi de modification du catalogue Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Détails du suivi de modification du catalogue Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114287"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="a9055-103">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="a9055-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="a9055-104">Les fournisseurs de services en couche sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="a9055-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="a9055-105">À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="a9055-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="a9055-106">Le suivi des événements de modification du catalogue Winsock pour les fournisseurs de services en couche (LSP) est lié à l’installation du LSP, à la suppression du LSP, à la désactivation LSP et aux opérations de réinitialisation du catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="a9055-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="a9055-107">Tous les événements suivants sont écrits sur le canal *opérationnel Microsoft-Windows-Winsock-ws2help/Operational* , qui est différent de l’autre suivi d’événements réseau Winsock enregistré sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a9055-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="a9055-108">Les éléments suivants décrivent chacun des événements Winsock LSP qui peuvent être suivis et détaillent les paramètres et les informations qui sont journalisés.</span><span class="sxs-lookup"><span data-stu-id="a9055-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="a9055-109">Installation du LSP</span><span class="sxs-lookup"><span data-stu-id="a9055-109">LSP Install</span></span>

<span data-ttu-id="a9055-110">ID d’événement = 1</span><span class="sxs-lookup"><span data-stu-id="a9055-110">Event ID = 1</span></span>

<span data-ttu-id="a9055-111">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="a9055-111">Level = 4 (Information)</span></span>

<span data-ttu-id="a9055-112">Les événements LSP Winsock suivants sont suivis pour une opération d’installation LSP :</span><span class="sxs-lookup"><span data-stu-id="a9055-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="a9055-113">Une entrée de protocole est installée dans le catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="a9055-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="a9055-114">Les paramètres suivants sont consignés pour un événement d’installation LSP :</span><span class="sxs-lookup"><span data-stu-id="a9055-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="a9055-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a9055-115">Parameter</span></span>                                                                                                | <span data-ttu-id="a9055-116">Description</span><span class="sxs-lookup"><span data-stu-id="a9055-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9055-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nom LSP</span><span class="sxs-lookup"><span data-stu-id="a9055-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="a9055-118">Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="a9055-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="a9055-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue</span><span class="sxs-lookup"><span data-stu-id="a9055-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="a9055-120">Le catalogue Winsock (32 bits ou 64 bits) sur lequel est installé le LSP.</span><span class="sxs-lookup"><span data-stu-id="a9055-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="a9055-121">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="a9055-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="a9055-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>D'</span><span class="sxs-lookup"><span data-stu-id="a9055-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="a9055-123">Nom de fichier du module de l’application effectuant l’appel d’installation LSP.</span><span class="sxs-lookup"><span data-stu-id="a9055-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="a9055-124"><span id="GUID"></span><span id="guid"></span>UNIQUES</span><span class="sxs-lookup"><span data-stu-id="a9055-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="a9055-125">Valeur GUID du fournisseur de transport Winsock sous lequel le LSP est installé.</span><span class="sxs-lookup"><span data-stu-id="a9055-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="a9055-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie</span><span class="sxs-lookup"><span data-stu-id="a9055-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="a9055-127">Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="a9055-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="a9055-128">Désinstallation de LSP</span><span class="sxs-lookup"><span data-stu-id="a9055-128">LSP Uninstall</span></span>

<span data-ttu-id="a9055-129">ID d’événement = 2</span><span class="sxs-lookup"><span data-stu-id="a9055-129">Event ID = 2</span></span>

<span data-ttu-id="a9055-130">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="a9055-130">Level = 4 (Information)</span></span>

<span data-ttu-id="a9055-131">Les événements LSP Winsock suivants sont suivis pour une opération de désinstallation LSP :</span><span class="sxs-lookup"><span data-stu-id="a9055-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="a9055-132">Une entrée de protocole est supprimée du catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="a9055-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="a9055-133">Les paramètres suivants sont consignés pour un événement de désinstallation LSP :</span><span class="sxs-lookup"><span data-stu-id="a9055-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="a9055-134">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a9055-134">Parameter</span></span>                                                                                                | <span data-ttu-id="a9055-135">Description</span><span class="sxs-lookup"><span data-stu-id="a9055-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9055-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nom LSP</span><span class="sxs-lookup"><span data-stu-id="a9055-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="a9055-137">Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="a9055-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="a9055-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue</span><span class="sxs-lookup"><span data-stu-id="a9055-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="a9055-139">Le catalogue Winsock (32 bits ou 64 bits) dans lequel le LSP est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a9055-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="a9055-140">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="a9055-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="a9055-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>D'</span><span class="sxs-lookup"><span data-stu-id="a9055-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="a9055-142">Nom du fichier de module de l’application qui effectue l’appel de l’LSP de suppression.</span><span class="sxs-lookup"><span data-stu-id="a9055-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="a9055-143"><span id="GUID"></span><span id="guid"></span>UNIQUES</span><span class="sxs-lookup"><span data-stu-id="a9055-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="a9055-144">Valeur GUID du fournisseur de transport Winsock duquel le LSP est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a9055-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="a9055-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie</span><span class="sxs-lookup"><span data-stu-id="a9055-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="a9055-146">Membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="a9055-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="a9055-147">Désactivation LSP</span><span class="sxs-lookup"><span data-stu-id="a9055-147">LSP Disable</span></span>

<span data-ttu-id="a9055-148">ID d’événement = 3</span><span class="sxs-lookup"><span data-stu-id="a9055-148">Event ID = 3</span></span>

<span data-ttu-id="a9055-149">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="a9055-149">Level = 4 (Information)</span></span>

<span data-ttu-id="a9055-150">Les événements LSP Winsock suivants sont suivis pour une opération de désactivation LSP :</span><span class="sxs-lookup"><span data-stu-id="a9055-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="a9055-151">Une entrée de protocole est désactivée dans le catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="a9055-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="a9055-152">Les paramètres suivants sont consignés pour un événement de désactivation LSP :</span><span class="sxs-lookup"><span data-stu-id="a9055-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="a9055-153">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a9055-153">Parameter</span></span>                                                                                                | <span data-ttu-id="a9055-154">Description</span><span class="sxs-lookup"><span data-stu-id="a9055-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9055-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nom LSP</span><span class="sxs-lookup"><span data-stu-id="a9055-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="a9055-156">Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="a9055-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="a9055-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue</span><span class="sxs-lookup"><span data-stu-id="a9055-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="a9055-158">Le catalogue Winsock (32 bits ou 64 bits) sur lequel est désactivé le LSP.</span><span class="sxs-lookup"><span data-stu-id="a9055-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="a9055-159">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="a9055-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="a9055-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>D'</span><span class="sxs-lookup"><span data-stu-id="a9055-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="a9055-161">Nom du fichier de module de l’application qui effectue l’appel de désactivation du LSP.</span><span class="sxs-lookup"><span data-stu-id="a9055-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="a9055-162"><span id="GUID"></span><span id="guid"></span>UNIQUES</span><span class="sxs-lookup"><span data-stu-id="a9055-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="a9055-163">Valeur GUID du fournisseur de transport Winsock sur lequel le LSP est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a9055-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="a9055-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Catégorie</span><span class="sxs-lookup"><span data-stu-id="a9055-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="a9055-165">Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="a9055-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="a9055-166">Réinitialisation du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="a9055-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="a9055-167">ID d’événement = 4</span><span class="sxs-lookup"><span data-stu-id="a9055-167">Event ID = 4</span></span>

<span data-ttu-id="a9055-168">Niveau = 4 (informations)</span><span class="sxs-lookup"><span data-stu-id="a9055-168">Level = 4 (Information)</span></span>

<span data-ttu-id="a9055-169">Les événements LSP Winsock suivants sont suivis pour une opération de réinitialisation du catalogue Winsock :</span><span class="sxs-lookup"><span data-stu-id="a9055-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="a9055-170">Le catalogue Winsock est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="a9055-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="a9055-171">Les paramètres suivants sont enregistrés pour un événement de réinitialisation du catalogue Winsock :</span><span class="sxs-lookup"><span data-stu-id="a9055-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="a9055-172">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a9055-172">Parameter</span></span>                                                                                        | <span data-ttu-id="a9055-173">Description</span><span class="sxs-lookup"><span data-stu-id="a9055-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9055-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue</span><span class="sxs-lookup"><span data-stu-id="a9055-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="a9055-175">Le catalogue Winsock (32 bits ou 64 bits) en cours de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="a9055-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="a9055-176">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="a9055-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a9055-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9055-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9055-178">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="a9055-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="a9055-179">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="a9055-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="a9055-180">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="a9055-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="a9055-181">Détails du suivi d’événements réseau Winsock</span><span class="sxs-lookup"><span data-stu-id="a9055-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
