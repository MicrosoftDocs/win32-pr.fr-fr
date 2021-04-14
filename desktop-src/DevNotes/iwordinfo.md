---
description: L’interface IWordInfo est un composant de ressource de langue spécifique au japonais. L’objet analyse le texte et identifie les mots individuels, en retournant les mots de la chaîne ou retourne les formes de dictionnaire (racine) des mots dans le texte de la chaîne.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interface IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522975"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="b15ce-104">Interface IWordInfo</span><span class="sxs-lookup"><span data-stu-id="b15ce-104">IWordInfo interface</span></span>

<span data-ttu-id="b15ce-105">\[Cette interface est obsolète et n’est pas prise en charge sur Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="b15ce-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="b15ce-106">L’interface **IWordInfo** est un composant de ressource de langue spécifique au japonais.</span><span class="sxs-lookup"><span data-stu-id="b15ce-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="b15ce-107">L’objet analyse le texte et identifie les mots individuels, en retournant les mots de la chaîne ou retourne les formes de dictionnaire (racine) des mots dans le texte de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b15ce-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="b15ce-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b15ce-108">Members</span></span>

<span data-ttu-id="b15ce-109">L’interface **IWordInfo** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b15ce-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b15ce-110">**IWordInfo** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b15ce-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="b15ce-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b15ce-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b15ce-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b15ce-112">Methods</span></span>

<span data-ttu-id="b15ce-113">L’interface **IWordInfo** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b15ce-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="b15ce-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="b15ce-114">Method</span></span>        | <span data-ttu-id="b15ce-115">Description</span><span class="sxs-lookup"><span data-stu-id="b15ce-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15ce-116">**BreakText**</span><span class="sxs-lookup"><span data-stu-id="b15ce-116">**BreakText**</span></span> | <span data-ttu-id="b15ce-117">Analyse le texte pour identifier les mots et fournit les résultats à l’objet [WordSink](/previous-versions//ms691570(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b15ce-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b15ce-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b15ce-118">Remarks</span></span>

<span data-ttu-id="b15ce-119">Cette interface est utilisée pour récupérer les césures lexicales ou les formulaires de dictionnaire du texte à analyser.</span><span class="sxs-lookup"><span data-stu-id="b15ce-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="b15ce-120">Le format de dictionnaire d’un mot est le formulaire uninflected du mot.</span><span class="sxs-lookup"><span data-stu-id="b15ce-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="b15ce-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b15ce-121">Requirements</span></span>



| <span data-ttu-id="b15ce-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b15ce-122">Requirement</span></span> | <span data-ttu-id="b15ce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b15ce-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b15ce-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b15ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b15ce-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b15ce-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b15ce-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b15ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b15ce-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b15ce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b15ce-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b15ce-128">End of client support</span></span><br/>    | <span data-ttu-id="b15ce-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b15ce-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b15ce-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b15ce-130">End of server support</span></span><br/>    | <span data-ttu-id="b15ce-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b15ce-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b15ce-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b15ce-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b15ce-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b15ce-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b15ce-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b15ce-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15ce-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="b15ce-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="b15ce-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b15ce-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
