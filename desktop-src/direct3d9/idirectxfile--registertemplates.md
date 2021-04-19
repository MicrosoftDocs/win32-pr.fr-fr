---
description: Inscrit des modèles personnalisés. Action déconseillée.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'IDirectXFile :: RegisterTemplates, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523819"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="c0b24-104">IDirectXFile :: RegisterTemplates, méthode</span><span class="sxs-lookup"><span data-stu-id="c0b24-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="c0b24-105">Inscrit des modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c0b24-105">Registers custom templates.</span></span> <span data-ttu-id="c0b24-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c0b24-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b24-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0b24-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="c0b24-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0b24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b24-109">*pvData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0b24-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b24-110">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0b24-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0b24-111">Pointeur vers une mémoire tampon qui se compose d’un fichier DirectX au format texte ou binaire qui contient des modèles.</span><span class="sxs-lookup"><span data-stu-id="c0b24-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="c0b24-112">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0b24-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b24-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0b24-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0b24-114">Taille de la mémoire tampon vers laquelle pointe pvData, en octets.</span><span class="sxs-lookup"><span data-stu-id="c0b24-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b24-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0b24-115">Return value</span></span>

<span data-ttu-id="c0b24-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0b24-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0b24-117">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0b24-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c0b24-118">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADVALUE, DXFILEERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="c0b24-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b24-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c0b24-119">Remarks</span></span>

<span data-ttu-id="c0b24-120">Le fragment de code suivant fournit un exemple d’appel à **RegisterTemplates** et des exemples de contenu pour la mémoire tampon vers laquelle pvData pointe.</span><span class="sxs-lookup"><span data-stu-id="c0b24-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="c0b24-121">Tous les modèles doivent spécifier un nom et un identificateur unique universel (UUID).</span><span class="sxs-lookup"><span data-stu-id="c0b24-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b24-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b24-122">Requirements</span></span>



| <span data-ttu-id="c0b24-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0b24-123">Requirement</span></span> | <span data-ttu-id="c0b24-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0b24-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b24-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0b24-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c0b24-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b24-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0b24-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0b24-127">Library</span></span><br/> | <dl> <span data-ttu-id="c0b24-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b24-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b24-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0b24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b24-130">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="c0b24-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
