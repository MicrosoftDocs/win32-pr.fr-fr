---
title: WM/StreamTypeInfo
description: L’attribut WM/StreamTypeInfo contient les informations de configuration du flux spécifié dans le fichier ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Format Windows Media WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380694"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="1e710-104">WM/StreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="1e710-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="1e710-105">L’attribut **WM/StreamTypeInfo** contient les informations de configuration du flux spécifié dans le fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="1e710-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1e710-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="1e710-106">Global Constant</span></span>

<span data-ttu-id="1e710-107">\_wszWMStreamTypeInfo g</span><span class="sxs-lookup"><span data-stu-id="1e710-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="1e710-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="1e710-108">Data Type</span></span>

<span data-ttu-id="1e710-109">[**WM \_ \_ \_ informations sur le type de flux**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ type WMT \_ binaire**)</span><span class="sxs-lookup"><span data-stu-id="1e710-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="1e710-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1e710-110">Remarks</span></span>

<span data-ttu-id="1e710-111">Cet attribut s’applique à des flux spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1e710-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="1e710-112">Vous ne pouvez pas récupérer cet attribut pour le flux 0.</span><span class="sxs-lookup"><span data-stu-id="1e710-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="1e710-113">Cet attribut est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1e710-113">This attribute is read-only.</span></span>

<span data-ttu-id="1e710-114">L’objet de l’éditeur de métadonnées peut accéder à **WM/StreamTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="1e710-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="1e710-115">Il s’agit de la seule façon d’accéder aux informations de configuration de flux sans ouvrir le fichier avec l’objet lecteur (ou l’objet lecteur synchrone).</span><span class="sxs-lookup"><span data-stu-id="1e710-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="1e710-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e710-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e710-117">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="1e710-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




