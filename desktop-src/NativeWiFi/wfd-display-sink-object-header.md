---
description: Décrit les données de l’objet récepteur d’affichage incluses dans une notification ou un résultat de notification.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: Structure WFD_DISPLAY_SINK_OBJECT_HEADER (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864809"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="5280f-103">\_Structure d' \_ \_ \_ en-tête d’objet récepteur WFD</span><span class="sxs-lookup"><span data-stu-id="5280f-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="5280f-104">La structure d' **\_ \_ \_ \_ en-tête d’objet du récepteur d’affichage WFD** décrit les données de l’objet récepteur d’affichage incluses dans une notification ou un résultat de notification.</span><span class="sxs-lookup"><span data-stu-id="5280f-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="5280f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5280f-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="5280f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5280f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5280f-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="5280f-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="5280f-108">Type de l’objet récepteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5280f-108">The type of the display sink object.</span></span> <span data-ttu-id="5280f-109">Vous pouvez utiliser le type d' **objet récepteur d’affichage WFD identifiant le \_ \_ \_ \_ \_ paramètre par défaut** , qui est défini comme valeur 1.</span><span class="sxs-lookup"><span data-stu-id="5280f-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="5280f-110">**Faisant**</span><span class="sxs-lookup"><span data-stu-id="5280f-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="5280f-111">Version de révision de l’objet récepteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5280f-111">The revision version of the display sink object.</span></span> <span data-ttu-id="5280f-112">Vous pouvez utiliser la révision de l’objet récepteur de l’identificateur **WFD, \_ \_ \_ \_ \_ version \_ 1** , qui est définie comme valeur 1.</span><span class="sxs-lookup"><span data-stu-id="5280f-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="5280f-113">**Durée**</span><span class="sxs-lookup"><span data-stu-id="5280f-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="5280f-114">Longueur des données dans la notification ou le résultat de la notification.</span><span class="sxs-lookup"><span data-stu-id="5280f-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5280f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5280f-115">Requirements</span></span>



| <span data-ttu-id="5280f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5280f-116">Requirement</span></span> | <span data-ttu-id="5280f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5280f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5280f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5280f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5280f-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5280f-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5280f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5280f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5280f-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5280f-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5280f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5280f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5280f-123"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="5280f-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




