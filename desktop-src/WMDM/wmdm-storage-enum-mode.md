---
title: Énumération WMDM_STORAGE_ENUM_MODE
description: Le \_ \_ \_ type d’énumération du mode enum de stockage WMDM définit la manière dont le contenu sur le stockage doit être énuméré. Cette énumération est utilisée par IWMDMStorage3 SetEnumPreference.
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528391"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="da88e-105">\_ \_ Énumération du mode enum de stockage WMDM \_</span><span class="sxs-lookup"><span data-stu-id="da88e-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="da88e-106">Le type d’énumération du **\_ \_ \_ mode enum de stockage WMDM** définit la manière dont le contenu sur le stockage doit être énuméré.</span><span class="sxs-lookup"><span data-stu-id="da88e-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="da88e-107">Cette énumération est utilisée par [**IWMDMStorage3 :: SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span><span class="sxs-lookup"><span data-stu-id="da88e-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="da88e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da88e-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="da88e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="da88e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da88e-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**\_mode enum \_ brut**</span><span class="sxs-lookup"><span data-stu-id="da88e-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="da88e-111">Énumère le contenu sur le stockage de la même manière qu’il est organisé dans le système de fichiers du stockage.</span><span class="sxs-lookup"><span data-stu-id="da88e-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="da88e-112">**MODE ÉNUMÉRer utiliser les préférences de l' \_ \_ \_ appareil \_**</span><span class="sxs-lookup"><span data-stu-id="da88e-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="da88e-113">Énumère le contenu sur le stockage en fonction de la préférence de l’appareil, comme indiqué par le paramètre d’appareil *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="da88e-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="da88e-114">**\_vues de \_ métadonnées du mode enum \_**</span><span class="sxs-lookup"><span data-stu-id="da88e-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="da88e-115">Énumère le contenu sur le stockage en organisant le contenu en fonction d’une vue de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="da88e-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="da88e-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**MODE ÉNUMÉRer utiliser les préférences de l' \_ \_ \_ appareil \_**</span><span class="sxs-lookup"><span data-stu-id="da88e-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="da88e-117">Énumère le contenu sur le stockage en fonction de la préférence de l’appareil, comme indiqué par le paramètre d’appareil *UseMetadataViews* .</span><span class="sxs-lookup"><span data-stu-id="da88e-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="da88e-118">**\_vues de \_ métadonnées du mode enum \_**</span><span class="sxs-lookup"><span data-stu-id="da88e-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="da88e-119">Énumère le contenu sur le stockage en organisant le contenu en fonction d’une vue de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="da88e-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="da88e-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_vues de \_ métadonnées du mode enum \_**</span><span class="sxs-lookup"><span data-stu-id="da88e-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="da88e-121">Énumère le contenu sur le stockage en organisant le contenu en fonction d’une vue de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="da88e-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da88e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da88e-122">Requirements</span></span>



| <span data-ttu-id="da88e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da88e-123">Requirement</span></span> | <span data-ttu-id="da88e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="da88e-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da88e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="da88e-125">Header</span></span><br/> | <dl> <span data-ttu-id="da88e-126"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da88e-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da88e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da88e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da88e-128">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="da88e-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





