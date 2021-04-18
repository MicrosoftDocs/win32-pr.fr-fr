---
description: Contient des informations sur les modules étendus.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Structure de AUX_MODULE_EXTENDED_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540636"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="0d65f-103">\_Structure des \_ informations étendues du module aux \_</span><span class="sxs-lookup"><span data-stu-id="0d65f-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="0d65f-104">Contient des informations sur les modules étendus.</span><span class="sxs-lookup"><span data-stu-id="0d65f-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d65f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d65f-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="0d65f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0d65f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d65f-107">**BasicInfo**</span><span class="sxs-lookup"><span data-stu-id="0d65f-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0d65f-108">Structure [**des \_ \_ \_ informations de base des modules**](aux-module-basic-info-struct.md) aux.</span><span class="sxs-lookup"><span data-stu-id="0d65f-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0d65f-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="0d65f-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="0d65f-110">Taille, en octets, du module chargé.</span><span class="sxs-lookup"><span data-stu-id="0d65f-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="0d65f-111">**FileNameOffset**</span><span class="sxs-lookup"><span data-stu-id="0d65f-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0d65f-112">Offset du nom de fichier dans la mémoire tampon **FullPathName** .</span><span class="sxs-lookup"><span data-stu-id="0d65f-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0d65f-113">**FullPathName**</span><span class="sxs-lookup"><span data-stu-id="0d65f-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="0d65f-114">Chemin d’accès complet du module.</span><span class="sxs-lookup"><span data-stu-id="0d65f-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d65f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0d65f-115">Remarks</span></span>

<span data-ttu-id="0d65f-116">La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="0d65f-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d65f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d65f-117">Requirements</span></span>



| <span data-ttu-id="0d65f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d65f-118">Requirement</span></span> | <span data-ttu-id="0d65f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d65f-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d65f-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0d65f-120">Redistributable</span></span><br/> | <span data-ttu-id="0d65f-121">Bibliothèque d’API auxiliaires Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="0d65f-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="0d65f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d65f-122">Header</span></span><br/>          | <dl> <span data-ttu-id="0d65f-123"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d65f-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d65f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d65f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d65f-125">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="0d65f-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="0d65f-126">**\_informations de \_ base du module aux \_**</span><span class="sxs-lookup"><span data-stu-id="0d65f-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




