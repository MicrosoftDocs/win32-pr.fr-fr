---
title: EnumLayoutOrTipForSetup fonction)
description: Énumère les dispositions de clavier installées et les services de texte de l’interface utilisateur du programme d’installation ou OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- EnumLayoutOrTipForSetup fonction Text Services Framework
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511551"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="7360a-104">EnumLayoutOrTipForSetup fonction)</span><span class="sxs-lookup"><span data-stu-id="7360a-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="7360a-105">Énumère les dispositions de clavier installées et les services de texte de l’interface utilisateur du programme d’installation ou OOBE.</span><span class="sxs-lookup"><span data-stu-id="7360a-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="7360a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7360a-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7360a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7360a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7360a-108">*LangID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7360a-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7360a-109">ID de langue de l’élément à énumérer.</span><span class="sxs-lookup"><span data-stu-id="7360a-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="7360a-110">*pLayoutOrTip* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7360a-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7360a-111">Pointeur vers la mémoire tampon qui reçoit le tableau de structures LAYOUTORTIP.</span><span class="sxs-lookup"><span data-stu-id="7360a-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="7360a-112">Il peut s’agir de la **valeur null** pour recevoir le nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="7360a-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="7360a-113">*uBufLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7360a-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7360a-114">Longueur de la mémoire tampon vers laquelle pointe *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="7360a-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="7360a-115">Cette valeur est ignorée si *pLayoutOrTip* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7360a-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7360a-116">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7360a-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7360a-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7360a-117">Not used.</span></span> <span data-ttu-id="7360a-118">Ce doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7360a-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7360a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7360a-119">Return value</span></span>

<span data-ttu-id="7360a-120">Si *pLayoutOrTip* a la **valeur null**, le nombre d’éléments de clavier enregistrés dans le système ; dans le cas contraire, il s’agit du nombre d’éléments de clavier copiés dans *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="7360a-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="7360a-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7360a-121">Remarks</span></span>

<span data-ttu-id="7360a-122">Il n’existe aucune bibliothèque d’importation qui définit cette fonction. il est donc nécessaire d’obtenir un pointeur vers cette fonction à l’aide de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="7360a-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="7360a-123">L’utilisation incorrecte de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut compromettre la sécurité de votre application en chargeant la dll incorrecte.</span><span class="sxs-lookup"><span data-stu-id="7360a-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="7360a-124">Pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Microsoft Windows, consultez l’article sur l’ordre de recherche de la [bibliothèque de liens dynamiques](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="7360a-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="7360a-125">La définition de LAYOUTORTIP est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7360a-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="7360a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7360a-126">Requirements</span></span>



| <span data-ttu-id="7360a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7360a-127">Requirement</span></span> | <span data-ttu-id="7360a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7360a-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7360a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7360a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7360a-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7360a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7360a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7360a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7360a-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7360a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7360a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7360a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7360a-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7360a-134"><dt>Input.dll</dt></span></span> </dl> |



 

