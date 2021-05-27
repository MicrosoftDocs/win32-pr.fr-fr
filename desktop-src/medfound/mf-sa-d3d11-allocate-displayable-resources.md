---
description: Spécifie si l’allocateur d’exemple de la MFT (SA) doit allouer la texture Direct3D sous-jacente à l’aide de l’indicateur D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE.
title: MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES (Mftransform.h)
ms.topic: reference
ms.date: 03/31/2018
ms.openlocfilehash: fedcfbe98344dd9b424c1a8ce90e847e98f1af51
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548704"
---
# <a name="mf_sa_d3d_allocate_displayable_resources-attribute"></a><span data-ttu-id="7462b-103">\_Attribut des \_ \_ \_ ressources affichables \_ de l’allocation de la sa D3D MF</span><span class="sxs-lookup"><span data-stu-id="7462b-103">MF\_SA\_D3D\_ALLOCATE\_DISPLAYABLE\_RESOURCES attribute</span></span>

<span data-ttu-id="7462b-104">Spécifie si l’allocateur d’exemple de la MFT (SA) doit allouer la texture Direct3D sous-jacente à l’aide de l’indicateur [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) .</span><span class="sxs-lookup"><span data-stu-id="7462b-104">Specifies if the MFT’s Sample Allocator (SA) should allocate the underlying Direct3D Texture using the [D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) flag.</span></span> 

## <a name="data-type"></a><span data-ttu-id="7462b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7462b-105">Data type</span></span>

<span data-ttu-id="7462b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7462b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7462b-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="7462b-107">Remarks</span></span>

<span data-ttu-id="7462b-108">Cet attribut est disponible en vedette avec Windows 10 Build 20348.</span><span class="sxs-lookup"><span data-stu-id="7462b-108">This attribute is available staring with Windows 10 build 20348.</span></span> 

> [!NOTE]
> <span data-ttu-id="7462b-109">Le champ membre **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** de l’énumération [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) sera disponible dans une version ultérieure du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7462b-109">The **D3D11_RESOURCE_MISC_SHARED_DISPLAYABLE** member field of the [D3D11_RESOURCE_MISC_FLAG](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) enumeration will be available in a future release of the SDK.</span></span>

<span data-ttu-id="7462b-110">La couche de plateforme Media Foundation définit l’attribut **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** lors du rendu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="7462b-110">The Media Foundation platform layer sets the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute when rendering video.</span></span> <span data-ttu-id="7462b-111">Une application peut également choisir de définir cet attribut si elle souhaite implémenter son propre convertisseur vidéo et utiliser des ressources affichables par D3D11.</span><span class="sxs-lookup"><span data-stu-id="7462b-111">An app could also opt to set this attribute if it wants to implement its own video renderer and make use of D3D11 Displayable Resources.</span></span> 

## <a name="example"></a><span data-ttu-id="7462b-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="7462b-112">Example</span></span>

<span data-ttu-id="7462b-113">L’exemple de code suivant illustre l’utilisation de l’attribut **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** .</span><span class="sxs-lookup"><span data-stu-id="7462b-113">The following code example demonstrates the usage of the **MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES** attribute.</span></span>

```cpp
class DecoderMFT : public IMFAttributes, public IMFTransform 
{ 
    //  
    ... Other implementation details ommitted 
    // 

public: 
    // Implementation of IMFAttributes::GetAttributes which is invoked by the MF Topology Loader 
    STDMETHODIMP GetAttribtues(IMFAttributes** attributes) 
    { 
        m_attributes.copyTo(attributes); 
        return S_OK; 
    } 

 

private: 
    // Private method to be called before DecoderMFT initializes its sample pool. 
    // A good place for this to happen is in the method which processes the  
    // 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING' event. 
    // At a minimum, this processing would be in DecoderMFT's implementation of IMFTransform::ProcessMessage.  

    HRESULT ConfigureTextureFlags() 
    { 
        UINT32 allocateDisplayables = MFGetAttributeUINT32(m_attributes.get(), 
            MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES, 0); 

        // If no MF_SA_* attributes which correspond to D3D misc flags are set then it is valid for 
        // miscFlags to be set to 0. 
        m_textureDesc.miscFlags = 0; 
        UINT32 sharedResources = 0; 

        if (allocateDisplayables != 0) 
        { 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_DISPLAYABLE; 
            // The following flag is required for the decoders output to 
            // use D3D11_RESOURCE_MISC_DISPLAYABLE. 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_EXCLUSIVE_WRITER; 

            // The following flags are required for the presentation API 
            // to consume and present these resources (also known as direct presentation). 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED_NTHANDLE; 

            sharedResources = 1; 
        } 
        else  
        { 
            // This handles the case when MF_SA_D3D11_ALLOCATE_DISPLAYABLE_RESOURCES was 0 or missing. 
            sharedResources = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED_WITHOUT_MUTEX, 0); 

            if (sharedResources != 0) 
            { 
                m_textureDesc.miscFlags |= D3D11_RESOURCE_MISC_SHARED; 
            } 
            else 
            { 
                UINT32 sharedKeyMutex = MFGetAttributeUINT32(m_attributes.get(), MF_SA_D3D11_SHARED, 0); 

                if (sharedKeyMutex != 0) 
                { 
                    m_textureDesc.micsFlags |= D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX; 
                } 
            } 
        } 

        // Processing for other MF_SA_* attributes which imply D3D11_RESOURCE_MISC flag 
        // omitted from this sample. 

        return S_OK; 

    } 

    // Private method showing how DecoderMFT can create a texture with the flags required 
    // to satisfy "MF_SA_D3D11_ALLOCATE_DISPLAYBLE_RESOURCES".  
    // Because this is a private function we know the passed in pointer is always valid. 
    // This would be invoked by another private DecoderMFT function when allocating an MFSample 
    // for its sample pool. 

    HRESULT AllocateTextureForSample(ID3D11Texture2D** texture2D) 
    { 
        return m_d3dDevice->CreateTexture2D(&m_textureDesc, nullptr, texture2D); 
    } 

    // ... other members omitted 
    wil::com_ptr_nothrow<IMFAttributes> m_attributes; 
    wil::com_ptr_nothrow<ID3D11Device> m_d3dDevice; 

    // This a texture description for D3D11 resources. 
    D3D11_TEXTURE_2D_DESC m_textureDesc = {}; 

}; 
```

## <a name="requirements"></a><span data-ttu-id="7462b-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7462b-114">Requirements</span></span>



| <span data-ttu-id="7462b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7462b-115">Requirement</span></span> | <span data-ttu-id="7462b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7462b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7462b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7462b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7462b-118">Windows 10 Build 20348</span><span class="sxs-lookup"><span data-stu-id="7462b-118">Windows 10 build 20348</span></span><br/>                                    |
| <span data-ttu-id="7462b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7462b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7462b-120"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="7462b-120"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7462b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7462b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7462b-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7462b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7462b-123">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7462b-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7462b-124">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7462b-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7462b-125">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7462b-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




