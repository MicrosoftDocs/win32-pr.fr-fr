---
title: Identifiable
description: L’attribut recherché est un attribut de niveau fichier qui spécifie si une application peut rechercher des points dans le contenu.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Format Windows Media recherché
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314498"
---
# <a name="seekable"></a><span data-ttu-id="a5e68-104">Identifiable</span><span class="sxs-lookup"><span data-stu-id="a5e68-104">Seekable</span></span>

<span data-ttu-id="a5e68-105">L’attribut **recherché** est un attribut de niveau fichier qui spécifie si une application peut rechercher des points dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="a5e68-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a5e68-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="a5e68-106">Global Constant</span></span>

<span data-ttu-id="a5e68-107">\_wszWMSeekable g</span><span class="sxs-lookup"><span data-stu-id="a5e68-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="a5e68-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="a5e68-108">Data Type</span></span>

<span data-ttu-id="a5e68-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a5e68-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e68-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a5e68-110">Remarks</span></span>

<span data-ttu-id="a5e68-111">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="a5e68-111">This is a coded attribute.</span></span>

<span data-ttu-id="a5e68-112">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="a5e68-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="a5e68-113">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a5e68-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="a5e68-114">La valeur de cet attribut pour un fichier peut varier en fonction de l’objet qui expose l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) ou [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilisée pour la récupérer.</span><span class="sxs-lookup"><span data-stu-id="a5e68-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="a5e68-115">Cela est dû au fait que les objets de lecteur (à la fois synchrones et asynchrones) effectuent une vérification plus approfondie que l’objet de l’éditeur de métadonnées, pour déterminer si vous pouvez rechercher un point dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="a5e68-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="a5e68-116">La valeur d’attribut **recherchée** retournée par un objet lecteur est plus précise.</span><span class="sxs-lookup"><span data-stu-id="a5e68-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5e68-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5e68-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e68-118">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="a5e68-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




