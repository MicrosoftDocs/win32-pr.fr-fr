---
description: Inscrit des modèles personnalisés.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'ID3DXFile :: RegisterTemplates, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522363"
---
# <a name="id3dxfileregistertemplates-method"></a><span data-ttu-id="5ffb7-103">ID3DXFile :: RegisterTemplates, méthode</span><span class="sxs-lookup"><span data-stu-id="5ffb7-103">ID3DXFile::RegisterTemplates method</span></span>

<span data-ttu-id="5ffb7-104">Inscrit des modèles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-104">Registers custom templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ffb7-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="5ffb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ffb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ffb7-107">*pvData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ffb7-107">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ffb7-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb7-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ffb7-109">Pointeur vers une mémoire tampon qui se compose d’un fichier. x au format texte ou binaire qui contient des modèles.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-109">Pointer to a buffer consisting of a .x file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb7-110">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ffb7-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ffb7-111">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ffb7-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ffb7-112">Taille de la mémoire tampon vers laquelle pointe pvData, en octets.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-112">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ffb7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ffb7-113">Return value</span></span>

<span data-ttu-id="5ffb7-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ffb7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ffb7-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5ffb7-116">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ffb7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5ffb7-117">Remarks</span></span>

<span data-ttu-id="5ffb7-118">Le fragment de code suivant fournit un exemple d’appel à **RegisterTemplates** et des exemples de contenu pour la mémoire tampon vers laquelle **pvData** pointe.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-118">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which **pvData** points.</span></span>


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



<span data-ttu-id="5ffb7-119">Tous les modèles doivent spécifier un nom et un UUID.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-119">All templates must specify a name and a UUID.</span></span>

<span data-ttu-id="5ffb7-120">Cette méthode appelle la méthode [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) , en obtenant un pointeur d’interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) en appelant [**CreateEnumObject**](id3dxfile--createenumobject.md) avec **pvData** comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ffb7-120">This method calls the [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) method, obtaining an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface pointer by calling [**CreateEnumObject**](id3dxfile--createenumobject.md) with **pvData** as the first parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ffb7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ffb7-121">Requirements</span></span>



| <span data-ttu-id="5ffb7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ffb7-122">Requirement</span></span> | <span data-ttu-id="5ffb7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ffb7-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffb7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ffb7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5ffb7-125"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ffb7-125"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="5ffb7-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ffb7-126">Library</span></span><br/> | <dl> <span data-ttu-id="5ffb7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ffb7-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5ffb7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ffb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffb7-129">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="5ffb7-129">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="5ffb7-130">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="5ffb7-130">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
