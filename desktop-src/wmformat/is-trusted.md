---
title: Is_Trusted
description: L' \_ attribut is Trusted est un attribut de niveau fichier qui spécifie si l’URL d’acquisition de licence dans le fichier est approuvée.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Format Windows Media Is_Trusted
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940512"
---
# <a name="is_trusted"></a><span data-ttu-id="06480-104">Est \_ approuvé</span><span class="sxs-lookup"><span data-stu-id="06480-104">Is\_Trusted</span></span>

<span data-ttu-id="06480-105">L’attribut **is \_ Trusted** est un attribut de niveau fichier qui spécifie si l’URL d’acquisition de licence dans le fichier est approuvée.</span><span class="sxs-lookup"><span data-stu-id="06480-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="06480-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="06480-106">Global Constant</span></span>

<span data-ttu-id="06480-107">\_wszWMTrusted g</span><span class="sxs-lookup"><span data-stu-id="06480-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="06480-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="06480-108">Data Type</span></span>

<span data-ttu-id="06480-109">**\_type WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="06480-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="06480-110">Notes</span><span class="sxs-lookup"><span data-stu-id="06480-110">Remarks</span></span>

<span data-ttu-id="06480-111">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="06480-111">This is a coded attribute.</span></span>

<span data-ttu-id="06480-112">Avant de naviguer vers une URL d’acquisition de licence contenue dans un fichier protégé par DRM, une application doit d’abord vérifier que cette propriété a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="06480-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="06480-113">Si la valeur est false, l’application doit avertir l’utilisateur que l’URL a peut-être été falsifiée.</span><span class="sxs-lookup"><span data-stu-id="06480-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="06480-114">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="06480-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="06480-115">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06480-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="06480-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06480-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06480-117">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="06480-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




