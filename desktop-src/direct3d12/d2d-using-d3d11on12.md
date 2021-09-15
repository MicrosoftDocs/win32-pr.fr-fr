---
title: D2D à l’aide de D3D11on12
description: L’exemple D3D1211on12 montre comment restituer du contenu D2D sur du contenu D3D12 en partageant des ressources entre un appareil 11 et un appareil 12.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18399b85499787f74dab725d562b6a299878b35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521748"
---
# <a name="d2d-using-d3d11on12"></a>D2D à l’aide de D3D11on12

L’exemple **D3D1211on12** montre comment restituer du contenu D2D sur du contenu D3D12 en partageant des ressources entre un appareil 11 et un appareil 12.

-   [Créer un ID3D11On12Device](#create-an-id3d11on12device)
-   [Créer une fabrique D2D](#create-a-d2d-factory)
-   [Créer une cible de rendu pour D2D](#create-a-render-target-for-d2d)
-   [Créer des objets texte D2D de base](#create-basic-d2d-text-objects)
-   [Mise à jour de la boucle de rendu principale](#updating-the-main-render-loop)
-   [Exécution de l'exemple](#run-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="create-an-id3d11on12device"></a>Créer un ID3D11On12Device

La première étape consiste à créer un [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) après la création du [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) , ce qui implique la création d’un [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) encapsulé autour du **ID3D12Device** via l’API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Cette API prend également, entre autres paramètres, un [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) afin que l’appareil 11On12 puisse soumettre ses commandes. Une fois le **ID3D11Device** créé, vous pouvez interroger l’interface **ID3D11On12Device** à partir de celui-ci. Il s’agit de l’objet périphérique principal qui sera utilisé pour configurer D2D.

Dans la méthode **LoadPipeline** , configurez les appareils.

``` syntax
 // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));
```



| Workflow d’appel                                              | Paramètres |
|--------------------------------------------------------|------------|
| [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a>Créer une fabrique D2D

Maintenant que nous disposons d’un appareil 11On12, nous l’utilisons pour créer une fabrique et un appareil D2D de la même manière qu’avec D3D11.

Ajoutez à la méthode **LoadAssets** .

``` syntax
 // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &d2dFactoryOptions, &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &m_dWriteFactory));
    }
```



| Workflow d’appel                                                                        | Paramètres                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_Options de \_ contexte de périphérique d2d1 \_**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [**\_Type de fabrique d2d1 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [**ID2D1Factory3::CreateDevice**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [**ID2D1Device::CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [**DWriteCreateFactory**](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [**\_type de fabrique DWRITE \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a>Créer une cible de rendu pour D2D

D3D12 est propriétaire de la chaîne de permutation. par conséquent, si vous souhaitez effectuer un rendu sur la mémoire tampon d’arrière-plan à l’aide de notre appareil 11On12 (contenu D2D), nous devons créer des ressources encapsulées de type [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) à partir des mémoires tampons d’arrière-plan de type [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource). Cela permet de lier le **ID3D12Resource** avec une interface basée sur d3d11 afin qu’il puisse être utilisé avec l’appareil 11On12. Une fois que nous avons une ressource encapsulée, nous pouvons créer une surface cible de rendu pour le rendu D2D, également dans la méthode **LoadAssets** .

``` syntax
 // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory->GetDesktopDpi(&dpiX, &dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );  

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
```



<table>
<thead>
<tr class="header">
<th>Workflow d’appel</th>
<th>Paramètres</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></td>
<td><dl><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a><br />
[<strong>D2D1_BITMAP_OPTIONS</strong>] (/Windows/Desktop/API/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)<br />
[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)<br />
[<strong>DXGI_FORMAT</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format)<br />
[<strong>D2D1_ALPHA_MODE</strong>] (/Windows/Desktop/API/dcommon/ne-dcommon-d2d1_alpha_mode)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain :: GetBuffer</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></td>
<td><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext :: CreateBitmapFromDxgiSurface</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a>Créer des objets texte D2D de base

Nous avons maintenant un [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) pour afficher le contenu 3D, un [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) partagé avec notre appareil via un [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) , que nous pouvons utiliser pour afficher le contenu 2D, et ils sont tous deux configurés pour être rendus dans la même chaîne de permutation. Cet exemple utilise simplement l’appareil D2D pour restituer du texte sur la scène 3D, de la même façon que les jeux affichent leur interface utilisateur. Pour cela, nous devons créer des objets D2D de base, toujours dans la méthode **LoadAssets** .

``` syntax
 // Create D2D/DWrite objects for rendering text.
    {
        ThrowIfFailed(m_d2dDeviceContext->CreateSolidColorBrush(D2D1::ColorF(D2D1::ColorF::Black), &m_textBrush));
        ThrowIfFailed(m_dWriteFactory->CreateTextFormat(
            L"Verdana",
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            50,
            L"en-us",
            &m_textFormat
            ));
        ThrowIfFailed(m_textFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER));
        ThrowIfFailed(m_textFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER));
    }
```



| Workflow d’appel                                                                                           | Paramètres                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ID2D1RenderTarget :: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))    | [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [**IDWriteFactory :: CreateTextFormat**](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [**épaisseur de la \_ police DWRITE \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [**IDWriteTextFormat::SetTextAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [**DWRITE \_ alignement du texte \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [**IDWriteTextFormat::SetParagraphAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [**DWRITE \_ alignement des paragraphes \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a>Mise à jour de la boucle de rendu principale

Maintenant que l’initialisation de l’exemple est terminée, nous pouvons passer à la boucle de rendu principale.

``` syntax
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(0, 0));

    MoveToNextFrame();
}
```



| Workflow d’appel                                                              | Paramètres |
|------------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

La seule chose à faire pour notre boucle de rendu est l’appel **RenderUI** , qui utilisera D2D pour afficher l’interface utilisateur. Notez que nous exécutons tout d’abord toutes les listes de commandes D3D12 pour afficher notre scène 3D, puis nous rendons notre interface utilisateur au-dessus. Avant de plonger dans **RenderUI**, nous devons examiner une modification apportée à **PopulateCommandLists**. Dans d’autres exemples, nous plaçons généralement une barrière de ressources sur la liste de commandes avant de la fermer pour faire passer la mémoire tampon d’arrière-plan de l’état de la cible de rendu à l’état actuel. Toutefois, dans cet exemple, nous supprimons ce cloisonnement de ressources, car nous devons toujours afficher les mémoires tampons d’arrière-plan avec D2D. Notez que lorsque nous avons créé nos ressources encapsulées de la mémoire tampon d’arrière-plan, nous avons spécifié l’état de la cible du rendu comme « IN » et l’état actuel comme « OUT ».

**RenderUI** est relativement simple en termes d’utilisation D2D. Nous définissons la cible de rendu et nous rendons notre texte. Toutefois, avant d’utiliser des ressources encapsulées sur un appareil 11On12, telles que les cibles de rendu de la mémoire tampon d’arrière-plan, nous devons appeler l’API [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) sur l’appareil 11On12. Après le rendu, nous appelons l’API [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) sur l’appareil 11On12. En appelant **ReleaseWrappedResources** , nous envoyons une barrière de ressources en arrière-plan qui fera passer la ressource spécifiée à l’État « out » spécifié au moment de la création. Dans notre cas, il s’agit de l’état actuel. Enfin, pour envoyer toutes les commandes effectuées sur l’appareil 11On12 au [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)partagé, vous devez appeler [**flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) sur le [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).

``` syntax
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}
```



| Workflow d’appel                                                                                                                                                                                 | Paramètres                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [**D2D1 \_ taille \_ F**](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [**D2D1 \_ rect \_ F**](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [**RectF**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [**ID2D1DeviceContext :: SetTarget**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [**ID2D1RenderTarget :: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [**ID2D1RenderTarget :: SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| [**ID2D1RenderTarget ::D rawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) |                                       |
| [**ID2D1RenderTarget :: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [**ID3D11DeviceContext :: Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a>Exécution de l'exemple

![sortie finale de l’échantillon 11 sur 12](images/11on12image.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Walk-Throughs de code D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Direct3D 11 sur 12](direct3d-11-on-12.md)
</dt> <dt>

[Interopérabilité Direct3D 12](direct3d-12-interop.md)
</dt> <dt>

[Référence 11on12](direct3d-11on12-reference.md)
</dt> </dl>

 

 