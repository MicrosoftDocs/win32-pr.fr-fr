---
description: Le \_ \_ type d’énumération des types de débits wpd fournit une description du type de compression fichiers audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Énumération WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533422"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="7e143-103">\_Énumération des types de débit wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e143-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="7e143-104">Le type d’énumération des **\_ \_ types de débits wpd** fournit une description du type de compression d’un fichier audio.</span><span class="sxs-lookup"><span data-stu-id="7e143-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e143-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e143-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="7e143-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7e143-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7e143-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_type de débit wpd \_ \_ non utilisé**</span><span class="sxs-lookup"><span data-stu-id="7e143-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="7e143-108">Cette valeur n’a pas été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7e143-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="7e143-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_type de débit wpd \_ \_ discret**</span><span class="sxs-lookup"><span data-stu-id="7e143-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="7e143-110">Compression à vitesse de transmission constante.</span><span class="sxs-lookup"><span data-stu-id="7e143-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="7e143-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIABLE de type de vitesse de \_ transmission wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7e143-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="7e143-112">Compression à vitesse de transmission variable.</span><span class="sxs-lookup"><span data-stu-id="7e143-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="7e143-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**\_type de vitesse de transmission wpd \_ \_ libre**</span><span class="sxs-lookup"><span data-stu-id="7e143-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="7e143-114">Taux binaire de format libre.</span><span class="sxs-lookup"><span data-stu-id="7e143-114">Free format bit rate.</span></span> <span data-ttu-id="7e143-115">Il s’agit d’une vitesse binaire constante inférieure à la vitesse de transmission maximale autorisée.</span><span class="sxs-lookup"><span data-stu-id="7e143-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e143-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e143-116">Requirements</span></span>



| <span data-ttu-id="7e143-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e143-117">Requirement</span></span> | <span data-ttu-id="7e143-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e143-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e143-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e143-119">Header</span></span><br/> | <dl> <span data-ttu-id="7e143-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e143-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e143-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e143-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e143-122">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="7e143-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




