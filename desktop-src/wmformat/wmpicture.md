---
title: WM/image
description: L’attribut WM/Picture contient une image associée au contenu.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Format Windows Media WM/Picture
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940442"
---
# <a name="wmpicture"></a><span data-ttu-id="76028-104">WM/image</span><span class="sxs-lookup"><span data-stu-id="76028-104">WM/Picture</span></span>

<span data-ttu-id="76028-105">L’attribut **WM/Picture** contient une image associée au contenu.</span><span class="sxs-lookup"><span data-stu-id="76028-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="76028-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="76028-106">Global Constant</span></span>

<span data-ttu-id="76028-107">\_wszWMPicture g</span><span class="sxs-lookup"><span data-stu-id="76028-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="76028-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="76028-108">Data Type</span></span>

<span data-ttu-id="76028-109">[**WM \_ IMAGE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ type de type WMT \_ binaire**)</span><span class="sxs-lookup"><span data-stu-id="76028-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="76028-110">Notes</span><span class="sxs-lookup"><span data-stu-id="76028-110">Remarks</span></span>

<span data-ttu-id="76028-111">Cet attribut est compatible avec le frame ID3, APIC.</span><span class="sxs-lookup"><span data-stu-id="76028-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="76028-112">La spécification ID3 du frame APIC stipule que, bien qu’il puisse y avoir un nombre quelconque d’images APIC associées à un fichier, une seule peut être de type 1 et une seule peut être de type 2.</span><span class="sxs-lookup"><span data-stu-id="76028-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="76028-113">La spécification stipule également que la description de l’image ne peut pas dépasser 64 caractères, mais peut être vide.</span><span class="sxs-lookup"><span data-stu-id="76028-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="76028-114">Les attributs WM/Picture ajoutés avec les objets du kit de développement logiciel (SDK) du format Windows Media ne sont pas validés automatiquement pour être conformes aux spécifications ID3.</span><span class="sxs-lookup"><span data-stu-id="76028-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="76028-115">Vous devez ajouter du code dans votre application pour effectuer les validations si vous souhaitez assurer une compatibilité complète avec ID3.</span><span class="sxs-lookup"><span data-stu-id="76028-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="76028-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76028-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76028-117">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="76028-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="76028-118">**\_image WM**</span><span class="sxs-lookup"><span data-stu-id="76028-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




