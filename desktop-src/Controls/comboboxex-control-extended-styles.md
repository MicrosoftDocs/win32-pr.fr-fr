---
title: Styles étendus de contrôle ComboBoxEx (CommCtrl. h)
description: Prendre en charge les styles étendus répertoriés dans cette section, ainsi que la plupart des styles de contrôle de zone de liste modifiable standard.
ms.assetid: 4741ac5e-1c46-4fd3-9174-b4ceb479261f
topic_type:
- apiref
api_name:
- CBES_EX_CASESENSITIVE
- CBES_EX_NOEDITIMAGE
- CBES_EX_NOEDITIMAGEINDENT
- CBES_EX_NOSIZELIMIT
- CBES_EX_PATHWORDBREAKPROC
- CBES_EX_TEXTENDELLIPSIS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71dc92264dbd1bd2f5a4b1136d9a6138e1fcffa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528115"
---
# <a name="comboboxex-control-extended-styles"></a><span data-ttu-id="b97b7-103">Styles étendus de contrôle ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="b97b7-103">ComboBoxEx Control Extended Styles</span></span>

<span data-ttu-id="b97b7-104">Prendre en charge les styles étendus répertoriés dans cette section, ainsi que la plupart des styles de contrôle de zone de liste modifiable standard.</span><span class="sxs-lookup"><span data-stu-id="b97b7-104">Support the extended styles that are listed in this section as well as most standard combo box control styles.</span></span>



| <span data-ttu-id="b97b7-105">Constante</span><span class="sxs-lookup"><span data-stu-id="b97b7-105">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="b97b7-106">Description</span><span class="sxs-lookup"><span data-stu-id="b97b7-106">Description</span></span>                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CBES_EX_CASESENSITIVE"></span><span id="cbes_ex_casesensitive"></span><dl> <span data-ttu-id="b97b7-107"><dt>**CBES \_ ex \_ CaseSensitive**</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-107"><dt>**CBES\_EX\_CASESENSITIVE**</dt></span></span> </dl>             | <span data-ttu-id="b97b7-108">Les recherches **BSTR** dans la liste respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="b97b7-108">**BSTR** searches in the list will be case sensitive.</span></span> <span data-ttu-id="b97b7-109">Cela comprend les recherches à la suite du texte tapé dans la zone d’édition et du \_ message CB FindExactString.</span><span class="sxs-lookup"><span data-stu-id="b97b7-109">This includes searches as a result of text being typed in the edit box and the CB\_FINDSTRINGEXACT message.</span></span><br/>                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGE"></span><span id="cbes_ex_noeditimage"></span><dl> <span data-ttu-id="b97b7-110"><dt>**CBES \_ ex \_ NOEDITIMAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-110"><dt>**CBES\_EX\_NOEDITIMAGE**</dt></span></span> </dl>                   | <span data-ttu-id="b97b7-111">La zone d’édition et la liste déroulante n’affichent pas d’images d’élément.</span><span class="sxs-lookup"><span data-stu-id="b97b7-111">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOEDITIMAGEINDENT"></span><span id="cbes_ex_noeditimageindent"></span><dl> <span data-ttu-id="b97b7-112"><dt>**CBES \_ ex \_ NOEDITIMAGEINDENT**</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-112"><dt>**CBES\_EX\_NOEDITIMAGEINDENT**</dt></span></span> </dl> | <span data-ttu-id="b97b7-113">La zone d’édition et la liste déroulante n’affichent pas d’images d’élément.</span><span class="sxs-lookup"><span data-stu-id="b97b7-113">The edit box and the dropdown list will not display item images.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="CBES_EX_NOSIZELIMIT"></span><span id="cbes_ex_nosizelimit"></span><dl> <span data-ttu-id="b97b7-114"><dt>**CBES \_ ex \_ NOSIZELIMIT**</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-114"><dt>**CBES\_EX\_NOSIZELIMIT**</dt></span></span> </dl>                   | <span data-ttu-id="b97b7-115">Permet au contrôle ComboBoxEx d’être dimensionné verticalement plus petit que son contrôle de zone de liste déroulante contenu.</span><span class="sxs-lookup"><span data-stu-id="b97b7-115">Allows the ComboBoxEx control to be vertically sized smaller than its contained combo box control.</span></span> <span data-ttu-id="b97b7-116">Si la taille du ComboBoxEx est inférieure à celle de la zone de liste déroulante, la zone de liste déroulante est découpée.</span><span class="sxs-lookup"><span data-stu-id="b97b7-116">If the ComboBoxEx is sized smaller than the combo box, the combo box will be clipped.</span></span> <br/>                                                                                                                                  |
| <span id="CBES_EX_PATHWORDBREAKPROC"></span><span id="cbes_ex_pathwordbreakproc"></span><dl> <span data-ttu-id="b97b7-117"><dt>**CBES \_ ex \_ PATHWORDBREAKPROC**</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-117"><dt>**CBES\_EX\_PATHWORDBREAKPROC**</dt></span></span> </dl> | <span data-ttu-id="b97b7-118">Windows NT uniquement.</span><span class="sxs-lookup"><span data-stu-id="b97b7-118">Windows NT only.</span></span> <span data-ttu-id="b97b7-119">La zone d’édition utilise la barre oblique (/), la barre oblique inverse ( \) et les caractères point (.) comme délimiteurs de mots.</span><span class="sxs-lookup"><span data-stu-id="b97b7-119">The edit box will use the slash (/), backslash (\), and period (.) characters as word delimiters.</span></span> <span data-ttu-id="b97b7-120">Ainsi, les raccourcis clavier pour le déplacement du curseur Word par mot sont effectifs dans les noms de chemin d’accès et les URL.</span><span class="sxs-lookup"><span data-stu-id="b97b7-120">This makes keyboard shortcuts for word-by-word cursor movement effective in path names and URLs.</span></span><br/>                                                                                                       |
| <span id="CBES_EX_TEXTENDELLIPSIS"></span><span id="cbes_ex_textendellipsis"></span><dl> <span data-ttu-id="b97b7-121"><dt>**CBES \_ ex \_ TEXTENDELLIPSIS**</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-121"><dt>**CBES\_EX\_TEXTENDELLIPSIS**</dt></span></span> </dl>       | <span data-ttu-id="b97b7-122">**Windows Vista et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="b97b7-122">**Windows Vista and later.**</span></span> <span data-ttu-id="b97b7-123">Fait en sorte que les éléments dans la liste déroulante et la zone d’édition (lorsque la zone d’édition est en lecture seule) soient tronqués par des points de suspension (« ... ») et non simplement par le bord du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b97b7-123">Causes items in the drop-down list and the edit box (when the edit box is read only) to be truncated with an ellipsis ("...") rather than just clipped by the edge of the control.</span></span> <span data-ttu-id="b97b7-124">Cela est utile lorsque le contrôle doit être défini sur une largeur fixe, mais que les entrées de la liste peuvent être longues.</span><span class="sxs-lookup"><span data-stu-id="b97b7-124">This is useful when the control needs to be set to a fixed width, yet the entries in the list may be long.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b97b7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b97b7-125">Remarks</span></span>

<span data-ttu-id="b97b7-126">Vous définissez et récupérez les styles étendus de ComboBox à l’aide des messages [**CBEM \_ SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) et [**CBEM \_ GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="b97b7-126">You set and retrieve the combobox extended styles by using [**CBEM\_SETEXTENDEDSTYLE**](cbem-setextendedstyle.md) and [**CBEM\_GETEXTENDEDSTYLE**](cbem-getextendedstyle.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="b97b7-127">Si vous essayez de définir un style étendu pour un contrôle ComboBoxEx créé avec le style [**CBS \_ simple**](combo-box-styles.md) , il se peut qu’il ne redessine pas correctement.</span><span class="sxs-lookup"><span data-stu-id="b97b7-127">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it might not repaint properly.</span></span> <span data-ttu-id="b97b7-128">Le **style \_ simple CBS** ne fonctionne pas correctement avec le \_ \_ style étendu CBES ex PATHWORDBREAKPROC.</span><span class="sxs-lookup"><span data-stu-id="b97b7-128">The **CBS\_SIMPLE** style also does not work properly with the CBES\_EX\_PATHWORDBREAKPROC extended style.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b97b7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b97b7-129">Requirements</span></span>



| <span data-ttu-id="b97b7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b97b7-130">Requirement</span></span> | <span data-ttu-id="b97b7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97b7-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b97b7-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b97b7-132">Header</span></span><br/> | <dl> <span data-ttu-id="b97b7-133"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b97b7-133"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





