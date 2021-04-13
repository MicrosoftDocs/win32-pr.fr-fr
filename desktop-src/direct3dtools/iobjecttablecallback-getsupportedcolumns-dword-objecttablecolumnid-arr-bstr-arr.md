---
description: Obtient des informations sur les colonnes (types de données d’objet) prises en charge par la table des objets.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableCallback :: GetSupportedColumns, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ed077e0921043245e4ff3dda4b1c33dd4e3f20d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481273"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span data-ttu-id="f1b4a-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback :: GetSupportedColumns, méthode</span><span class="sxs-lookup"><span data-stu-id="f1b4a-103"><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns method</span></span>

<span data-ttu-id="f1b4a-104">Obtient des informations sur les colonnes (types de données d’objet) prises en charge par la table des objets.</span><span class="sxs-lookup"><span data-stu-id="f1b4a-104">Gets information about which columns (types of object data) are supported by the object table.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b4a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1b4a-105">Syntax</span></span>


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="f1b4a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1b4a-106">Parameters</span></span>

<span data-ttu-id="f1b4a-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="f1b4a-107">*numColumns* </span></span>  
<span data-ttu-id="f1b4a-108">Nombre de colonnes prises en charge par la table des objets.</span><span class="sxs-lookup"><span data-stu-id="f1b4a-108">The number of columns supported by the object table.</span></span>

<span data-ttu-id="f1b4a-109">*count0_pIDs* </span><span class="sxs-lookup"><span data-stu-id="f1b4a-109">*count0_pIDs* </span></span>  
<span data-ttu-id="f1b4a-110">ID de chaque colonne prise en charge par la table des objets.</span><span class="sxs-lookup"><span data-stu-id="f1b4a-110">The IDs of each column supported by the object table.</span></span>

<span data-ttu-id="f1b4a-111">*count0_pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="f1b4a-111">*count0_pBstrNames* </span></span>  
<span data-ttu-id="f1b4a-112">Noms de chaque colonne, sous la forme d’une chaîne COM, pris en charge par la table des objets.</span><span class="sxs-lookup"><span data-stu-id="f1b4a-112">The names of each column, as a COM string, supported by the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="f1b4a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1b4a-113">Return value</span></span>

<span data-ttu-id="f1b4a-114">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f1b4a-114">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f1b4a-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1b4a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b4a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1b4a-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f1b4a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1b4a-117">Header</span></span></p></td><td><span data-ttu-id="f1b4a-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f1b4a-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f1b4a-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1b4a-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f1b4a-120">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="f1b4a-120">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
