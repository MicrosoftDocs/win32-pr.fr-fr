---
title: Interface ISoftKbd (Softkbdc. h)
description: L’interface ISoftKbd est utilisée par les applications et les services de texte pour implémenter un clavier logiciel.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- ISoftKbd interface Text Services Framework
- ISoftKbd interface Text Services Framework, Description
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510726"
---
# <a name="isoftkbd-interface"></a><span data-ttu-id="a0b63-105">Interface ISoftKbd</span><span class="sxs-lookup"><span data-stu-id="a0b63-105">ISoftKbd interface</span></span>

<span data-ttu-id="a0b63-106">L’interface **ISoftKbd** est utilisée par les applications et les services de texte pour implémenter un clavier logiciel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-106">The **ISoftKbd** interface is used by applications and text services to implement a soft keyboard.</span></span>

## <a name="members"></a><span data-ttu-id="a0b63-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a0b63-107">Members</span></span>

<span data-ttu-id="a0b63-108">L’interface **ISoftKbd** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a0b63-108">The **ISoftKbd** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a0b63-109">**ISoftKbd** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0b63-109">**ISoftKbd** also has these types of members:</span></span>

-   [<span data-ttu-id="a0b63-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0b63-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0b63-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0b63-111">Methods</span></span>

<span data-ttu-id="a0b63-112">L’interface **ISoftKbd** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a0b63-112">The **ISoftKbd** interface has these methods.</span></span>



| <span data-ttu-id="a0b63-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0b63-113">Method</span></span>                                                                                        | <span data-ttu-id="a0b63-114">Description</span><span class="sxs-lookup"><span data-stu-id="a0b63-114">Description</span></span>                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0b63-115">**AdviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="a0b63-115">**AdviseSoftKeyboardEventSink**</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)                   | <span data-ttu-id="a0b63-116">Installe un récepteur d’événements de clavier logiciel pour gérer les notifications OnKeySelection à partir du clavier logiciel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-116">Installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span><br/> |
| [<span data-ttu-id="a0b63-117">**CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="a0b63-117">**CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md) | <span data-ttu-id="a0b63-118">Crée une disposition de clavier logiciel à partir de la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a0b63-118">Creates a soft keyboard layout from the specified resource.</span></span><br/>                                        |
| [<span data-ttu-id="a0b63-119">**CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="a0b63-119">**CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | <span data-ttu-id="a0b63-120">Crée une disposition de clavier logiciel à partir du fichier XML spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0b63-120">Creates a soft keyboard layout from the specified XML file.</span></span><br/>                                        |
| [<span data-ttu-id="a0b63-121">**CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="a0b63-121">**CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)                         | <span data-ttu-id="a0b63-122">Crée une fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0b63-122">Creates a soft keyboard window.</span></span><br/>                                                                    |
| [<span data-ttu-id="a0b63-123">**DestroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="a0b63-123">**DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)                       | <span data-ttu-id="a0b63-124">Détruit une fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0b63-124">Destroys a soft keyboard window.</span></span><br/>                                                                   |
| [<span data-ttu-id="a0b63-125">**EnumSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="a0b63-125">**EnumSoftKeyboard**</span></span>](isoftkbd-enumsoftkeyboard.md)                                         | <span data-ttu-id="a0b63-126">Énumère les claviers logiciels possibles qui prennent en charge le langage spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0b63-126">Enumerates the possible soft keyboards that support the specified language.</span></span><br/>                        |
| [<span data-ttu-id="a0b63-127">**GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="a0b63-127">**GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)                               | <span data-ttu-id="a0b63-128">Récupère la couleur de clavier programmable correspondant au type de couleur fourni.</span><span class="sxs-lookup"><span data-stu-id="a0b63-128">Retrieves the soft keyboard color corresponding to the supplied color type.</span></span><br/>                        |
| [<span data-ttu-id="a0b63-129">**GetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="a0b63-129">**GetSoftKeyboardPosSize**</span></span>](isoftkbd-getsoftkeyboardpossize.md)                             | <span data-ttu-id="a0b63-130">Récupère la position de départ et la taille d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-130">Retrieves the starting position and size of a soft keyboard.</span></span><br/>                                       |
| [<span data-ttu-id="a0b63-131">**GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="a0b63-131">**GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)                           | <span data-ttu-id="a0b63-132">Récupère la police de texte utilisée par un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-132">Retrieves the text font used by a soft keyboard.</span></span><br/>                                                   |
| [<span data-ttu-id="a0b63-133">**GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="a0b63-133">**GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)                           | <span data-ttu-id="a0b63-134">Récupère le mode de type pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-134">Retrieves the type mode for a soft keyboard.</span></span><br/>                                                       |
| [<span data-ttu-id="a0b63-135">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="a0b63-135">**Initialize**</span></span>](isoftkbd-initialize.md)                                                     | <span data-ttu-id="a0b63-136">Initialise tous les champs nécessaires pour un clavier logiciel et génère des dispositions de clavier conditionnel standard.</span><span class="sxs-lookup"><span data-stu-id="a0b63-136">Initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span><br/> |
| [<span data-ttu-id="a0b63-137">**SelectSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="a0b63-137">**SelectSoftKeyboard**</span></span>](isoftkbd-selectsoftkeyboard.md)                                     | <span data-ttu-id="a0b63-138">Sélectionne le clavier logiciel spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0b63-138">Selects the specified soft keyboard.</span></span><br/>                                                               |
| [<span data-ttu-id="a0b63-139">**SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="a0b63-139">**SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)                                 | <span data-ttu-id="a0b63-140">Définit le texte de l’étiquette à partir de la disposition d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-140">Sets the label text from the layout for a soft keyboard.</span></span><br/>                                           |
| [<span data-ttu-id="a0b63-141">**SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="a0b63-141">**SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)           | <span data-ttu-id="a0b63-142">Définit une combinaison d’étiquette et de texte utilisée pour décrire un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-142">Sets a combination of label and text used to describe a soft keyboard.</span></span><br/>                             |
| [<span data-ttu-id="a0b63-143">**SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="a0b63-143">**SetSoftKeyboardColors**</span></span>](isoftkbd-setsoftkeyboardcolors.md)                               | <span data-ttu-id="a0b63-144">Définit la couleur du clavier logiciel correspondant au type de couleur fourni.</span><span class="sxs-lookup"><span data-stu-id="a0b63-144">Sets the soft keyboard color corresponding to the supplied color type.</span></span><br/>                             |
| [<span data-ttu-id="a0b63-145">**SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="a0b63-145">**SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)                             | <span data-ttu-id="a0b63-146">Définit la position de départ et la taille d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-146">Sets the starting position and size of a soft keyboard.</span></span><br/>                                            |
| [<span data-ttu-id="a0b63-147">**SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="a0b63-147">**SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)                           | <span data-ttu-id="a0b63-148">Définit la police de texte utilisée par un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-148">Sets the text font used by a soft keyboard.</span></span><br/>                                                        |
| [<span data-ttu-id="a0b63-149">**SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="a0b63-149">**SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)                           | <span data-ttu-id="a0b63-150">Définit le mode de type pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-150">Sets the type mode for a soft keyboard.</span></span><br/>                                                            |
| [<span data-ttu-id="a0b63-151">**ShowKeysForKeyScanMode**</span><span class="sxs-lookup"><span data-stu-id="a0b63-151">**ShowKeysForKeyScanMode**</span></span>](isoftkbd-showkeysforkeyscanmode.md)                             | <span data-ttu-id="a0b63-152">Affiche les clés utilisées pour le mode d’analyse de clé pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-152">Displays the keys used for the key scan mode for a soft keyboard.</span></span><br/>                                  |
| [<span data-ttu-id="a0b63-153">**ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="a0b63-153">**ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)                                         | <span data-ttu-id="a0b63-154">Affiche un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-154">Displays a soft keyboard.</span></span><br/>                                                                          |
| [<span data-ttu-id="a0b63-155">**UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="a0b63-155">**UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)               | <span data-ttu-id="a0b63-156">Supprime un récepteur d’événements de clavier logiciel.</span><span class="sxs-lookup"><span data-stu-id="a0b63-156">Removes a soft keyboard event sink.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="a0b63-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0b63-157">Requirements</span></span>



| <span data-ttu-id="a0b63-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0b63-158">Requirement</span></span> | <span data-ttu-id="a0b63-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0b63-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b63-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0b63-160">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b63-161">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0b63-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a0b63-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0b63-162">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b63-163">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0b63-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0b63-164">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a0b63-164">Redistributable</span></span><br/>          | <span data-ttu-id="a0b63-165">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a0b63-165">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a0b63-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0b63-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b63-167"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-167"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a0b63-168">MIDL</span><span class="sxs-lookup"><span data-stu-id="a0b63-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0b63-169"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-169"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a0b63-170">DLL</span><span class="sxs-lookup"><span data-stu-id="a0b63-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0b63-171"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0b63-171"><dt>Softkbd.dll</dt></span></span> </dl> |



 

