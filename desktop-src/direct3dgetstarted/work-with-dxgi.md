---
title: Utiliser les ressources de l’appareil DirectX
description: découvrez le rôle de Microsoft directx graphics Infrastructure (DXGI) dans votre jeu DirectX Windows Store.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068659"
---
# <a name="work-with-directx-device-resources"></a>Utiliser les ressources de l’appareil DirectX

découvrez le rôle de Microsoft directx graphics Infrastructure (DXGI) dans votre jeu DirectX Windows Store. DXGI est un ensemble d’API utilisé pour configurer et gérer les ressources de la carte graphique et graphiques de bas niveau. Sans cela, vous n’auriez aucun moyen de dessiner les graphiques de votre jeu dans une fenêtre.

DXGI de cette façon : pour accéder directement au GPU et gérer ses ressources, vous devez disposer d’un moyen de le décrire à votre application. L’élément le plus important concernant le GPU est l’endroit où vous pouvez dessiner des pixels afin qu’il puisse envoyer ces pixels à l’écran. En général, il s’agit de la « mémoire tampon d’arrière-plan », c’est-à-dire d’un emplacement dans la mémoire du GPU dans lequel vous pouvez dessiner les pixels, puis faire en sorte qu’elle soit « retournée » ou « permutée » et envoyée à l’écran sur un signal d’actualisation. DXGI vous permet d’acquérir cet emplacement et les moyens d’utiliser cette mémoire tampon (appelée *chaîne de permutation* , car il s’agit d’une chaîne de mémoires tampons remplaçables, qui autorise plusieurs stratégies de mise en mémoire tampon).

Pour ce faire, vous devez avoir accès à l’écriture dans la chaîne de permutation et à un handle vers la fenêtre qui affichera la mémoire tampon d’arrière-plan actuelle pour la chaîne de permutation. Vous devez également connecter les deux pour vous assurer que le système d’exploitation actualise la fenêtre avec le contenu de la mémoire tampon d’arrière-plan lorsque vous lui demandez de le faire.

Le processus global de dessin à l’écran est le suivant :

-   Procurez-vous un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) pour votre application.
-   Obtenir une interface pour le périphérique et le contexte Direct3D.
-   Créez la chaîne de permutation pour afficher votre image rendue dans le [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).
-   Créer une cible de rendu pour le dessin et la remplir avec des pixels.
-   Présentez la chaîne de permutation !

## <a name="create-a-window-for-your-app"></a>Créer une fenêtre pour votre application

La première chose à faire est de créer une fenêtre. Tout d’abord, créez une classe de fenêtre en remplissant une instance de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), puis inscrivez-la à l’aide de [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). La classe de fenêtre contient les propriétés essentielles de la fenêtre, y compris l’icône qu’elle utilise, la fonction de traitement de message statique (plus encore plus loin) et un nom unique pour la classe de fenêtre.


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



Ensuite, vous créez la fenêtre. Nous devons également fournir des informations sur la taille de la fenêtre et le nom de la classe de fenêtre que nous venons de créer. Quand vous appelez [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), vous recevez en retour un pointeur opaque vers la fenêtre appelée HWND ; vous devez conserver le pointeur HWND et l’utiliser chaque fois que vous devez référencer la fenêtre, y compris en la détruisant ou en la recréant, et (particulièrement important) lors de la création de la chaîne de permutation DXGI que vous utilisez pour dessiner dans la fenêtre.


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



le modèle d’application de bureau Windows comprend un hook dans la boucle de messages Windows. Vous devez baser votre boucle de programme principale sur ce hook en écrivant une fonction « StaticWindowProc » pour traiter les événements de fenêtrage. il doit s’agir d’une fonction statique, car Windows l’appellera en dehors du contexte d’une instance de classe. Voici un exemple très simple d’une fonction de traitement de message statique.


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



Cet exemple simple vérifie uniquement les conditions de sortie du programme : [**WM \_ Close**](/windows/desktop/winmsg/wm-close), sent lorsque la fenêtre est requise pour être fermée, et [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), qui est envoyé après la suppression de la fenêtre de l’écran. Une application de production complète doit également gérer d’autres événements de fenêtrage : pour obtenir la liste complète des événements de fenêtrage, consultez [notifications de fenêtre](/windows/desktop/winmsg/window-notifications).

la boucle de programme principale elle-même doit accuser réception des messages Windows en autorisant Windows la possibilité d’exécuter la procédure de message statique. aidez le programme à s’exécuter efficacement en dupliquant le comportement : chaque itération doit choisir de traiter de nouveaux messages Windows s’ils sont disponibles, et si aucun message ne se trouve dans la file d’attente, elle doit restituer un nouveau frame. Voici un exemple très simple :


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Obtenir une interface pour le périphérique et le contexte Direct3D

La première étape de l’utilisation de Direct3D consiste à acquérir une interface pour le matériel Direct3D (le GPU), représenté sous la forme d’instances de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) et [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2). La première est une représentation virtuelle des ressources GPU et la seconde est une abstraction indépendante du périphérique du pipeline de rendu et du processus. Voici un moyen simple de le considérer : **ID3D11Device** contient les méthodes graphiques que vous appelez rarement, généralement avant tout rendu, pour acquérir et configurer l’ensemble des ressources dont vous avez besoin pour commencer à dessiner des pixels. **ID3D11DeviceContext**, en revanche, contient les méthodes que vous appelez dans chaque frame : chargement dans des mémoires tampons et des vues et autres ressources, modification de l’état de fusion et de fusion de sortie, gestion des nuanceurs et dessin des résultats du passage de ces ressources par le biais des États et des nuanceurs.

Il y a une partie très importante de ce processus : la définition du niveau de fonctionnalité. Le niveau de fonctionnalité indique à DirectX le niveau minimum de matériel pris en charge par votre application, avec le niveau de fonctionnalité D3D \_ \_ \_ 9 \_ 1 comme ensemble de fonctionnalités le plus bas et le \_ niveau de fonctionnalité D3D \_ \_ 11 \_ 1 comme le plus élevé actuel. Vous devez prendre en charge 9 \_ 1 comme valeur minimale si vous souhaitez atteindre le public le plus vaste possible. Prenez le temps de lire les niveaux des [fonctionnalités](/previous-versions/windows/apps/hh994923(v=win.10)) Direct3D et évaluez les niveaux de fonctionnalité minimale et maximale que vous souhaitez que votre jeu prenne en charge et comprenez les implications de votre choix.

Obtenez des références (pointeurs) sur le périphérique Direct3D et le contexte de périphérique, puis stockez-les en tant que variables de niveau classe sur l’instance **DeviceResources** (en tant que pointeurs intelligents **ComPtr** ). Utilisez ces références chaque fois que vous avez besoin d’accéder au périphérique Direct3D ou au contexte de périphérique.


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a>Créer la chaîne de permutation

OK : vous avez une fenêtre dans laquelle dessiner, et vous disposez d’une interface pour envoyer des données et fournir des commandes au GPU. Voyons maintenant comment les réunir.

Tout d’abord, vous indiquez à DXGI les valeurs à utiliser pour les propriétés de la chaîne de permutation. Pour ce faire, utilisez une structure [**\_ desc de \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) . Six champs sont particulièrement importants pour les applications de bureau :

-   **Windowed**: indique si la chaîne de permutation est pleine-écran ou découpée dans la fenêtre. Affectez la valeur TRUE pour placer la chaîne de permutation dans la fenêtre que vous avez créée précédemment.
-   **BufferUsage**: définissez cette valeur sur la sortie de la \_ cible de rendu de l’utilisation de dxgi \_ \_ \_ . Cela indique que la chaîne de permutation sera une surface de dessin, ce qui vous permet de l’utiliser en tant que cible de rendu Direct3D.
-   **SwapEffect**: définissez cette valeur sur dxgi \_ swap \_ Effect \_ Flip \_ Sequential.
-   **Format**: le format \_ dxgi \_ B8G8R8A8 \_ UNORM spécifie la couleur 32 bits : 8 bits pour chacun des trois canaux de couleurs RVB et 8 bits pour le canal alpha.
-   **BufferCount**: définissez cette valeur sur 2 pour un comportement traditionnel de double mise en mémoire tampon afin d’éviter de détruire. Définissez le nombre de mémoires tampons sur 3 Si votre contenu graphique prend plusieurs cycles d’actualisation de l’analyse pour afficher une image unique (à 60 Hz, par exemple, le seuil est supérieur à 16 ms).
-   **SampleDesc**: ce champ contrôle l’échantillonnage multiple. Définissez **Count** sur 1 et **Quality** sur 0 pour les chaînes de permutation de modèle. (Pour utiliser l’échantillonnage multiple avec les chaînes de permutation-modèle, dessinez sur une cible de rendu à échantillonnage multiple distincte, puis résolvez cette cible vers la chaîne de permutation juste avant de la présenter. un exemple de code est fourni dans l' [échantillonnage multiple dans Windows applications du windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).)

Une fois que vous avez spécifié une configuration pour la chaîne de permutation, vous devez utiliser la même fabrique de DXGI qui a créé l’appareil Direct3D (et le contexte de périphérique) pour créer la chaîne de permutation.

* * Forme abrégée : * *

Récupérez la référence [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que vous avez créée précédemment. Effectuez une conversion vers [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (si vous ne l’avez pas déjà fait), puis appelez [**IDXGIDevice :: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) pour acquérir l’adaptateur DXGI. Obtenir la fabrique parente pour cet adaptateur en appelant [**IDXGIFactory2 :: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) hérite de [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) — vous pouvez maintenant utiliser cette fabrique pour créer la chaîne de permutation en appelant [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), comme illustré dans l’exemple de code suivant.


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



Si vous venez de commencer, il est probablement préférable d’utiliser la configuration indiquée ici. À ce stade, si vous connaissez déjà les versions précédentes de DirectX, vous vous demandez peut-être : « pourquoi ne pas créer l’appareil et échanger la chaîne en même temps, au lieu de revenir à l’ensemble de ces classes ? » La réponse est efficace : les chaînes de permutation sont des ressources de périphérique Direct3D et les ressources de l’appareil sont liées à l’appareil Direct3D particulier qui les a créées. Si vous créez un nouveau périphérique avec une nouvelle chaîne de permutation, vous devez recréer toutes les ressources de votre appareil à l’aide du nouveau périphérique Direct3D. Ainsi, en créant la chaîne de permutation avec la même fabrique (comme indiqué ci-dessus), vous pouvez recréer la chaîne de permutation et continuer à utiliser les ressources de l’appareil Direct3D que vous avez déjà chargées.

À présent, vous disposez d’une fenêtre du système d’exploitation, d’un moyen d’accéder au GPU et à ses ressources, et d’une chaîne de permutation pour afficher les résultats du rendu. Tout ce qu’il reste à faire, c’est de relier tout cela !

## <a name="create-a-render-target-for-drawing"></a>Créer une cible de rendu pour le dessin

Le pipeline du nuanceur a besoin d’une ressource dans laquelle dessiner des pixels. La façon la plus simple de créer cette ressource consiste à définir une ressource [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) comme mémoire tampon d’arrière-plan pour le nuanceur de pixels dans lequel dessiner, puis à lire cette texture dans la chaîne de permutation.

Pour ce faire, vous créez une *vue* de cible de rendu. Dans Direct3D, une vue est un moyen d’accéder à une ressource spécifique. Dans ce cas, la vue permet au nuanceur de pixels d’écrire dans la texture à mesure qu’il termine ses opérations par pixel.

Examinons le code de cette. Lorsque vous définissez \_ \_ \_ \_ la sortie de la cible de rendu de l’utilisation de dxgi sur la chaîne de permutation, qui a activé la ressource Direct3D sous-jacente à utiliser comme surface de dessin. Pour obtenir notre affichage de la cible de rendu, il suffit d’obtenir la mémoire tampon d’arrière-plan de la chaîne de permutation et de créer une vue de cible de rendu liée à la ressource de mémoire tampon d’arrière-plan.


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



Créez également une *mémoire tampon de stencil de profondeur*. Une mémoire tampon de stencil de profondeur est simplement une forme particulière de ressource [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , qui est généralement utilisée pour déterminer les pixels qui ont une priorité de dessin lors de la pixellisation en fonction de la distance des objets dans la scène de l’appareil photo. Une mémoire tampon de stencil de profondeur peut également être utilisée pour les effets de stencil, où les pixels spécifiques sont ignorés ou ignorés pendant la pixellisation. La taille de cette mémoire tampon doit être identique à celle de la cible de rendu. Notez que vous ne pouvez pas lire ou afficher la texture du stencil de profondeur de la mémoire tampon de trame, car elle est utilisée exclusivement par le pipeline du nuanceur avant et Pendant la pixellisation finale.

Créez également une vue pour la mémoire tampon du stencil de profondeur en tant que [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). La vue indique au pipeline de nuanceur comment interpréter la ressource [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) sous-jacente. par conséquent, si vous ne fournissez pas cette vue, aucun test de profondeur par pixel n’est effectué, et les objets de votre scène peuvent paraître un peu à l’intérieur de la partie la moins importante !


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



La dernière étape consiste à créer une fenêtre d’affichage. Cela définit le rectangle visible de la mémoire tampon d’arrière-plan affichée à l’écran. vous pouvez modifier la partie de la mémoire tampon affichée à l’écran en modifiant les paramètres de la fenêtre d’affichage. Ce code cible la taille de fenêtre entière, ou la résolution d’écran, dans le cas de chaînes d’échange plein écran. Pour vous amuser, modifiez les valeurs de coordonnées fournies et observez les résultats.


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



Et c’est ainsi que vous n’avez rien à faire pour dessiner des pixels dans une fenêtre ! Au début, il est judicieux de vous familiariser avec la façon dont DirectX, via DXGI, gère les ressources essentielles dont vous avez besoin pour commencer à dessiner des pixels.

Ensuite, vous allez examiner la structure du pipeline Graphics. consultez [comprendre le pipeline de rendu du modèle d’application DirectX](understand-the-directx-11-2-graphics-pipeline.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**À suivre**
</dt> <dt>

[Utiliser des nuanceurs et des ressources de nuanceur](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 