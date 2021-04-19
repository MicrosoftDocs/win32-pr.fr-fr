---
title: attribut public
description: L’attribut \ public \ comprend un alias déclaré avec le mot clé typedef dans la bibliothèque de types.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- MIDL (attribut public)
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106538797"
---
# <a name="public-attribute"></a><span data-ttu-id="80517-104">attribut public</span><span class="sxs-lookup"><span data-stu-id="80517-104">public attribute</span></span>

<span data-ttu-id="80517-105">L’attribut **\[ \] public** comprend un alias déclaré avec le mot clé [**typedef**](typedef.md) dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="80517-105">The **\[public\]** attribute includes an alias declared with the [**typedef**](typedef.md) keyword in the type library.</span></span>

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a><span data-ttu-id="80517-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80517-107">*type de données*</span><span class="sxs-lookup"><span data-stu-id="80517-107">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="80517-108">Type de données pour lequel l’identificateur sera un alias.</span><span class="sxs-lookup"><span data-stu-id="80517-108">The data type that the identifier will be an alias for.</span></span>

</dd> <dt>

<span data-ttu-id="80517-109">*identifier*</span><span class="sxs-lookup"><span data-stu-id="80517-109">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="80517-110">Autre nom par lequel le *type de données* sera connu dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="80517-110">Another name by which *data-type* will be known in the software.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80517-111">Notes</span><span class="sxs-lookup"><span data-stu-id="80517-111">Remarks</span></span>

<span data-ttu-id="80517-112">Par défaut, un alias qui est déclaré avec [**typedef**](typedef.md) et n’a pas d’autres attributs est traité comme une **\# définition** et n’est pas inclus dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="80517-112">By default, an alias that is declared with [**typedef**](typedef.md) and has no other attributes is treated as a **\#define** and is not included in the type library.</span></span> <span data-ttu-id="80517-113">L’utilisation de l’attribut **\[ public \]** garantit que l’alias devient partie intégrante de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="80517-113">Using the **\[public\]** attribute ensures that the alias becomes part of the type library.</span></span>

> [!Note]  
> <span data-ttu-id="80517-114">Le compilateur MIDL requiert que vous appliquiez explicitement l’attribut **\[ public \]** à chaque typedef que vous souhaitez public.</span><span class="sxs-lookup"><span data-stu-id="80517-114">The MIDL compiler requires that you explicitly apply the **\[public\]** attribute to each typedef that you want public.</span></span>

 

## <a name="examples"></a><span data-ttu-id="80517-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="80517-115">Examples</span></span>

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a><span data-ttu-id="80517-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80517-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80517-117">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="80517-117">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="80517-118">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="80517-118">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="80517-119">**interface**</span><span class="sxs-lookup"><span data-stu-id="80517-119">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="80517-120">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="80517-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="80517-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="80517-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 