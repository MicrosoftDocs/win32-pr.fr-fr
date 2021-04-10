---
title: WM/EncodingTime
description: L’attribut WM/EncodingTime contient un horodatage de l’heure à laquelle le contenu a été encodé.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Format Windows Media WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030425"
---
# <a name="wmencodingtime"></a><span data-ttu-id="c9dad-104">WM/EncodingTime</span><span class="sxs-lookup"><span data-stu-id="c9dad-104">WM/EncodingTime</span></span>

<span data-ttu-id="c9dad-105">L’attribut **WM/EncodingTime** contient un horodatage de l’heure à laquelle le contenu a été encodé.</span><span class="sxs-lookup"><span data-stu-id="c9dad-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c9dad-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="c9dad-106">Global Constant</span></span>

<span data-ttu-id="c9dad-107">\_wszWMEncodingTime g</span><span class="sxs-lookup"><span data-stu-id="c9dad-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="c9dad-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="c9dad-108">Data Type</span></span>

<span data-ttu-id="c9dad-109">**fileTime** (**\_ type WMT \_ QWord**)</span><span class="sxs-lookup"><span data-stu-id="c9dad-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="c9dad-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c9dad-110">Remarks</span></span>

<span data-ttu-id="c9dad-111">Cet attribut utilise une valeur FILETIME, qui est une valeur 64 bits représentant le nombre d’unités de temps de 100 nanosecondes écoulées depuis le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="c9dad-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="c9dad-112">Pour plus d’informations sur FILETIME, consultez la section informations système Windows du kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="c9dad-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="c9dad-113">Il ne s’agit pas d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="c9dad-113">This is not a coded attribute.</span></span> <span data-ttu-id="c9dad-114">Vous devez la définir manuellement si vous souhaitez l’inclure dans vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="c9dad-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9dad-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9dad-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9dad-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="c9dad-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




