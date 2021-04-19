---
title: Constantes PICTYPE (OleCtl. h)
description: Décrivez le type d’un objet Picture tel qu’il est retourné par le type d’extraction IPicture, ainsi que \_ pour décrire le type d’image dans le membre picType de la structure PICTDESC transmise à OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511550"
---
# <a name="pictype-constants"></a><span data-ttu-id="25ca8-103">Constantes PICTYPE</span><span class="sxs-lookup"><span data-stu-id="25ca8-103">PICTYPE Constants</span></span>

<span data-ttu-id="25ca8-104">Décrit le type d’un objet image tel qu’il est retourné par [**IPicture :: obtenir le \_ type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), ainsi que pour décrire le type d’image dans le membre **PicType** de la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) qui est passée à [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="25ca8-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="25ca8-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="25ca8-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="25ca8-106">Description</span><span class="sxs-lookup"><span data-stu-id="25ca8-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="25ca8-107"><dt>**PICTYPE \_ Non initialisé**</dt> <dt>(-1)</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="25ca8-108">L’objet image n’est pas actuellement initialisé.</span><span class="sxs-lookup"><span data-stu-id="25ca8-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="25ca8-109">Cette valeur est valide uniquement en tant que valeur de retour du [**\_ type ipicture :: obtenir**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) et n’est pas valide avec la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="25ca8-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="25ca8-110"><dt>**PICTYPE \_ AUCUN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="25ca8-111">Un nouvel objet Picture doit être créé sans l’État Initialized.</span><span class="sxs-lookup"><span data-stu-id="25ca8-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="25ca8-112">Cette valeur est valide uniquement dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="25ca8-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="25ca8-113"><dt>**PICTYPE \_ BITMAP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="25ca8-114">Le type Picture est un bitmap.</span><span class="sxs-lookup"><span data-stu-id="25ca8-114">The picture type is a bitmap.</span></span> <span data-ttu-id="25ca8-115">Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ **BMP** de cette structure contient les paramètres d’initialisation appropriés.</span><span class="sxs-lookup"><span data-stu-id="25ca8-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="25ca8-116"><dt>**PICTYPE \_ MÉTAFICHIER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="25ca8-117">Le type Picture est un métafichier.</span><span class="sxs-lookup"><span data-stu-id="25ca8-117">The picture type is a metafile.</span></span> <span data-ttu-id="25ca8-118">Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ **WMF** de cette structure contient les paramètres d’initialisation appropriés.</span><span class="sxs-lookup"><span data-stu-id="25ca8-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="25ca8-119"><dt>**PICTYPE \_ ICÔNE**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="25ca8-120">Le type d’image est une icône.</span><span class="sxs-lookup"><span data-stu-id="25ca8-120">The picture type is an icon.</span></span> <span data-ttu-id="25ca8-121">Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ d' **icône** de cette structure contient les paramètres d’initialisation appropriés.</span><span class="sxs-lookup"><span data-stu-id="25ca8-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="25ca8-122"><dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="25ca8-123">Le type Picture est un métafichier amélioré.</span><span class="sxs-lookup"><span data-stu-id="25ca8-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="25ca8-124">Lorsque cette valeur apparaît dans la structure [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , cela signifie que le champ **EMF** de cette structure contient les paramètres d’initialisation appropriés.</span><span class="sxs-lookup"><span data-stu-id="25ca8-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="25ca8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25ca8-125">Requirements</span></span>



| <span data-ttu-id="25ca8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25ca8-126">Requirement</span></span> | <span data-ttu-id="25ca8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="25ca8-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25ca8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ca8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="25ca8-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25ca8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25ca8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25ca8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="25ca8-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25ca8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25ca8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="25ca8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ca8-133"><dt>OleCtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ca8-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25ca8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25ca8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ca8-135">**IPicture :: obten, \_ type**</span><span class="sxs-lookup"><span data-stu-id="25ca8-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="25ca8-136">**OleCreatePictureIndirect**</span><span class="sxs-lookup"><span data-stu-id="25ca8-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="25ca8-137">**PICTDESC**</span><span class="sxs-lookup"><span data-stu-id="25ca8-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





