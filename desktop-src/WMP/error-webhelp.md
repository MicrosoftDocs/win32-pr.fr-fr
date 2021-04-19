---
title: Erreur. Webhelp, méthode
description: La méthode Webhelp ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro). | Erreur. Webhelp, méthode
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- méthode Webhelp lecteur Windows Media
- méthode Webhelp lecteur Windows Media, classe d’erreur
- Classe d’erreur lecteur Windows Media, méthode Webhelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537622"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="b1eac-107">Erreur. Webhelp, méthode</span><span class="sxs-lookup"><span data-stu-id="b1eac-107">Error.webHelp method</span></span>

<span data-ttu-id="b1eac-108">La méthode **Webhelp** ouvre la page d’aide Web du lecteur Windows Media pour afficher des informations supplémentaires sur la première erreur de la file d’attente des erreurs (index zéro).</span><span class="sxs-lookup"><span data-stu-id="b1eac-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1eac-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1eac-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="b1eac-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1eac-110">Parameters</span></span>

<span data-ttu-id="b1eac-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b1eac-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1eac-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1eac-112">Return value</span></span>

<span data-ttu-id="b1eac-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b1eac-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1eac-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b1eac-114">Remarks</span></span>

<span data-ttu-id="b1eac-115">Les pages d’aide Web contiennent toujours les informations les plus récentes et les plus détaillées sur les erreurs du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1eac-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="b1eac-116">Cette méthode transfère automatiquement les autres informations requises par l’aide Web, telles que la version du système d’exploitation utilisée.</span><span class="sxs-lookup"><span data-stu-id="b1eac-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="b1eac-117">Pour accéder directement aux pages d’aide Web, utilisez le code d’erreur suivant et les liens du centre d’aide et de support.</span><span class="sxs-lookup"><span data-stu-id="b1eac-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="b1eac-118">Informations de code d’erreur du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="b1eac-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="b1eac-119">Centre de solutions du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="b1eac-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="b1eac-120">**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.</span><span class="sxs-lookup"><span data-stu-id="b1eac-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="b1eac-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="b1eac-121">Examples</span></span>

<span data-ttu-id="b1eac-122">L’exemple suivant crée un élément bouton HTML qui lance la page d’aide Web du lecteur Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b1eac-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="b1eac-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b1eac-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="b1eac-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1eac-124">Requirements</span></span>



| <span data-ttu-id="b1eac-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1eac-125">Requirement</span></span> | <span data-ttu-id="b1eac-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1eac-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1eac-127">Version</span><span class="sxs-lookup"><span data-stu-id="b1eac-127">Version</span></span><br/> | <span data-ttu-id="b1eac-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b1eac-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b1eac-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b1eac-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1eac-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1eac-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1eac-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1eac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1eac-132">**Error, objet**</span><span class="sxs-lookup"><span data-stu-id="b1eac-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





