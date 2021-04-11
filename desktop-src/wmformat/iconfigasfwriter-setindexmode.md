---
title: Méthode IConfigAsfWriter SetIndexMode
description: La méthode SetIndexMode permet à l’application de contrôler si le fichier sera indexé temporellement.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Méthode SetIndexMode format Windows Media
- Méthode SetIndexMode format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031286"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="b1a75-106">IConfigAsfWriter :: SetIndexMode, méthode</span><span class="sxs-lookup"><span data-stu-id="b1a75-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="b1a75-107">La méthode **SetIndexMode** permet à l’application de contrôler si le fichier sera indexé temporellement.</span><span class="sxs-lookup"><span data-stu-id="b1a75-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a75-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1a75-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="b1a75-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1a75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a75-110">*bIndexFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b1a75-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a75-111">Variable de type **bool**; **True** spécifie que le fichier sera indexé temporellement.</span><span class="sxs-lookup"><span data-stu-id="b1a75-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a75-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1a75-112">Return value</span></span>

<span data-ttu-id="b1a75-113">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1a75-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b1a75-114">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1a75-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1a75-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b1a75-115">Remarks</span></span>

<span data-ttu-id="b1a75-116">Par défaut, l' [enregistreur ASF WM](wm-asf-writer-filter.md) crée des fichiers ASF indexés de façon temporelle.</span><span class="sxs-lookup"><span data-stu-id="b1a75-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="b1a75-117">Il effectue l’indexation lorsque le graphique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="b1a75-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="b1a75-118">Vous pouvez désactiver ce comportement si vous souhaitez effectuer votre propre indexation basée sur des trames en tant qu’étape de traitement.</span><span class="sxs-lookup"><span data-stu-id="b1a75-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="b1a75-119">Pour créer un fichier d’index de frames, appelez **SetIndexMode**(false), créez le fichier, puis utilisez directement les méthodes du kit de développement logiciel (SDK) du format Windows Media pour créer un index basé sur des frames pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="b1a75-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1a75-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1a75-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1a75-121">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1a75-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 