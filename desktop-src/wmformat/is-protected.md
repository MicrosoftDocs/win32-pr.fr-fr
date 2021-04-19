---
title: Is_Protected
description: L' \_ attribut is protected est un attribut de niveau fichier qui spécifie si le contenu du fichier a été protégé à l’aide de la gestion des droits numériques (DRM).
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Format Windows Media Is_Protected
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511272"
---
# <a name="is_protected"></a><span data-ttu-id="f9f43-104">Est \_ protégé</span><span class="sxs-lookup"><span data-stu-id="f9f43-104">Is\_Protected</span></span>

<span data-ttu-id="f9f43-105">L’attribut **is \_ protected** est un attribut de niveau fichier qui spécifie si le contenu du fichier a été protégé à l’aide de la gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="f9f43-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="f9f43-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="f9f43-106">Global Constant</span></span>

<span data-ttu-id="f9f43-107">\_wszWMProtected g</span><span class="sxs-lookup"><span data-stu-id="f9f43-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="f9f43-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9f43-108">Data Type</span></span>

<span data-ttu-id="f9f43-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f9f43-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="f9f43-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f9f43-110">Remarks</span></span>

<span data-ttu-id="f9f43-111">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="f9f43-111">This is a coded attribute.</span></span> <span data-ttu-id="f9f43-112">La récupération de cette propriété fournit les mêmes informations que l’appel de [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span><span class="sxs-lookup"><span data-stu-id="f9f43-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="f9f43-113">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="f9f43-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="f9f43-114">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9f43-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9f43-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9f43-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f43-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="f9f43-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




