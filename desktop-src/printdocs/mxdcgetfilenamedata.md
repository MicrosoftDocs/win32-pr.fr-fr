---
description: La \_ structure MXDC \_ obtenir \_ \_ des données de nom de fichier contient le chemin d’accès complet et le nom de fichier d’un fichier de sortie Microsoft XPS Document Converter (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Structure MXDC_GET_FILENAME_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864962"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="5833e-103">MXDC de l’accès à la \_ \_ structure des données de nom de fichier \_ \_</span><span class="sxs-lookup"><span data-stu-id="5833e-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="5833e-104">La structure **MXDC \_ obtenir des \_ \_ données de \_ nom** de fichier contient le chemin d’accès complet et le nom de fichier d’un fichier de sortie Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="5833e-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5833e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5833e-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="5833e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5833e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5833e-107">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="5833e-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="5833e-108">Taille de la mémoire tampon de sortie, **wszData**.</span><span class="sxs-lookup"><span data-stu-id="5833e-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="5833e-109">**wszData**</span><span class="sxs-lookup"><span data-stu-id="5833e-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="5833e-110">Chemin d’accès complet et nom de fichier du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="5833e-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5833e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5833e-111">Remarks</span></span>

<span data-ttu-id="5833e-112">Cette structure est retournée par [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) lorsqu’elle est appelée avec l’échappement d’échappement [**MXDC \_**](mxdc-escape.md) et que la structure [**\_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) qui est passée dans le paramètre *lpszInData* a son **opcode** défini sur **MXDCOP recevoir le \_ nom de \_ fichier**.</span><span class="sxs-lookup"><span data-stu-id="5833e-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5833e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5833e-113">Requirements</span></span>



| <span data-ttu-id="5833e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5833e-114">Requirement</span></span> | <span data-ttu-id="5833e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5833e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5833e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5833e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5833e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5833e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5833e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5833e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5833e-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5833e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5833e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5833e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5833e-121"><dt>Mxdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="5833e-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5833e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5833e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5833e-123">Impression</span><span class="sxs-lookup"><span data-stu-id="5833e-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5833e-124">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="5833e-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="5833e-125">[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5833e-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5833e-126">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="5833e-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="5833e-127">**MXDC \_ échappement**</span><span class="sxs-lookup"><span data-stu-id="5833e-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

