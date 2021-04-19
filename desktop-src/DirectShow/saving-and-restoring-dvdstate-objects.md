---
description: Enregistrement et restauration d’objets DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Enregistrement et restauration d’objets DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515528"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="e671b-103">Enregistrement et restauration d’objets DvdState</span><span class="sxs-lookup"><span data-stu-id="e671b-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="e671b-104">Les objets [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permettent aux applications d’enregistrer un instantané de la session utilisateur, y compris des informations telles que l’emplacement actuel sur le disque, le niveau parental de la personne qui consulte, les flux audio et sous-image sélectionnés, etc.</span><span class="sxs-lookup"><span data-stu-id="e671b-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="e671b-105">Cela signifie que les utilisateurs peuvent enregistrer leur place sur un disque DVD-Video et les regarder ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e671b-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="e671b-106">Les applications ne peuvent pas créer d’objets DvdState.</span><span class="sxs-lookup"><span data-stu-id="e671b-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="e671b-107">Ces objets sont créés en interne par le navigateur DVD lorsqu’une application appelle [**IDvdInfo2 :: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span><span class="sxs-lookup"><span data-stu-id="e671b-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="e671b-108">Les objets DvdState exposent l’interface [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) pour permettre aux applications de demander certaines informations.</span><span class="sxs-lookup"><span data-stu-id="e671b-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="e671b-109">Dans l’exemple d’application de DVD, les fonctions **CDvdCore :: RestoreBookmark** et **CDvdCore :: SaveBookmark** montrent comment enregistrer et récupérer des objets DvdState.</span><span class="sxs-lookup"><span data-stu-id="e671b-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e671b-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e671b-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e671b-111">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="e671b-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



