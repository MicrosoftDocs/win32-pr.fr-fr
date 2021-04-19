---
title: THÈME. showErrorDialog
description: La méthode showErrorDialog affiche la boîte de dialogue d’erreur standard.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEMe. showErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528532"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="75248-104">THÈME. showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="75248-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="75248-105">La méthode **showErrorDialog** affiche la boîte de dialogue d’erreur standard.</span><span class="sxs-lookup"><span data-stu-id="75248-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="75248-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75248-106">Parameters</span></span>

<span data-ttu-id="75248-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="75248-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75248-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75248-108">Return Value</span></span>

<span data-ttu-id="75248-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="75248-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75248-110">Notes</span><span class="sxs-lookup"><span data-stu-id="75248-110">Remarks</span></span>

<span data-ttu-id="75248-111">Si **Settings. enableErrorDialogs** a la valeur false, cette méthode peut être utilisée pour afficher la boîte de dialogue d’erreur par programmation.</span><span class="sxs-lookup"><span data-stu-id="75248-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="75248-112">S’il n’y a pas d’erreurs dans la file d’attente des erreurs, la boîte de dialogue d’erreur ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="75248-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="75248-113">Pour le lecteur Windows Media série 9 ou version ultérieure, cette méthode doit être appelée à partir du gestionnaire d’événements d’erreur.</span><span class="sxs-lookup"><span data-stu-id="75248-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="75248-114">Le lecteur Windows Media série 9 ou version ultérieure efface la file d’attente d’erreurs pour les apparences après le déclenchement de l’événement d’erreur.</span><span class="sxs-lookup"><span data-stu-id="75248-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="75248-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75248-115">Requirements</span></span>



| <span data-ttu-id="75248-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75248-116">Requirement</span></span> | <span data-ttu-id="75248-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="75248-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="75248-118">Version</span><span class="sxs-lookup"><span data-stu-id="75248-118">Version</span></span><br/> | <span data-ttu-id="75248-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="75248-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75248-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75248-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75248-121">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="75248-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="75248-122">**Paramètres. enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="75248-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





