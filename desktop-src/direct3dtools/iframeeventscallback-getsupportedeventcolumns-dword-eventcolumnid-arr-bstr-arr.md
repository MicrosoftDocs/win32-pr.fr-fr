---
description: Obtient des informations sur les colonnes (types de données d’événement) prises en charge par la liste d’événements.
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsCallback :: GetSupportedEventColumns, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481944"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="af6ce-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback :: GetSupportedEventColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="af6ce-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="af6ce-104">Obtient des informations sur les colonnes (types de données d’événement) prises en charge par la liste d’événements.</span><span class="sxs-lookup"><span data-stu-id="af6ce-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6ce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af6ce-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="af6ce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af6ce-106">Parameters</span></span>

<span data-ttu-id="af6ce-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="af6ce-107">*numColumns* </span></span>  
<span data-ttu-id="af6ce-108">Nombre de colonnes prises en charge par</span><span class="sxs-lookup"><span data-stu-id="af6ce-108">The number of columns supported by</span></span>

<span data-ttu-id="af6ce-109">*count0 \_ PID* </span><span class="sxs-lookup"><span data-stu-id="af6ce-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="af6ce-110">ID de chaque colonne prise en charge par la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="af6ce-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="af6ce-111">*count0 \_ pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="af6ce-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="af6ce-112">Noms de chaque colonne, sous la forme d’une chaîne COM, pris en charge par la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="af6ce-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="af6ce-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af6ce-113">Return value</span></span>

<span data-ttu-id="af6ce-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="af6ce-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af6ce-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af6ce-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6ce-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af6ce-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="af6ce-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="af6ce-117">Header</span></span></p></td><td><span data-ttu-id="af6ce-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="af6ce-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="af6ce-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af6ce-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="af6ce-120">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="af6ce-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
