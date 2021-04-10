---
title: EC_WMT_INDEX_EVENT (kit de développement logiciel (SDK) Windows Media format 11)
description: événement d’index de l’WMT de la EC \_ \_ \_
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Kit de développement logiciel (SDK) Windows Media format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format), EC_WMT_INDEX_EVENT
- ASF (format avancé des systèmes), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032187"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="f176d-108">EC_WMT_INDEX_EVENT (kit de développement logiciel (SDK) Windows Media format 11)</span><span class="sxs-lookup"><span data-stu-id="f176d-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="f176d-109">Envoyé par le kit de développement logiciel (SDK) de format Windows Media lorsqu’une application utilise le writer ASF pour indexer les fichiers Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="f176d-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="f176d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f176d-110">Parameters</span></span>

<span data-ttu-id="f176d-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f176d-111">*lParam1*</span></span>

<span data-ttu-id="f176d-112">Il peut s’agir de l’un des messages d' **\_ État WMT** suivants.</span><span class="sxs-lookup"><span data-stu-id="f176d-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="f176d-113">Message</span><span class="sxs-lookup"><span data-stu-id="f176d-113">Message</span></span>              | <span data-ttu-id="f176d-114">Description</span><span class="sxs-lookup"><span data-stu-id="f176d-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="f176d-115">WMT \_ démarré</span><span class="sxs-lookup"><span data-stu-id="f176d-115">WMT\_STARTED</span></span>         | <span data-ttu-id="f176d-116">L’indexation a commencé.</span><span class="sxs-lookup"><span data-stu-id="f176d-116">Indexing has begun.</span></span> <span data-ttu-id="f176d-117">*lParam2* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f176d-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="f176d-118">WMT \_ fermé</span><span class="sxs-lookup"><span data-stu-id="f176d-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="f176d-119">L’indexation est terminée.</span><span class="sxs-lookup"><span data-stu-id="f176d-119">Indexing has been completed.</span></span> <span data-ttu-id="f176d-120">*lParam2* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f176d-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="f176d-121">progression de l' \_ index WMT \_</span><span class="sxs-lookup"><span data-stu-id="f176d-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="f176d-122">L’indexation est en cours.</span><span class="sxs-lookup"><span data-stu-id="f176d-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="f176d-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f176d-123">*lParam2*</span></span>

<span data-ttu-id="f176d-124">Si *lParam1* a été \_ fermé par WMT ou si WMT \_ a démarré, *lParam2* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f176d-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="f176d-125">Si *lParam1* est \_ \_ la progression de l’index WMT, *lParam2* est une **valeur DWORD** qui exprime la progression en pourcentage de la taille totale du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f176d-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f176d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f176d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f176d-127">**Informations de référence sur DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="f176d-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 




