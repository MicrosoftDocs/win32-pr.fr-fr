---
description: Enregistre les données du filtre dans le flux donné.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: CPersistStream. Save, méthode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526727"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="7f1b3-103">CPersistStream. Save, méthode</span><span class="sxs-lookup"><span data-stu-id="7f1b3-103">CPersistStream.Save method</span></span>

<span data-ttu-id="7f1b3-104">Enregistre les données du filtre dans le flux donné.</span><span class="sxs-lookup"><span data-stu-id="7f1b3-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f1b3-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="7f1b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f1b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f1b3-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="7f1b3-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="7f1b3-108">Pointeur vers le flux vers lequel les données doivent être enregistrées.</span><span class="sxs-lookup"><span data-stu-id="7f1b3-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="7f1b3-109">*fClearDirty*</span><span class="sxs-lookup"><span data-stu-id="7f1b3-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="7f1b3-110">Indicateur qui spécifie s’il faut réinitialiser l’indicateur de modification du flux actuel. **True** signifie qu’il doit être réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="7f1b3-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="7f1b3-111">(Lorsque la méthode est appelée dans le cadre d’une opération d’enregistrement, la valeur est généralement **true**; quand elle est appelée dans le cadre d’une opération Enregistrer sous, la valeur est généralement **false**.)</span><span class="sxs-lookup"><span data-stu-id="7f1b3-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f1b3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f1b3-112">Return value</span></span>

<span data-ttu-id="7f1b3-113">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f1b3-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f1b3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7f1b3-114">Remarks</span></span>

<span data-ttu-id="7f1b3-115">Cette fonction membre implémente la méthode **IPersistStream :: Save** .</span><span class="sxs-lookup"><span data-stu-id="7f1b3-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="7f1b3-116">Il appelle **writeInt** avec la version logicielle, appelle [**CPersistStream :: WriteToStream**](cpersiststream-writetostream.md) avec le flux dans *pstm*, puis réinitialise **mPS \_ fDirty**.</span><span class="sxs-lookup"><span data-stu-id="7f1b3-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f1b3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f1b3-117">Requirements</span></span>



| <span data-ttu-id="7f1b3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f1b3-118">Requirement</span></span> | <span data-ttu-id="7f1b3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f1b3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f1b3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f1b3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7f1b3-121"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b3-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f1b3-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f1b3-122">Library</span></span><br/> | <dl> <span data-ttu-id="7f1b3-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f1b3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f1b3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f1b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1b3-125">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="7f1b3-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




