---
description: Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Pointeur de fonction LPFNInitRoutine (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530961"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="a1b27-103">Pointeur de fonction LPFNInitRoutine</span><span class="sxs-lookup"><span data-stu-id="a1b27-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="a1b27-104">Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a1b27-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1b27-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="a1b27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1b27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b27-107">*bLoading*</span><span class="sxs-lookup"><span data-stu-id="a1b27-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b27-108">**True** lorsque la dll est chargée, **false** lorsque la dll est déchargée.</span><span class="sxs-lookup"><span data-stu-id="a1b27-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="a1b27-109">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="a1b27-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b27-110">Pointeur vers le CLISD de l’objet, spécifié dans la variable de membre [**CFactoryTemplate :: m \_ ClsID**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b27-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b27-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1b27-111">Return value</span></span>

<span data-ttu-id="a1b27-112">Ce pointeur de fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a1b27-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b27-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1b27-113">Requirements</span></span>



| <span data-ttu-id="a1b27-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1b27-114">Requirement</span></span> | <span data-ttu-id="a1b27-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1b27-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b27-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1b27-116">Header</span></span><br/> | <dl> <span data-ttu-id="a1b27-117"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1b27-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b27-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1b27-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b27-119">**CFactoryTemplate, classe**</span><span class="sxs-lookup"><span data-stu-id="a1b27-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




