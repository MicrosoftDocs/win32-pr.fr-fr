---
title: Utiliser les ressources de l’appareil DirectX
description: Comprendre le rôle de Microsoft DirectX Graphics infrastructure (DXGI) dans votre jeu DirectX du Windows Store.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096e2be6f957d99bc6e5055f845c14448ecd647f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463355"
---
# <a name="work-with-directx-device-resources"></a><span data-ttu-id="b3685-103">Utiliser les ressources de l’appareil DirectX</span><span class="sxs-lookup"><span data-stu-id="b3685-103">Work with DirectX device resources</span></span>

<span data-ttu-id="b3685-104">Comprendre le rôle de Microsoft DirectX Graphics infrastructure (DXGI) dans votre jeu DirectX du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b3685-104">Understand the role of the Microsoft DirectX Graphics Infrastructure (DXGI) in your Windows Store DirectX game.</span></span> <span data-ttu-id="b3685-105">DXGI est un ensemble d’API utilisé pour configurer et gérer les ressources de la carte graphique et graphiques de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="b3685-105">DXGI is a set of APIs used to configure and manage low-level graphics and graphics adapter resources.</span></span> <span data-ttu-id="b3685-106">Sans cela, vous n’auriez aucun moyen de dessiner les graphiques de votre jeu dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3685-106">Without it, you'd have no way to draw your game's graphics to a window.</span></span>

<span data-ttu-id="b3685-107">DXGI de cette façon : pour accéder directement au GPU et gérer ses ressources, vous devez disposer d’un moyen de le décrire à votre application.</span><span class="sxs-lookup"><span data-stu-id="b3685-107">Think of DXGI this way: to directly access the GPU and manage its resources, you must have a way to describe it to your app.</span></span> <span data-ttu-id="b3685-108">L’élément le plus important concernant le GPU est l’endroit où vous pouvez dessiner des pixels afin qu’il puisse envoyer ces pixels à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b3685-108">The most important piece of info you need about the GPU is the place to draw pixels so it can send those pixels to the screen.</span></span> <span data-ttu-id="b3685-109">En général, il s’agit de la « mémoire tampon d’arrière-plan », c’est-à-dire d’un emplacement dans la mémoire du GPU dans lequel vous pouvez dessiner les pixels, puis faire en sorte qu’elle soit « retournée » ou « permutée » et envoyée à l’écran sur un signal d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="b3685-109">Typically this is called the "back buffer"—a location in GPU memory where you can draw the pixels and then have it "flipped" or "swapped" and sent to the screen on a refresh signal.</span></span> <span data-ttu-id="b3685-110">DXGI vous permet d’acquérir cet emplacement et les moyens d’utiliser cette mémoire tampon (appelée *chaîne de permutation* , car il s’agit d’une chaîne de mémoires tampons remplaçables, qui autorise plusieurs stratégies de mise en mémoire tampon).</span><span class="sxs-lookup"><span data-stu-id="b3685-110">DXGI lets you acquire that location and the means to use that buffer (called a *swap chain* because it is a chain of swappable buffers, allowing for multiple buffering strategies).</span></span>

<span data-ttu-id="b3685-111">Pour ce faire, vous devez avoir accès à l’écriture dans la chaîne de permutation et à un handle vers la fenêtre qui affichera la mémoire tampon d’arrière-plan actuelle pour la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b3685-111">To do this, you need access to write to the swap chain, and a handle to the window that will display the current back buffer for the swap chain.</span></span> <span data-ttu-id="b3685-112">Vous devez également connecter les deux pour vous assurer que le système d’exploitation actualise la fenêtre avec le contenu de la mémoire tampon d’arrière-plan lorsque vous lui demandez de le faire.</span><span class="sxs-lookup"><span data-stu-id="b3685-112">You also need to connect the two to ensure that the operating system will refresh the window with the contents of the back buffer when you request it to do so.</span></span>

<span data-ttu-id="b3685-113">Le processus global de dessin à l’écran est le suivant :</span><span class="sxs-lookup"><span data-stu-id="b3685-113">The overall process for drawing to the screen is as follows:</span></span>

-   <span data-ttu-id="b3685-114">Procurez-vous un [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) pour votre application.</span><span class="sxs-lookup"><span data-stu-id="b3685-114">Get a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) for your app.</span></span>
-   <span data-ttu-id="b3685-115">Obtenir une interface pour le périphérique et le contexte Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b3685-115">Get an interface for the Direct3D device and context.</span></span>
-   <span data-ttu-id="b3685-116">Créez la chaîne de permutation pour afficher votre image rendue dans le [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="b3685-116">Create the swap chain to display your rendered image in the [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>
-   <span data-ttu-id="b3685-117">Créer une cible de rendu pour le dessin et la remplir avec des pixels.</span><span class="sxs-lookup"><span data-stu-id="b3685-117">Create a render target for drawing and populate it with pixels.</span></span>
-   <span data-ttu-id="b3685-118">Présentez la chaîne de permutation !</span><span class="sxs-lookup"><span data-stu-id="b3685-118">Present the swap chain!</span></span>

## <a name="create-a-window-for-your-app"></a><span data-ttu-id="b3685-119">Créer une fenêtre pour votre application</span><span class="sxs-lookup"><span data-stu-id="b3685-119">Create a window for your app</span></span>

<span data-ttu-id="b3685-120">La première chose à faire est de créer une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3685-120">The first thing we need to do is create a window.</span></span> <span data-ttu-id="b3685-121">Tout d’abord, créez une classe de fenêtre en remplissant une instance de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), puis inscrivez-la à l’aide de [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="b3685-121">First, create a window class by populating an instance of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), then register it using [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="b3685-122">La classe de fenêtre contient les propriétés essentielles de la fenêtre, y compris l’icône qu’elle utilise, la fonction de traitement de message statique (plus encore plus loin) et un nom unique pour la classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3685-122">The window class contains essential properties of the window, including the icon it uses, the static message processing function (more on this later), and a unique name for the window class.</span></span>


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



<span data-ttu-id="b3685-123">Ensuite, vous créez la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3685-123">Next, you create the window.</span></span> <span data-ttu-id="b3685-124">Nous devons également fournir des informations sur la taille de la fenêtre et le nom de la classe de fenêtre que nous venons de créer.</span><span class="sxs-lookup"><span data-stu-id="b3685-124">We also need to provide size information for the window and the name of the window class we just created.</span></span> <span data-ttu-id="b3685-125">Quand vous appelez [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), vous recevez en retour un pointeur opaque vers la fenêtre appelée HWND ; vous devez conserver le pointeur HWND et l’utiliser chaque fois que vous devez référencer la fenêtre, y compris en la détruisant ou en la recréant, et (particulièrement important) lors de la création de la chaîne de permutation DXGI que vous utilisez pour dessiner dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3685-125">When you call [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), you get back an opaque pointer to the window called an HWND; you'll need to keep the HWND pointer and use it any time you need to reference the window, including destroying or recreating it, and (especially important) when creating the DXGI swap chain you use to draw in the window.</span></span>


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



<span data-ttu-id="b3685-126">Le modèle d’application de bureau Windows comprend un hook dans la boucle de messages Windows.</span><span class="sxs-lookup"><span data-stu-id="b3685-126">The Windows desktop app model includes a hook into the Windows message loop.</span></span> <span data-ttu-id="b3685-127">Vous devez baser votre boucle de programme principale sur ce hook en écrivant une fonction « StaticWindowProc » pour traiter les événements de fenêtrage.</span><span class="sxs-lookup"><span data-stu-id="b3685-127">You'll need to base your main program loop off of this hook by writing a "StaticWindowProc" function to process windowing events.</span></span> <span data-ttu-id="b3685-128">Il doit s’agir d’une fonction statique, car Windows l’appellera en dehors du contexte d’une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="b3685-128">This must be a static function because Windows will call it outside of the context of any class instance.</span></span> <span data-ttu-id="b3685-129">Voici un exemple très simple d’une fonction de traitement de message statique.</span><span class="sxs-lookup"><span data-stu-id="b3685-129">Here's a very simple example of a static message processing function.</span></span>


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



<span data-ttu-id="b3685-130">Cet exemple simple vérifie uniquement les conditions de sortie du programme : [**WM \_ Close**](/windows/desktop/winmsg/wm-close), sent lorsque la fenêtre est requise pour être fermée, et [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), qui est envoyé après la suppression de la fenêtre de l’écran.</span><span class="sxs-lookup"><span data-stu-id="b3685-130">This simple example only checks for program exit conditions: [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), sent when the window is requested to be closed, and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), which is sent after the window is actually removed from the screen.</span></span> <span data-ttu-id="b3685-131">Une application de production complète doit également gérer d’autres événements de fenêtrage : pour obtenir la liste complète des événements de fenêtrage, consultez [notifications de fenêtre](/windows/desktop/winmsg/window-notifications).</span><span class="sxs-lookup"><span data-stu-id="b3685-131">A full, production app needs to handle other windowing events too—for the complete list of windowing events, see [Window Notifications](/windows/desktop/winmsg/window-notifications).</span></span>

<span data-ttu-id="b3685-132">La boucle de programme principale elle-même doit accuser réception des messages Windows en permettant à Windows d’exécuter la procédure de message statique.</span><span class="sxs-lookup"><span data-stu-id="b3685-132">The main program loop itself needs to acknowledge Windows messages by allowing Windows the opportunity to run the static message proc.</span></span> <span data-ttu-id="b3685-133">Aidez le programme à s’exécuter efficacement en dupliquant le comportement : chaque itération doit choisir de traiter les nouveaux messages Windows s’ils sont disponibles et, si aucun message ne se trouve dans la file d’attente, il doit afficher un nouveau Frame.</span><span class="sxs-lookup"><span data-stu-id="b3685-133">Help the program run efficiently by forking the behavior: each iteration should choose to process new Windows messages if they are available, and if no messages are in the queue it should render a new frame.</span></span> <span data-ttu-id="b3685-134">Voici un exemple très simple :</span><span class="sxs-lookup"><span data-stu-id="b3685-134">Here's a very simple example:</span></span>


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a><span data-ttu-id="b3685-135">Obtenir une interface pour le périphérique et le contexte Direct3D</span><span class="sxs-lookup"><span data-stu-id="b3685-135">Get an interface for the Direct3D device and context</span></span>

<span data-ttu-id="b3685-136">La première étape de l’utilisation de Direct3D consiste à acquérir une interface pour le matériel Direct3D (le GPU), représenté sous la forme d’instances de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) et [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span><span class="sxs-lookup"><span data-stu-id="b3685-136">The first step to using Direct3D is to acquire an interface for the Direct3D hardware (the GPU), represented as instances of [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span></span> <span data-ttu-id="b3685-137">La première est une représentation virtuelle des ressources GPU et la seconde est une abstraction indépendante du périphérique du pipeline de rendu et du processus.</span><span class="sxs-lookup"><span data-stu-id="b3685-137">The former is a virtual representation of the GPU resources, and the latter is a device-agnostic abstraction of the rendering pipeline and process.</span></span> <span data-ttu-id="b3685-138">Voici un moyen simple de le considérer : **ID3D11Device** contient les méthodes graphiques que vous appelez rarement, généralement avant tout rendu, pour acquérir et configurer l’ensemble des ressources dont vous avez besoin pour commencer à dessiner des pixels.</span><span class="sxs-lookup"><span data-stu-id="b3685-138">Here's an easy way to think of it: **ID3D11Device** contains the graphics methods you call infrequently, usually before any rendering occurs, to acquire and configure the set of resources you need to start drawing pixels.</span></span> <span data-ttu-id="b3685-139">**ID3D11DeviceContext**, en revanche, contient les méthodes que vous appelez dans chaque frame : chargement dans des mémoires tampons et des vues et autres ressources, modification de l’état de fusion et de fusion de sortie, gestion des nuanceurs et dessin des résultats du passage de ces ressources par le biais des États et des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="b3685-139">**ID3D11DeviceContext**, on the other hand, contains the methods you call every frame: loading in buffers and views and other resources, changing output-merger and rasterizer state, managing shaders, and drawing the results of passing those resources through the states and shaders.</span></span>

<span data-ttu-id="b3685-140">Il y a une partie très importante de ce processus : la définition du niveau de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="b3685-140">There's one very important part of this process: setting the feature level.</span></span> <span data-ttu-id="b3685-141">Le niveau de fonctionnalité indique à DirectX le niveau minimum de matériel pris en charge par votre application, avec le niveau de fonctionnalité D3D \_ \_ \_ 9 \_ 1 comme ensemble de fonctionnalités le plus bas et le \_ niveau de fonctionnalité D3D \_ \_ 11 \_ 1 comme le plus élevé actuel.</span><span class="sxs-lookup"><span data-stu-id="b3685-141">The feature level tells DirectX the minimum level of hardware your app supports, with D3D\_FEATURE\_LEVEL\_9\_1 as the lowest feature set and D3D\_FEATURE\_LEVEL\_11\_1 as the current highest.</span></span> <span data-ttu-id="b3685-142">Vous devez prendre en charge 9 \_ 1 comme valeur minimale si vous souhaitez atteindre le public le plus vaste possible.</span><span class="sxs-lookup"><span data-stu-id="b3685-142">You should support 9\_1 as the minimum if you want to reach the widest possible audience.</span></span> <span data-ttu-id="b3685-143">Prenez le temps de lire les niveaux des [fonctionnalités](/previous-versions/windows/apps/hh994923(v=win.10)) Direct3D et évaluez les niveaux de fonctionnalité minimale et maximale que vous souhaitez que votre jeu prenne en charge et comprenez les implications de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b3685-143">Take some time to read up on Direct3D [feature levels](/previous-versions/windows/apps/hh994923(v=win.10)) and assess for yourself the minimum and maximum feature levels you want your game to support and to understand the implications of your choice.</span></span>

<span data-ttu-id="b3685-144">Obtenez des références (pointeurs) sur le périphérique Direct3D et le contexte de périphérique, puis stockez-les en tant que variables de niveau classe sur l’instance **DeviceResources** (en tant que pointeurs intelligents **ComPtr** ).</span><span class="sxs-lookup"><span data-stu-id="b3685-144">Obtain references (pointers) to both the Direct3D device and device context and store them as class-level variables on the **DeviceResources** instance (as **ComPtr** smart pointers).</span></span> <span data-ttu-id="b3685-145">Utilisez ces références chaque fois que vous avez besoin d’accéder au périphérique Direct3D ou au contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="b3685-145">Use these references whenever you need to access the Direct3D device or device context.</span></span>


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



## <a name="create-the-swap-chain"></a><span data-ttu-id="b3685-146">Créer la chaîne de permutation</span><span class="sxs-lookup"><span data-stu-id="b3685-146">Create the swap chain</span></span>

<span data-ttu-id="b3685-147">OK : vous avez une fenêtre dans laquelle dessiner, et vous disposez d’une interface pour envoyer des données et fournir des commandes au GPU.</span><span class="sxs-lookup"><span data-stu-id="b3685-147">Okay: You have a window to draw in, and you have an interface to send data and give commands to the GPU.</span></span> <span data-ttu-id="b3685-148">Voyons maintenant comment les réunir.</span><span class="sxs-lookup"><span data-stu-id="b3685-148">Now let's see how to bring them together.</span></span>

<span data-ttu-id="b3685-149">Tout d’abord, vous indiquez à DXGI les valeurs à utiliser pour les propriétés de la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b3685-149">First, you tell DXGI what values to use for the properties of the swap chain.</span></span> <span data-ttu-id="b3685-150">Pour ce faire, utilisez une structure [**\_ desc de \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .</span><span class="sxs-lookup"><span data-stu-id="b3685-150">Do this using a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span> <span data-ttu-id="b3685-151">Six champs sont particulièrement importants pour les applications de bureau :</span><span class="sxs-lookup"><span data-stu-id="b3685-151">Six fields are particularly important for desktop apps:</span></span>

-   <span data-ttu-id="b3685-152">**Windowed**: indique si la chaîne de permutation est pleine-écran ou découpée dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b3685-152">**Windowed**: Indicates whether the swap chain is full-screen or clipped to the window.</span></span> <span data-ttu-id="b3685-153">Affectez la valeur TRUE pour placer la chaîne de permutation dans la fenêtre que vous avez créée précédemment.</span><span class="sxs-lookup"><span data-stu-id="b3685-153">Set this to TRUE to put the swap chain in the window you created earlier.</span></span>
-   <span data-ttu-id="b3685-154">**BufferUsage**: définissez cette valeur sur la sortie de la \_ cible de rendu de l’utilisation de dxgi \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b3685-154">**BufferUsage**: Set this to DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT.</span></span> <span data-ttu-id="b3685-155">Cela indique que la chaîne de permutation sera une surface de dessin, ce qui vous permet de l’utiliser en tant que cible de rendu Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b3685-155">This indicates that the swap chain will be a drawing surface, allowing you to use it as a Direct3D render-target.</span></span>
-   <span data-ttu-id="b3685-156">**SwapEffect**: définissez cette valeur sur dxgi \_ swap \_ Effect \_ Flip \_ Sequential.</span><span class="sxs-lookup"><span data-stu-id="b3685-156">**SwapEffect**: Set this to DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL.</span></span>
-   <span data-ttu-id="b3685-157">**Format**: le format \_ dxgi \_ B8G8R8A8 \_ UNORM spécifie la couleur 32 bits : 8 bits pour chacun des trois canaux de couleurs RVB et 8 bits pour le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="b3685-157">**Format**: The DXGI\_FORMAT\_B8G8R8A8\_UNORM format specifies 32-bit color: 8 bits for each of the three RGB color channels, and 8 bits for the alpha channel.</span></span>
-   <span data-ttu-id="b3685-158">**BufferCount**: définissez cette valeur sur 2 pour un comportement traditionnel de double mise en mémoire tampon afin d’éviter de détruire.</span><span class="sxs-lookup"><span data-stu-id="b3685-158">**BufferCount**: Set this to 2 for a traditional double-buffered behavior to avoid tearing.</span></span> <span data-ttu-id="b3685-159">Définissez le nombre de mémoires tampons sur 3 Si votre contenu graphique prend plusieurs cycles d’actualisation de l’analyse pour afficher une image unique (à 60 Hz, par exemple, le seuil est supérieur à 16 ms).</span><span class="sxs-lookup"><span data-stu-id="b3685-159">Set the buffer count to 3 if your graphics content takes more than one monitor refresh cycle to render a single frame (at 60 Hz for example, the threshold is more than 16 ms).</span></span>
-   <span data-ttu-id="b3685-160">**SampleDesc**: ce champ contrôle l’échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="b3685-160">**SampleDesc**: This field controls multisampling.</span></span> <span data-ttu-id="b3685-161">Définissez **Count** sur 1 et **Quality** sur 0 pour les chaînes de permutation de modèle.</span><span class="sxs-lookup"><span data-stu-id="b3685-161">Set **Count** to 1 and **Quality** to 0 for flip-model swap chains.</span></span> <span data-ttu-id="b3685-162">(Pour utiliser l’échantillonnage multiple avec les chaînes de permutation-modèle, dessinez sur une cible de rendu à échantillonnage multiple distincte, puis résolvez cette cible vers la chaîne de permutation juste avant de la présenter.</span><span class="sxs-lookup"><span data-stu-id="b3685-162">(To use multisampling with flip-model swap chains, draw on a separate multisampled render target and then resolve that target to the swap chain just before presenting it.</span></span> <span data-ttu-id="b3685-163">Un exemple de code est fourni dans [échantillonnage multiple dans les applications du Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).)</span><span class="sxs-lookup"><span data-stu-id="b3685-163">Example code is provided in [Multisampling in Windows Store apps](/previous-versions/windows/apps/dn458384(v=win.10)).)</span></span>

<span data-ttu-id="b3685-164">Une fois que vous avez spécifié une configuration pour la chaîne de permutation, vous devez utiliser la même fabrique de DXGI qui a créé l’appareil Direct3D (et le contexte de périphérique) pour créer la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b3685-164">After you have specified a configuration for the swap chain, you must use the same DXGI factory that created the Direct3D device (and device context) in order to create the swap chain.</span></span>

<span data-ttu-id="b3685-165">**Forme abrégée :  **</span><span class="sxs-lookup"><span data-stu-id="b3685-165">**Short form:  **</span></span>

<span data-ttu-id="b3685-166">Récupérez la référence [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que vous avez créée précédemment.</span><span class="sxs-lookup"><span data-stu-id="b3685-166">Get the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) reference you created previously.</span></span> <span data-ttu-id="b3685-167">Effectuez une conversion vers [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (si vous ne l’avez pas déjà fait), puis appelez [**IDXGIDevice :: GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) pour acquérir l’adaptateur DXGI.</span><span class="sxs-lookup"><span data-stu-id="b3685-167">Upcast it to [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (if you haven't already) and then call [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) to acquire the DXGI adapter.</span></span> <span data-ttu-id="b3685-168">Obtenir la fabrique parente pour cet adaptateur en appelant [**IDXGIFactory2 :: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) hérite de [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) — vous pouvez maintenant utiliser cette fabrique pour créer la chaîne de permutation en appelant [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b3685-168">Get the parent factory for that adapter by calling [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))—now you can use that factory to create the swap chain by calling [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), as seen in the following code sample.</span></span>


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



<span data-ttu-id="b3685-169">Si vous venez de commencer, il est probablement préférable d’utiliser la configuration indiquée ici.</span><span class="sxs-lookup"><span data-stu-id="b3685-169">If you're just starting out, it's probably best to use the configuration shown here.</span></span> <span data-ttu-id="b3685-170">À ce stade, si vous connaissez déjà les versions précédentes de DirectX, vous vous demandez peut-être : « pourquoi ne pas créer l’appareil et échanger la chaîne en même temps, au lieu de revenir à l’ensemble de ces classes ? »</span><span class="sxs-lookup"><span data-stu-id="b3685-170">Now at this point, if you are already familiar with previous versions of DirectX you might be asking: "Why didn't we create the device and swap chain at the same time, instead of walking back through all of those classes?"</span></span> <span data-ttu-id="b3685-171">La réponse est efficace : les chaînes de permutation sont des ressources de périphérique Direct3D et les ressources de l’appareil sont liées à l’appareil Direct3D particulier qui les a créées.</span><span class="sxs-lookup"><span data-stu-id="b3685-171">The answer is efficiency: swap chains are Direct3D device resources, and device resources are tied to the particular Direct3D device that created them.</span></span> <span data-ttu-id="b3685-172">Si vous créez un nouveau périphérique avec une nouvelle chaîne de permutation, vous devez recréer toutes les ressources de votre appareil à l’aide du nouveau périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b3685-172">If you create a new device with a new swap chain, you have to recreate all your device resources using the new Direct3D device.</span></span> <span data-ttu-id="b3685-173">Ainsi, en créant la chaîne de permutation avec la même fabrique (comme indiqué ci-dessus), vous pouvez recréer la chaîne de permutation et continuer à utiliser les ressources de l’appareil Direct3D que vous avez déjà chargées.</span><span class="sxs-lookup"><span data-stu-id="b3685-173">So by creating the swap chain with the same factory (as shown above), you are able to recreate the swap chain and continue using the Direct3D device resources you already have loaded!</span></span>

<span data-ttu-id="b3685-174">À présent, vous disposez d’une fenêtre du système d’exploitation, d’un moyen d’accéder au GPU et à ses ressources, et d’une chaîne de permutation pour afficher les résultats du rendu.</span><span class="sxs-lookup"><span data-stu-id="b3685-174">Now you've got a window from the operating system, a way to access the GPU and its resources, and a swap chain to display the rendering results.</span></span> <span data-ttu-id="b3685-175">Tout ce qu’il reste à faire, c’est de relier tout cela !</span><span class="sxs-lookup"><span data-stu-id="b3685-175">All that's left is to wire the whole thing together!</span></span>

## <a name="create-a-render-target-for-drawing"></a><span data-ttu-id="b3685-176">Créer une cible de rendu pour le dessin</span><span class="sxs-lookup"><span data-stu-id="b3685-176">Create a render target for drawing</span></span>

<span data-ttu-id="b3685-177">Le pipeline du nuanceur a besoin d’une ressource dans laquelle dessiner des pixels.</span><span class="sxs-lookup"><span data-stu-id="b3685-177">The shader pipeline needs a resource to draw pixels into.</span></span> <span data-ttu-id="b3685-178">La façon la plus simple de créer cette ressource consiste à définir une ressource [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) comme mémoire tampon d’arrière-plan pour le nuanceur de pixels dans lequel dessiner, puis à lire cette texture dans la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b3685-178">The simplest way to create this resource is to define a [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource as a back buffer for the pixel shader to draw into, and then read that texture into the swap chain.</span></span>

<span data-ttu-id="b3685-179">Pour ce faire, vous créez une *vue* de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b3685-179">To do this, you create a render-target *view*.</span></span> <span data-ttu-id="b3685-180">Dans Direct3D, une vue est un moyen d’accéder à une ressource spécifique.</span><span class="sxs-lookup"><span data-stu-id="b3685-180">In Direct3D, a view is a way to access a specific resource.</span></span> <span data-ttu-id="b3685-181">Dans ce cas, la vue permet au nuanceur de pixels d’écrire dans la texture à mesure qu’il termine ses opérations par pixel.</span><span class="sxs-lookup"><span data-stu-id="b3685-181">In this case, the view enables the pixel shader to write into the texture as it completes its per-pixel operations.</span></span>

<span data-ttu-id="b3685-182">Examinons le code de cette.</span><span class="sxs-lookup"><span data-stu-id="b3685-182">Let's look at the code for this.</span></span> <span data-ttu-id="b3685-183">Lorsque vous définissez \_ \_ \_ \_ la sortie de la cible de rendu de l’utilisation de dxgi sur la chaîne de permutation, qui a activé la ressource Direct3D sous-jacente à utiliser comme surface de dessin.</span><span class="sxs-lookup"><span data-stu-id="b3685-183">When you set DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT on the swap chain, that enabled the underlying Direct3D resource to be used as a drawing surface.</span></span> <span data-ttu-id="b3685-184">Pour obtenir notre affichage de la cible de rendu, il suffit d’obtenir la mémoire tampon d’arrière-plan de la chaîne de permutation et de créer une vue de cible de rendu liée à la ressource de mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b3685-184">So to get our render target view, we just need to get the back buffer from the swap chain and create a render target view bound to the back buffer resource.</span></span>


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



<span data-ttu-id="b3685-185">Créez également une *mémoire tampon de stencil de profondeur*.</span><span class="sxs-lookup"><span data-stu-id="b3685-185">Also create a *depth-stencil buffer*.</span></span> <span data-ttu-id="b3685-186">Une mémoire tampon de stencil de profondeur est simplement une forme particulière de ressource [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , qui est généralement utilisée pour déterminer les pixels qui ont une priorité de dessin lors de la pixellisation en fonction de la distance des objets dans la scène de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b3685-186">A depth-stencil buffer is just a particular form of [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource, which is typically used to determine which pixels have draw priority during rasterization based on the distance of the objects in the scene from the camera.</span></span> <span data-ttu-id="b3685-187">Une mémoire tampon de stencil de profondeur peut également être utilisée pour les effets de stencil, où les pixels spécifiques sont ignorés ou ignorés pendant la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="b3685-187">A depth-stencil buffer can also be used for stencil effects, where specific pixels are discarded or ignored during rasterization.</span></span> <span data-ttu-id="b3685-188">La taille de cette mémoire tampon doit être identique à celle de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b3685-188">This buffer must be the same size as the render target.</span></span> <span data-ttu-id="b3685-189">Notez que vous ne pouvez pas lire ou afficher la texture du stencil de profondeur de la mémoire tampon de trame, car elle est utilisée exclusivement par le pipeline du nuanceur avant et Pendant la pixellisation finale.</span><span class="sxs-lookup"><span data-stu-id="b3685-189">Note that you cannot read from or render to the frame buffer depth-stencil texture because it is used exclusively by the shader pipeline before and during final rasterization.</span></span>

<span data-ttu-id="b3685-190">Créez également une vue pour la mémoire tampon du stencil de profondeur en tant que [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="b3685-190">Also create a view for the depth-stencil buffer as an [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span></span> <span data-ttu-id="b3685-191">La vue indique au pipeline de nuanceur comment interpréter la ressource [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) sous-jacente. par conséquent, si vous ne fournissez pas cette vue, aucun test de profondeur par pixel n’est effectué, et les objets de votre scène peuvent paraître un peu à l’intérieur de la partie la moins importante !</span><span class="sxs-lookup"><span data-stu-id="b3685-191">The view tells the shader pipeline how to interpret the underlying [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource - so if you don't supply this view no per-pixel depth testing is performed, and the objects in your scene may seem a bit inside-out at the very least!</span></span>


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



<span data-ttu-id="b3685-192">La dernière étape consiste à créer une fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b3685-192">The last step is to create a viewport.</span></span> <span data-ttu-id="b3685-193">Cela définit le rectangle visible de la mémoire tampon d’arrière-plan affichée à l’écran. vous pouvez modifier la partie de la mémoire tampon affichée à l’écran en modifiant les paramètres de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="b3685-193">This defines the visible rectangle of the back buffer displayed on the screen; you can change the part of the buffer that is displayed on the screen by changing the parameters of the viewport.</span></span> <span data-ttu-id="b3685-194">Ce code cible la taille de fenêtre entière, ou la résolution d’écran, dans le cas de chaînes d’échange plein écran.</span><span class="sxs-lookup"><span data-stu-id="b3685-194">This code targets the whole window size—or the screen resolution, in the case of full-screen swap chains.</span></span> <span data-ttu-id="b3685-195">Pour vous amuser, modifiez les valeurs de coordonnées fournies et observez les résultats.</span><span class="sxs-lookup"><span data-stu-id="b3685-195">For fun, change the supplied coordinate values and observe the results.</span></span>


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



<span data-ttu-id="b3685-196">Et c’est ainsi que vous n’avez rien à faire pour dessiner des pixels dans une fenêtre !</span><span class="sxs-lookup"><span data-stu-id="b3685-196">And that's how you go from nothing to drawing pixels in a window!</span></span> <span data-ttu-id="b3685-197">Au début, il est judicieux de vous familiariser avec la façon dont DirectX, via DXGI, gère les ressources essentielles dont vous avez besoin pour commencer à dessiner des pixels.</span><span class="sxs-lookup"><span data-stu-id="b3685-197">As you start out, it's a good idea to become familiar with how DirectX, through DXGI, manages the core resources you need to start drawing pixels.</span></span>

<span data-ttu-id="b3685-198">Ensuite, vous allez examiner la structure du pipeline Graphics. consultez [comprendre le pipeline de rendu du modèle d’application DirectX](understand-the-directx-11-2-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="b3685-198">Next you'll look at the structure of the graphics pipeline; see [Understand the DirectX app template's rendering pipeline](understand-the-directx-11-2-graphics-pipeline.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3685-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3685-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3685-200">**À suivre**</span><span class="sxs-lookup"><span data-stu-id="b3685-200">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="b3685-201">Utiliser des nuanceurs et des ressources de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b3685-201">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 