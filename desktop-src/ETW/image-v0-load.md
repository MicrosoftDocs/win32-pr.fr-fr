---
description: Cette classe est la classe de type d’événement pour les événements de chargement d’image. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Classe Image_V0_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971934"
---
# <a name="image_v0_load-class"></a><span data-ttu-id="a8ccf-104">Classe de charge d’image \_ v0 \_</span><span class="sxs-lookup"><span data-stu-id="a8ccf-104">Image\_V0\_Load class</span></span>

<span data-ttu-id="a8ccf-105">Cette classe est la classe de type d’événement pour les événements de chargement d’image.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-105">This class is the event type class for image load events.</span></span>

<span data-ttu-id="a8ccf-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ccf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8ccf-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="a8ccf-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a8ccf-108">Members</span></span>

<span data-ttu-id="a8ccf-109">La **classe \_ \_ Load de l’image v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a8ccf-109">The **Image\_V0\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="a8ccf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a8ccf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8ccf-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a8ccf-111">Properties</span></span>

<span data-ttu-id="a8ccf-112">La classe de **\_ \_ chargement image v0** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-112">The **Image\_V0\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8ccf-113">BaseAddress</span><span class="sxs-lookup"><span data-stu-id="a8ccf-113">BaseAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8ccf-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8ccf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8ccf-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a8ccf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8ccf-116">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="a8ccf-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a8ccf-117">Adresse de base de l’application dans laquelle l’image est chargée.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-117">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a8ccf-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="a8ccf-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8ccf-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a8ccf-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8ccf-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a8ccf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8ccf-121">Qualificateurs : WmiDataId (3), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="a8ccf-121">Qualifiers: WmiDataId(3), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a8ccf-122">Nom de fichier et extension de la DLL ou de l’image exécutable à charger.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-122">File name and extension of the DLL or executable image to load.</span></span>

</dd> <dt>

<span data-ttu-id="a8ccf-123">Module</span><span class="sxs-lookup"><span data-stu-id="a8ccf-123">ModuleSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8ccf-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8ccf-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8ccf-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a8ccf-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8ccf-126">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a8ccf-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a8ccf-127">Taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="a8ccf-127">Size of the image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8ccf-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a8ccf-128">Requirements</span></span>



| <span data-ttu-id="a8ccf-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8ccf-129">Requirement</span></span> | <span data-ttu-id="a8ccf-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8ccf-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a8ccf-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8ccf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ccf-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8ccf-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a8ccf-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8ccf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ccf-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8ccf-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a8ccf-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8ccf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ccf-136">**Image \_ v0**</span><span class="sxs-lookup"><span data-stu-id="a8ccf-136">**Image\_V0**</span></span>](image-v0.md)
</dt> </dl>

 

 




