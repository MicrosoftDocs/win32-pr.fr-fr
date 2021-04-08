---
description: La structure de la \_ ressource MXDC XPS \_ S0PAGE \_ contient des \_ informations sur une ressource, telle qu’une image ou une police, qui est associée à une page de document XPS et doit être transmise au fichier de sortie Microsoft XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Structure MXDC_XPS_S0PAGE_RESOURCE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865870"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="7cc40-103">\_Structure de \_ la \_ ressource \_ T MXDC XPS S0PAGE</span><span class="sxs-lookup"><span data-stu-id="7cc40-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="7cc40-104">La structure de la **\_ ressource MXDC XPS \_ S0PAGE \_ \_** contient des informations sur une ressource, telle qu’une image ou une police, qui est associée à une page de document XPS et doit être transmise au fichier de sortie Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="7cc40-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cc40-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="7cc40-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7cc40-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7cc40-107">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="7cc40-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="7cc40-108">Taille totale de cette structure et de la ressource à laquelle elle pointe.</span><span class="sxs-lookup"><span data-stu-id="7cc40-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="7cc40-109">**dwResourceType**</span><span class="sxs-lookup"><span data-stu-id="7cc40-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="7cc40-110">Une valeur de type [**MXDC \_ S0 \_ page \_ enums**](mxdcs0pageenums.md) indiquant le type de ressource, par exemple image TIFF ou police TrueType.</span><span class="sxs-lookup"><span data-stu-id="7cc40-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="7cc40-111">**szUri**</span><span class="sxs-lookup"><span data-stu-id="7cc40-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="7cc40-112">URI de la ressource.</span><span class="sxs-lookup"><span data-stu-id="7cc40-112">The URI of the resource.</span></span> <span data-ttu-id="7cc40-113">Ce nombre ne peut pas dépasser 260 octets.</span><span class="sxs-lookup"><span data-stu-id="7cc40-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7cc40-114">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="7cc40-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="7cc40-115">Taille de la ressource en octets.</span><span class="sxs-lookup"><span data-stu-id="7cc40-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7cc40-116">**bData**</span><span class="sxs-lookup"><span data-stu-id="7cc40-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="7cc40-117">Données de la ressource dans un tableau d’octets de taille 1 + taille de la ressource.</span><span class="sxs-lookup"><span data-stu-id="7cc40-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cc40-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7cc40-118">Remarks</span></span>

<span data-ttu-id="7cc40-119">Cette structure est ajoutée à une structure [**\_ t d' \_ en \_ -tête d’échappement MXDC**](mxdcescapeheader.md) (dont le **opcode** a la valeur **MXDCOP \_ Set \_ S0PAGERESOURCE**) pour créer une structure d' [**échappement de \_ \_ ressource \_ \_ MXDC S0PAGE**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc40-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="7cc40-120">La structure **MXDC \_ S0PAGE \_ Resource \_ Escape \_ T** qui en résulte est ensuite transmise dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc40-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="7cc40-121">L’effet est d’envoyer la ressource à MXDC pour la convertir et d’être écrite dans le fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="7cc40-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="7cc40-122">L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Toutefois, il peut y avoir plusieurs appels de ce type entre les appels à **StartPage** et **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="7cc40-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="7cc40-123">La consommation de la diffusion en continu est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ défini \_ S0PAGE \_** **opcode** de ressource pour chaque ressource sur la page avant d’appeler **ExtEscape** avec l' **opcode** **MXDCOP \_ Set \_ S0PAGE** .</span><span class="sxs-lookup"><span data-stu-id="7cc40-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cc40-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cc40-124">Requirements</span></span>



| <span data-ttu-id="7cc40-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cc40-125">Requirement</span></span> | <span data-ttu-id="7cc40-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cc40-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7cc40-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc40-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc40-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cc40-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cc40-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc40-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc40-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cc40-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7cc40-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cc40-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cc40-132"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cc40-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cc40-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cc40-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc40-134">Impression</span><span class="sxs-lookup"><span data-stu-id="7cc40-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7cc40-135">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7cc40-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="7cc40-136">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cc40-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7cc40-137">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="7cc40-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="7cc40-138">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="7cc40-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

