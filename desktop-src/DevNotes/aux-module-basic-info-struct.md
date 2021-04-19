---
description: Contient des informations sur le module de base.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Structure de AUX_MODULE_BASIC_INFO (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541644"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="1ed59-103">\_Structure des \_ informations de base des modules aux \_</span><span class="sxs-lookup"><span data-stu-id="1ed59-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="1ed59-104">Contient des informations sur le module de base.</span><span class="sxs-lookup"><span data-stu-id="1ed59-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ed59-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="1ed59-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1ed59-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ed59-107">**ImageBase**</span><span class="sxs-lookup"><span data-stu-id="1ed59-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="1ed59-108">Adresse de base du module dans l’espace d’adressage du noyau.</span><span class="sxs-lookup"><span data-stu-id="1ed59-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ed59-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1ed59-109">Remarks</span></span>

<span data-ttu-id="1ed59-110">La bibliothèque d’objets qui implémente cette API peut être téléchargée à partir d' [ici](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="1ed59-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed59-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ed59-111">Requirements</span></span>



| <span data-ttu-id="1ed59-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ed59-112">Requirement</span></span> | <span data-ttu-id="1ed59-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ed59-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed59-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1ed59-114">Redistributable</span></span><br/> | <span data-ttu-id="1ed59-115">Bibliothèque d’API auxiliaires Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="1ed59-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="1ed59-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ed59-116">Header</span></span><br/>          | <dl> <span data-ttu-id="1ed59-117"><dt>Aux \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed59-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ed59-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ed59-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed59-119">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="1ed59-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




