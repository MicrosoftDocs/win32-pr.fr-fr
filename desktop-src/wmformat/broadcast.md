---
title: Diffusion
description: L’attribut Broadcast est un attribut de niveau fichier qui indique si le contenu peut être diffusé. Il est supposé que tout contenu pour lequel aucun copyright n’a été attribué peut être légalement diffusé.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Diffuser le format Windows Media
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf9e7d94682f8dbf08850f87954a934fd909afe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511867"
---
# <a name="broadcast"></a><span data-ttu-id="7b406-105">Diffusion</span><span class="sxs-lookup"><span data-stu-id="7b406-105">Broadcast</span></span>

<span data-ttu-id="7b406-106">L’attribut **Broadcast** est un attribut de niveau fichier qui indique si le contenu peut être diffusé.</span><span class="sxs-lookup"><span data-stu-id="7b406-106">The **Broadcast** attribute is a file-level attribute indicating whether the content can be broadcast.</span></span> <span data-ttu-id="7b406-107">Il est supposé que tout contenu pour lequel aucun copyright n’a été attribué peut être légalement diffusé.</span><span class="sxs-lookup"><span data-stu-id="7b406-107">It is assumed that any content for which no copyright has been assigned can be legally broadcast.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7b406-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="7b406-108">Global Constant</span></span>

<span data-ttu-id="7b406-109">\_wszWMBroadcast g</span><span class="sxs-lookup"><span data-stu-id="7b406-109">g\_wszWMBroadcast</span></span>

## <a name="data-type"></a><span data-ttu-id="7b406-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="7b406-110">Data Type</span></span>

<span data-ttu-id="7b406-111">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7b406-111">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b406-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7b406-112">Remarks</span></span>

<span data-ttu-id="7b406-113">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="7b406-113">This is a coded attribute.</span></span>

<span data-ttu-id="7b406-114">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="7b406-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="7b406-115">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7b406-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b406-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b406-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b406-117">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="7b406-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




