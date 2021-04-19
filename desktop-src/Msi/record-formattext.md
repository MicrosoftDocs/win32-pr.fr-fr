---
description: La méthode FormatText de l’objet record met en forme les champs en fonction du modèle dans le champ 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Record. FormatText, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542682"
---
# <a name="recordformattext-method"></a><span data-ttu-id="8e241-103">Record. FormatText, méthode</span><span class="sxs-lookup"><span data-stu-id="8e241-103">Record.FormatText method</span></span>

<span data-ttu-id="8e241-104">La méthode **FormatText** de l’objet [**Record**](record-object.md) met en forme les champs en fonction du modèle dans le champ 0.</span><span class="sxs-lookup"><span data-stu-id="8e241-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e241-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e241-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="8e241-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e241-106">Parameters</span></span>

<span data-ttu-id="8e241-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8e241-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e241-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e241-108">Return value</span></span>

<span data-ttu-id="8e241-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8e241-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e241-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8e241-110">Remarks</span></span>

<span data-ttu-id="8e241-111">La méthode **FormatText** suit les fonctionnalités de la fonction [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) si **MsiFormatRecord** a reçu un handle de programme d’installation null en tant que premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="8e241-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="8e241-112">Par conséquent, seuls les paramètres de champ d’enregistrement sont traités et les propriétés ne sont pas disponibles pour la substitution.</span><span class="sxs-lookup"><span data-stu-id="8e241-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="8e241-113">Par exemple, une chaîne telle que « mettre en forme ce champ : \[ 1 \] , mettre en forme cette propriété : \[ propriété \] » est résolue en « mettre en forme ce champ : valeur du champ 1, mettre en forme cette propriété : \[ propriété \] ».</span><span class="sxs-lookup"><span data-stu-id="8e241-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="8e241-114">Les paramètres qui doivent être [mis en forme](formatted.md) sont placés entre crochets \[ ... \] .</span><span class="sxs-lookup"><span data-stu-id="8e241-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="8e241-115">Les crochets peuvent être itérés, car les substitutions sont résolues de l’intérieur vers l’extérieur.</span><span class="sxs-lookup"><span data-stu-id="8e241-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="8e241-116">Si une partie de la chaîne est entourée d’accolades {} et ne contient pas de crochets, elle reste inchangée, y compris les accolades.</span><span class="sxs-lookup"><span data-stu-id="8e241-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="8e241-117">Remarque dans le cas des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md), **FormatText** ne prend en charge qu’un ensemble limité de propriétés : les propriétés CustomActionData et ProductCode.</span><span class="sxs-lookup"><span data-stu-id="8e241-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="8e241-118">Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="8e241-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e241-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e241-119">Requirements</span></span>



| <span data-ttu-id="8e241-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e241-120">Requirement</span></span> | <span data-ttu-id="8e241-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e241-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e241-122">Version</span><span class="sxs-lookup"><span data-stu-id="8e241-122">Version</span></span><br/> | <span data-ttu-id="8e241-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e241-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8e241-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8e241-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8e241-125">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e241-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8e241-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8e241-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e241-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e241-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8e241-128">IID</span><span class="sxs-lookup"><span data-stu-id="8e241-128">IID</span></span><br/>     | <span data-ttu-id="8e241-129">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8e241-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="8e241-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e241-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e241-131">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="8e241-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="8e241-132">Correct</span><span class="sxs-lookup"><span data-stu-id="8e241-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="8e241-133">Types de données de colonne</span><span class="sxs-lookup"><span data-stu-id="8e241-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




