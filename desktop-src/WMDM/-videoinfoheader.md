---
title: Structure _VIDEOINFOHEADER
description: La \_ structure VIDEOINFOHEADER contient des informations sur un flux vidéo et inclut une \_ structure BITMAPINFOHEADER qui définit le format d’un frame individuel.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Structure de _VIDEOINFOHEADER Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528368"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="c6fbd-104">\_VIDEOINFOHEADER, structure</span><span class="sxs-lookup"><span data-stu-id="c6fbd-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="c6fbd-105">La structure **\_ VIDEOINFOHEADER** contient des informations sur un flux vidéo et inclut une structure **\_ BITMAPINFOHEADER** qui définit le format d’un frame individuel.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6fbd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6fbd-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="c6fbd-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c6fbd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c6fbd-108">**rcSource**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="c6fbd-109">La structure **Rect** qui spécifie la fenêtre vidéo source.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="c6fbd-110">**rcTarget**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="c6fbd-111">Structure **Rect** qui spécifie la fenêtre vidéo de destination.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="c6fbd-112">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="c6fbd-113">Valeur **DWORD** qui spécifie le débit de données approximatif du flux vidéo, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="c6fbd-114">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="c6fbd-115">Valeur **DWORD** qui spécifie le taux d’erreur des données du flux vidéo, en erreurs de bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="c6fbd-116">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="c6fbd-117">**Référence \_** Valeur de temps qui spécifie la durée d’affichage moyenne de la image vidéo, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="c6fbd-118">**bmiHeader**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="c6fbd-119">Structure **\_ BITMAPINFOHEADER** Win32 qui contient des informations de couleur et de dimension pour la bitmap de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="c6fbd-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6fbd-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6fbd-120">Requirements</span></span>



| <span data-ttu-id="c6fbd-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6fbd-121">Requirement</span></span> | <span data-ttu-id="c6fbd-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6fbd-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fbd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6fbd-123">Header</span></span><br/> | <dl> <span data-ttu-id="c6fbd-124"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6fbd-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6fbd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6fbd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fbd-126">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="c6fbd-127">**Structures**</span><span class="sxs-lookup"><span data-stu-id="c6fbd-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





