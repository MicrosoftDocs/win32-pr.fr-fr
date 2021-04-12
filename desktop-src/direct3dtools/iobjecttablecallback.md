---
description: Rappel pour retourner les données de la table d’objets.
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IObjectTableCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109870"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="aca35-103"><span id="vspixengine.iobjecttablecallback"></span>Interface IObjectTableCallback</span><span class="sxs-lookup"><span data-stu-id="aca35-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="aca35-104">Rappel pour retourner les données de la table d’objets.</span><span class="sxs-lookup"><span data-stu-id="aca35-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="aca35-105">Membres</span><span class="sxs-lookup"><span data-stu-id="aca35-105">Members</span></span>

<span data-ttu-id="aca35-106">L’interface **IObjectTableCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aca35-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aca35-107">**IObjectTableCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aca35-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="aca35-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aca35-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="aca35-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="aca35-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="aca35-110">L’interface **IObjectTableCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="aca35-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="aca35-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="aca35-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="aca35-112">Description</span><span class="sxs-lookup"><span data-stu-id="aca35-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="aca35-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="aca35-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aca35-114">Obtient des informations sur les colonnes (types de données d’objet) prises en charge par la table des objets.</span><span class="sxs-lookup"><span data-stu-id="aca35-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="aca35-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="aca35-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="aca35-116">Fonction de rappel utilisée pour informer l’hôte des informations de la table objet.</span><span class="sxs-lookup"><span data-stu-id="aca35-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="aca35-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aca35-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aca35-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="aca35-118">Header</span></span></p></td><td><span data-ttu-id="aca35-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aca35-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
