---
description: Définit des méthodes de mappage à un ID de classe.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Énumération TYSPEC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525132"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="4cd13-103">Énumération TYSPEC</span><span class="sxs-lookup"><span data-stu-id="4cd13-103">TYSPEC enumeration</span></span>

<span data-ttu-id="4cd13-104">Définit des méthodes de mappage à un ID de classe.</span><span class="sxs-lookup"><span data-stu-id="4cd13-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd13-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cd13-105">Syntax</span></span>


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a><span data-ttu-id="4cd13-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4cd13-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4cd13-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**\_CLSID TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="4cd13-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-108">CLSID.</span><span class="sxs-lookup"><span data-stu-id="4cd13-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="4cd13-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**</span><span class="sxs-lookup"><span data-stu-id="4cd13-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-110">Extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="4cd13-110">A file name extension.</span></span> <span data-ttu-id="4cd13-111">Cette valeur n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="4cd13-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="4cd13-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ MimeType**</span><span class="sxs-lookup"><span data-stu-id="4cd13-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-113">Type MIME.</span><span class="sxs-lookup"><span data-stu-id="4cd13-113">A MIME type.</span></span> <span data-ttu-id="4cd13-114">Cette valeur n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="4cd13-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="4cd13-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_nom de fichier TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="4cd13-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-116">Nom d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="4cd13-116">A file name.</span></span> <span data-ttu-id="4cd13-117">Cette valeur n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="4cd13-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="4cd13-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**\_ProgID TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="4cd13-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-119">PROGID.</span><span class="sxs-lookup"><span data-stu-id="4cd13-119">A PROGID.</span></span> <span data-ttu-id="4cd13-120">Cette valeur n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="4cd13-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="4cd13-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PackageName**</span><span class="sxs-lookup"><span data-stu-id="4cd13-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-122">Nom du package.</span><span class="sxs-lookup"><span data-stu-id="4cd13-122">A package name.</span></span> <span data-ttu-id="4cd13-123">Cette valeur n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="4cd13-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="4cd13-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_ObjectID TYSPEC**</span><span class="sxs-lookup"><span data-stu-id="4cd13-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="4cd13-125">Un ID d’objet.</span><span class="sxs-lookup"><span data-stu-id="4cd13-125">An object ID.</span></span> <span data-ttu-id="4cd13-126">Cette valeur n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="4cd13-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cd13-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4cd13-127">Remarks</span></span>

<span data-ttu-id="4cd13-128">L’Union **uCLSSPEC** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="4cd13-128">The **uCLSSPEC** union is defined as follows:</span></span>

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a><span data-ttu-id="4cd13-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cd13-129">Requirements</span></span>



| <span data-ttu-id="4cd13-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cd13-130">Requirement</span></span> | <span data-ttu-id="4cd13-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cd13-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd13-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="4cd13-132">IDL</span></span><br/> | <dl> <span data-ttu-id="4cd13-133"><dt>Wtypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cd13-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd13-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cd13-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd13-135">**Coinstallation**</span><span class="sxs-lookup"><span data-stu-id="4cd13-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
