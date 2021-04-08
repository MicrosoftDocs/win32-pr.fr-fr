---
title: Afficher des boîtes de dialogue
description: Afficher des boîtes de dialogue
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player Online stores, affichage des boîtes de dialogue
- magasins en ligne, afficher des boîtes de dialogue
- types 1 magasins en ligne, affichage des boîtes de dialogue
- Windows Media Player Online stores, boîtes de dialogue
- magasins en ligne, boîtes de dialogue
- tapez 1 magasins en ligne, boîtes de dialogue
- afficher des boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723514"
---
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="a2ab7-110">Afficher des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="a2ab7-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="a2ab7-111">Le magasin en ligne peut appeler des boîtes de dialogue par le biais du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a2ab7-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="a2ab7-112">Pour ce faire, appelez [External. ShowPopup](external-showpopup.md) à partir du code de script de la page de découverte, en fournissant une valeur d’index personnalisée qui représente la boîte de dialogue à afficher.</span><span class="sxs-lookup"><span data-stu-id="a2ab7-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="a2ab7-113">Cette valeur d’index n’a de sens que dans le code de la Banque en ligne ; Le lecteur Windows Media n’interprète pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="a2ab7-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="a2ab7-114">Le lecteur Windows Media appelle ensuite [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), en passant g \_ szItemInfo \_ PopupURL pour le paramètre *bstrInfoName* et le numéro d’index pour le paramètre *pContext* .</span><span class="sxs-lookup"><span data-stu-id="a2ab7-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="a2ab7-115">Le plug-in retourne alors un **BSTR** contenant l’URL de la page Web à afficher dans la boîte de dialogue et le lecteur affiche la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a2ab7-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2ab7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2ab7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ab7-117">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="a2ab7-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




