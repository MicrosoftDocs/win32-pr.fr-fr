---
title: Fonctions des extensions NPS
description: Fonctions des extensions NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510271"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="fcfff-103">Fonctions des extensions NPS</span><span class="sxs-lookup"><span data-stu-id="fcfff-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="fcfff-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fcfff-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="fcfff-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="fcfff-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="fcfff-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="fcfff-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="fcfff-107">Application définie</span><span class="sxs-lookup"><span data-stu-id="fcfff-107">Application Defined</span></span>

<span data-ttu-id="fcfff-108">L’architecture des dll d’extension NPS prend en charge les fonctions exportées suivantes :</span><span class="sxs-lookup"><span data-stu-id="fcfff-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="fcfff-109">**RadiusExtensionFreeAttributes**</span><span class="sxs-lookup"><span data-stu-id="fcfff-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="fcfff-110">**RadiusExtensionInit**</span><span class="sxs-lookup"><span data-stu-id="fcfff-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="fcfff-111">**RadiusExtensionProcess**</span><span class="sxs-lookup"><span data-stu-id="fcfff-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="fcfff-112">**RadiusExtensionProcessEx**</span><span class="sxs-lookup"><span data-stu-id="fcfff-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="fcfff-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="fcfff-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="fcfff-114">**RadiusExtensionTerm**</span><span class="sxs-lookup"><span data-stu-id="fcfff-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="fcfff-115">Les fonctions [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) et [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="fcfff-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="fcfff-116">La DLL d’extension peut exporter [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) au lieu de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) ou [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span><span class="sxs-lookup"><span data-stu-id="fcfff-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="fcfff-117">Si la DLL d’extension exporte [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), elle doit également exporter [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span><span class="sxs-lookup"><span data-stu-id="fcfff-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="fcfff-118">Défini par le système</span><span class="sxs-lookup"><span data-stu-id="fcfff-118">System Defined</span></span>

<span data-ttu-id="fcfff-119">Lorsque NPS appelle une implémentation de [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS transmet à la fonction un pointeur vers une structure de [**\_ bloc de \_ contrôle \_ d’extension RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .</span><span class="sxs-lookup"><span data-stu-id="fcfff-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="fcfff-120">La structure de [**\_ bloc de \_ contrôle \_ d’extension RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contient des pointeurs de fonction vers les fonctions suivantes fournies par NPS :</span><span class="sxs-lookup"><span data-stu-id="fcfff-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="fcfff-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="fcfff-124">Les fonctions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) et [**GetResponse**](/previous-versions/ms688270(v=vs.85)) retournent des pointeurs vers une structure de type [**\_ \_ tableau d’attributs RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span><span class="sxs-lookup"><span data-stu-id="fcfff-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="fcfff-125">La structure du [**\_ \_ tableau d’attributs RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contient des pointeurs de fonction vers les fonctions suivantes fournies par NPS :</span><span class="sxs-lookup"><span data-stu-id="fcfff-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="fcfff-126">[**Complémentaires**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-128">[**GetSize,**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="fcfff-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fcfff-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 