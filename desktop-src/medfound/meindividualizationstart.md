---
description: Déclenché par le moteur de stratégie lorsque l’individualisation est sur le le début. L’individualisation est effectuée à l’aide de l’implémentation d’applications de l’interface IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Événement MEIndividualizationStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518162"
---
# <a name="meindividualizationstart-event"></a><span data-ttu-id="b4819-104">Événement MEIndividualizationStart</span><span class="sxs-lookup"><span data-stu-id="b4819-104">MEIndividualizationStart event</span></span>

<span data-ttu-id="b4819-105">Déclenché par le moteur de stratégie lorsque l’individualisation est sur le le début.</span><span class="sxs-lookup"><span data-stu-id="b4819-105">Raised by the policy engine when individualization is about to begin.</span></span> <span data-ttu-id="b4819-106">L’individualisation est effectuée à l’aide de l’implémentation de l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.</span><span class="sxs-lookup"><span data-stu-id="b4819-106">Individualization is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="b4819-107">Une application individualisée est une application qui a reçu une mise à niveau de ses composants de gestion des droits numériques (DRM) qui la différencie de toutes les autres copies de la même application.</span><span class="sxs-lookup"><span data-stu-id="b4819-107">An individualized application is one that has received an upgrade to its digital rights management (DRM) components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="b4819-108">Les propriétaires de contenu peuvent exiger que leurs fichiers protégés soient lus uniquement sur une application qui a été individualisée.</span><span class="sxs-lookup"><span data-stu-id="b4819-108">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

## <a name="event-values"></a><span data-ttu-id="b4819-109">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="b4819-109">Event values</span></span>

<span data-ttu-id="b4819-110">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4819-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b4819-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b4819-111">VARTYPE</span></span>              | <span data-ttu-id="b4819-112">Description</span><span class="sxs-lookup"><span data-stu-id="b4819-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b4819-113">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="b4819-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b4819-114">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="b4819-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b4819-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b4819-115">Remarks</span></span>

<span data-ttu-id="b4819-116">Lorsque l’acquisition de licence est terminée, le moteur de stratégie déclenche l’événement [MEIndividualizationCompleted](meindividualizationcompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b4819-116">When license acquisition is completed, the policy engine raises the [MEIndividualizationCompleted](meindividualizationcompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4819-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4819-117">Requirements</span></span>



| <span data-ttu-id="b4819-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4819-118">Requirement</span></span> | <span data-ttu-id="b4819-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4819-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4819-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4819-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4819-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4819-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4819-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4819-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4819-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4819-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4819-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4819-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4819-125"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4819-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4819-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4819-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4819-127">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4819-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




