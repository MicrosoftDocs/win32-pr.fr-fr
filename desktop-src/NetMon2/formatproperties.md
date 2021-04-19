---
description: La fonction d’exportation FormatProperties met en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau. Si vous souhaitez afficher des données dans le volet d’informations, vous devez implémenter la fonction d’exportation FormatProperties dans toutes les dll de l’analyseur.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Fonction de rappel FormatProperties (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544212"
---
# <a name="formatproperties-callback-function"></a><span data-ttu-id="42c82-104">FormatProperties fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="42c82-104">FormatProperties callback function</span></span>

<span data-ttu-id="42c82-105">La fonction d’exportation **FormatProperties** met en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="42c82-105">The **FormatProperties** export function formats the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="42c82-106">Si vous souhaitez afficher des données dans le volet d’informations, vous devez implémenter la fonction d’exportation **FormatProperties** dans toutes les dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="42c82-106">If you want to display data in the details pane, you must implement the **FormatProperties** export function in all parser DLLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c82-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42c82-107">Syntax</span></span>


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a><span data-ttu-id="42c82-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42c82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c82-109">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42c82-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c82-110">Handle vers le frame en cours d’analyse.</span><span class="sxs-lookup"><span data-stu-id="42c82-110">Handle to the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="42c82-111">*lpFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42c82-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c82-112">Pointeur vers le premier octet d’un frame.</span><span class="sxs-lookup"><span data-stu-id="42c82-112">Pointer to the first byte of a frame.</span></span>

</dd> <dt>

<span data-ttu-id="42c82-113">*lpProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42c82-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c82-114">Pointeur vers le début des données de protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="42c82-114">Pointer to the beginning of the protocol data in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="42c82-115">*nPropertyInsts* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42c82-115">*nPropertyInsts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c82-116">Nombre de structures [PROPERTYINST](propertyinst.md) fournies par *lpPropInst*.</span><span class="sxs-lookup"><span data-stu-id="42c82-116">Number of [PROPERTYINST](propertyinst.md) structures provided by *lpPropInst*.</span></span>

</dd> <dt>

<span data-ttu-id="42c82-117">*lpPropInst* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42c82-117">*lpPropInst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c82-118">Pointeur vers un tableau de structures [PROPERTYINST](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="42c82-118">Pointer to an array of [PROPERTYINST](propertyinst.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c82-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42c82-119">Return value</span></span>

<span data-ttu-id="42c82-120">Si la fonction réussit, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="42c82-120">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="42c82-121">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="42c82-121">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="42c82-122">Notes</span><span class="sxs-lookup"><span data-stu-id="42c82-122">Remarks</span></span>

<span data-ttu-id="42c82-123">Moniteur réseau appelle la fonction **FormatProperties** pour afficher les données dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="42c82-123">Network Monitor calls the **FormatProperties** function to display data in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="42c82-124">En règle générale, **FormatProperties** est appelé pour mettre en forme la ligne de résumé pour un protocole, puis pour mettre en forme toutes les instances de propriété du protocole dans un frame.</span><span class="sxs-lookup"><span data-stu-id="42c82-124">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="42c82-125">Toutefois, Moniteur réseau ne garantit pas le nombre de fois où il appelle **FormatProperties** pour un analyseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="42c82-125">However, Network Monitor does not guarantee the number of times it calls **FormatProperties** for a specific parser.</span></span>

<span data-ttu-id="42c82-126">Pendant l’implémentation de la fonction **FormatProperties** , l’analyseur appelle indirectement la fonction [FormatPropertyInstance](formatpropertyinstance.md) pour utiliser le formateur générique fourni par Moniteur réseau, ou il peut appeler une procédure de formateur personnalisée définie par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="42c82-126">During the implementation of the **FormatProperties** function, the parser indirectly calls the [FormatPropertyInstance](formatpropertyinstance.md) function to use the generic formatter that Network Monitor provides, or it can call a custom formatter procedure that is defined by the parser.</span></span> <span data-ttu-id="42c82-127">L’un des formateurs doit être appelé pour chaque structure [PROPERTYINST](propertyinst.md) transmise à la dll de l’analyseur dans le paramètre *lpPropInst* .</span><span class="sxs-lookup"><span data-stu-id="42c82-127">One of the formatters must be called for each [PROPERTYINST](propertyinst.md) structure passed to the parser DLL in the *lpPropInst* parameter.</span></span>



| <span data-ttu-id="42c82-128">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="42c82-128">For Information on</span></span>                                          | <span data-ttu-id="42c82-129">Consultez</span><span class="sxs-lookup"><span data-stu-id="42c82-129">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="42c82-130">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="42c82-130">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="42c82-131">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="42c82-131">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="42c82-132">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="42c82-132">Which entry points are included in the parser DLL.</span></span>          | [<span data-ttu-id="42c82-133">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="42c82-133">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="42c82-134">L’implémentation de **FormatProperties**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="42c82-134">How to implement **FormatProperties**  includes an example.</span></span> | [<span data-ttu-id="42c82-135">Implémentation de FormatProperties</span><span class="sxs-lookup"><span data-stu-id="42c82-135">Implementing FormatProperties</span></span>](implementing-formatproperties.md) |
| <span data-ttu-id="42c82-136">Comment le formateur générique formate les différents types de données.</span><span class="sxs-lookup"><span data-stu-id="42c82-136">How the generic formatter formats different types of data.</span></span>  | [<span data-ttu-id="42c82-137">Sortie de formateur générique</span><span class="sxs-lookup"><span data-stu-id="42c82-137">Generic Formatter Output</span></span>](generic-formatter-output.md)           |



 

## <a name="requirements"></a><span data-ttu-id="42c82-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42c82-138">Requirements</span></span>



| <span data-ttu-id="42c82-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42c82-139">Requirement</span></span> | <span data-ttu-id="42c82-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="42c82-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42c82-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c82-141">Minimum supported client</span></span><br/> | <span data-ttu-id="42c82-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42c82-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42c82-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42c82-143">Minimum supported server</span></span><br/> | <span data-ttu-id="42c82-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42c82-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="42c82-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="42c82-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="42c82-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="42c82-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c82-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42c82-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c82-148">FormatPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="42c82-148">FormatPropertyInstance</span></span>](formatpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="42c82-149">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="42c82-149">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> <dt>

[<span data-ttu-id="42c82-150">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="42c82-150">PROPERTYINST</span></span>](propertyinst.md)
</dt> </dl>

 

 




