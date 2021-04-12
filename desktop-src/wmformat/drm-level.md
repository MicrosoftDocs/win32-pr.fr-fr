---
title: DRM_Level
description: '\_Le niveau DRM est un attribut de licence défini par le kit de développement logiciel (SDK) du format Windows Media lorsqu’il crée une licence locale pour les fichiers protégés par la gestion des droits numériques (DRM) 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- Format Windows Media DRM_Level
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314348"
---
# <a name="drm_level"></a><span data-ttu-id="1e519-104">\_Niveau DRM</span><span class="sxs-lookup"><span data-stu-id="1e519-104">DRM\_Level</span></span>

<span data-ttu-id="1e519-105">**DRM \_ Le niveau** est un attribut de licence défini par le kit de développement logiciel (SDK) Windows Media format lors de la création d’une licence locale pour les fichiers protégés avec la version 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="1e519-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="1e519-106">Il contient le niveau de sécurité que l’application appelante doit avoir pour accéder au contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="1e519-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="1e519-107">La valeur par défaut est 150.</span><span class="sxs-lookup"><span data-stu-id="1e519-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1e519-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="1e519-108">Global Constant</span></span>

<span data-ttu-id="1e519-109">\_niveau de wszWMDRM g \_</span><span class="sxs-lookup"><span data-stu-id="1e519-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="1e519-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="1e519-110">Data Type</span></span>

<span data-ttu-id="1e519-111">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1e519-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="1e519-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1e519-112">Remarks</span></span>

<span data-ttu-id="1e519-113">Le niveau de sécurité DRM d’une application est déterminé par la bibliothèque wmstubdrm particulière à laquelle il est lié au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="1e519-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="1e519-114">Pour plus d’informations sur ces niveaux de sécurité, consultez [obtention de la bibliothèque DRM requise](obtaining-the-required-drm-library.md).</span><span class="sxs-lookup"><span data-stu-id="1e519-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="1e519-115">Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour définir cette propriété lors de la protection des fichiers ASF avec la version 1 de DRM.</span><span class="sxs-lookup"><span data-stu-id="1e519-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e519-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e519-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e519-117">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="1e519-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




