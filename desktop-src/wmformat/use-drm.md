---
title: Use_DRM
description: L’attribut utiliser la \_ gestion des droits numériques (DRM) demande à l’objet enregistreur d’appliquer la protection DRM version 1 au fichier actuel.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Format Windows Media Use_DRM
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507783"
---
# <a name="use_drm"></a><span data-ttu-id="02e5c-104">Utiliser \_ DRM</span><span class="sxs-lookup"><span data-stu-id="02e5c-104">Use\_DRM</span></span>

<span data-ttu-id="02e5c-105">L’attribut utiliser la gestion des **\_ droits numériques (DRM** ) demande à l’objet enregistreur d’appliquer la protection DRM version 1 au fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="02e5c-105">The **Use\_DRM** attribute instructs the writer object to apply DRM version 1 protection to the current file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="02e5c-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="02e5c-106">Global Constant</span></span>

<span data-ttu-id="02e5c-107">g \_ wszWMUse \_ DRM</span><span class="sxs-lookup"><span data-stu-id="02e5c-107">g\_wszWMUse\_DRM</span></span>

## <a name="data-type"></a><span data-ttu-id="02e5c-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="02e5c-108">Data Type</span></span>

<span data-ttu-id="02e5c-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="02e5c-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="02e5c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="02e5c-110">Remarks</span></span>

<span data-ttu-id="02e5c-111">Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour affecter à cette propriété la **valeur true** lors de la création du contenu DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="02e5c-111">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property to **TRUE** when creating DRM version 1 content.</span></span> <span data-ttu-id="02e5c-112">Cette propriété n’est pas accessible à partir de l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="02e5c-112">This property is not accessible from the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="02e5c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02e5c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e5c-114">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="02e5c-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




