---
title: Comprendre le pipeline de rendu Direct3D 11
description: Précédemment, vous avez vu comment créer une fenêtre que vous pouvez utiliser pour dessiner dans le travail avec les ressources de l’appareil DirectX. À présent, vous allez apprendre à créer le pipeline graphique et à l’endroit où vous pouvez vous y connecter.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "106543548"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="b9ec3-104">Comprendre le pipeline de rendu Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b9ec3-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="b9ec3-105">Précédemment, vous avez vu comment créer une fenêtre que vous pouvez utiliser pour dessiner dans le [travail avec les ressources de l’appareil DirectX](work-with-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="b9ec3-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="b9ec3-106">À présent, vous allez apprendre à créer le pipeline graphique et à l’endroit où vous pouvez vous y connecter.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="b9ec3-107">Vous vous souviendrez qu’il existe deux interfaces Direct3D qui définissent le pipeline Graphics : [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), qui fournit une représentation virtuelle du GPU et de ses ressources. et [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), qui représente le traitement graphique pour le pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="b9ec3-108">En règle générale, vous utilisez une instance de **ID3D11Device** pour configurer et obtenir les ressources GPU dont vous avez besoin pour commencer à traiter les graphiques dans une scène, et vous utilisez **ID3D11DeviceContext** pour traiter ces ressources à chaque étape de nuanceur appropriée dans le pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="b9ec3-109">En général, vous appelez rarement des méthodes **ID3D11Device** , c’est-à-dire uniquement lorsque vous configurez une scène ou lorsque l’appareil change.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="b9ec3-110">En revanche, vous appelez **ID3D11DeviceContext** chaque fois que vous traitez un frame pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="b9ec3-111">Cet exemple crée et configure un pipeline graphique minimal adapté à l’affichage d’un cube à rotation simple et à nuance de vertex.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="b9ec3-112">Il illustre approximativement le plus petit ensemble de ressources nécessaires à l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="b9ec3-113">À mesure que vous lisez les informations, notez les limitations de l’exemple donné, dans lesquelles vous devrez peut-être l’étendre pour prendre en charge la scène que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="b9ec3-114">Cet exemple couvre deux classes C++ pour Graphics : une classe de gestionnaire de ressources pour appareils et une classe de convertisseur de scène 3D.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="b9ec3-115">Cette rubrique se concentre spécifiquement sur le convertisseur de scène 3D.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="b9ec3-116">Que fait le convertisseur de cube ?</span><span class="sxs-lookup"><span data-stu-id="b9ec3-116">What does the cube renderer do?</span></span>

<span data-ttu-id="b9ec3-117">Le pipeline Graphics est défini par la classe de convertisseur de scène 3D.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="b9ec3-118">Le convertisseur de scène est capable d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="b9ec3-119">Définissez des mémoires tampons constantes pour stocker vos données uniformes.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="b9ec3-120">Définissez des mémoires tampons de vertex pour stocker vos données de vertex d’objets et les tampons d’index correspondants pour permettre au nuanceur de sommets de remonter correctement les triangles.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="b9ec3-121">Créer des ressources de texture et des affichages de ressources.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="b9ec3-122">Chargez vos objets Shader.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-122">Load your shader objects.</span></span>
-   <span data-ttu-id="b9ec3-123">Mettez à jour les données graphiques pour afficher chaque frame.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="b9ec3-124">Rendez (dessinez) les graphiques dans la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="b9ec3-125">Les quatre premiers processus utilisent généralement les méthodes de l’interface [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) pour initialiser et gérer les ressources graphiques, et les deux dernières utilisent les méthodes de l’interface [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) pour gérer et exécuter le pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="b9ec3-126">Une instance de la classe de **convertisseur** est créée et gérée en tant que variable membre sur la classe de projet principale.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="b9ec3-127">L’instance **DeviceResources** est gérée comme un pointeur partagé entre plusieurs classes, notamment la classe de projet principale, la classe de fournisseur d’affichage d' **application** et le **convertisseur**.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="b9ec3-128">Si vous remplacez le **convertisseur** par votre propre classe, vous pouvez également déclarer et assigner l’instance **DeviceResources** en tant que membre d’un pointeur partagé :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="b9ec3-129">Il vous suffit de passer le pointeur dans le constructeur de classe (ou toute autre méthode d’initialisation) après la création de l’instance **DeviceResources** dans la méthode **Initialize** de la classe **app** .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="b9ec3-130">Vous pouvez également passer une **référence \_ ptr faible** si, à la place, vous souhaitez que votre classe principale soit entièrement propriétaire de l’instance **DeviceResources** .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="b9ec3-131">Créer le convertisseur de cube</span><span class="sxs-lookup"><span data-stu-id="b9ec3-131">Create the cube renderer</span></span>

<span data-ttu-id="b9ec3-132">Dans cet exemple, nous organisons la classe de convertisseur de scène avec les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="b9ec3-133">**CreateDeviceDependentResources**: appelée chaque fois que la scène doit être initialisée ou redémarrée.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="b9ec3-134">Cette méthode charge vos données, textures, nuanceurs et autres ressources de vertex initiaux, et construit la constante initiale et les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="b9ec3-135">En règle générale, la plupart du travail est effectué à l’aide des méthodes [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , et non des méthodes [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="b9ec3-136">**CreateWindowSizeDependentResources**: appelée chaque fois que l’état de la fenêtre change, par exemple en cas de redimensionnement ou de modification de l’orientation.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="b9ec3-137">Cette méthode reconstruit les matrices de transformation, telles que celles de votre appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="b9ec3-138">**Mise à jour**: appelée en général à partir de la partie du programme qui gère l’État immédiat du jeu ; dans cet exemple, nous l’appelons simplement à partir de la classe **principale** .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="b9ec3-139">Faire en sorte que cette méthode lise les informations d’état de jeu qui affectent le rendu, telles que les mises à jour de la position de l’objet ou les images d’animation, ainsi que les données de jeu globales comme les niveaux d’éclairage ou les modifications de la physique du jeu.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="b9ec3-140">Ces entrées sont utilisées pour mettre à jour les mémoires tampons constantes par image et les données d’objet.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="b9ec3-141">**Render**: généralement appelé à partir de la partie du programme qui gère la boucle de jeu ; dans ce cas, il est appelé à partir de la classe **principale** .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="b9ec3-142">Cette méthode construit le pipeline Graphics : elle lie les nuanceurs, lie les mémoires tampons et les ressources aux étapes du nuanceur et appelle le dessin pour le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="b9ec3-143">Ces méthodes comprennent le corps des comportements pour le rendu d’une scène avec Direct3D à l’aide de vos ressources.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="b9ec3-144">Si vous étendez cet exemple avec une nouvelle classe de rendu, déclarez-le sur la classe de projet principale.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="b9ec3-145">Ainsi :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="b9ec3-146">devient cela :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="b9ec3-147">Là encore, Notez que cet exemple suppose que les méthodes ont les mêmes signatures dans votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="b9ec3-148">Si les signatures ont changé, passez en revue la boucle **principale** et apportez les modifications en conséquence.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="b9ec3-149">Examinons plus en détail les méthodes de rendu de scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="b9ec3-150">Créer des ressources dépendantes de l’appareil</span><span class="sxs-lookup"><span data-stu-id="b9ec3-150">Create device dependent resources</span></span>

<span data-ttu-id="b9ec3-151">**CreateDeviceDependentResources** consolide toutes les opérations d’initialisation de la scène et de ses ressources à l’aide d’appels [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="b9ec3-152">Cette méthode suppose que l’appareil Direct3D vient d’être initialisé (ou a été recréé) pour une scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="b9ec3-153">Il recrée ou recharge toutes les ressources graphiques propres à la scène, telles que les nuanceurs de vertex et de pixels, les mémoires tampons de vertex et d’index des objets, ainsi que toutes les autres ressources (par exemple, les textures et les vues correspondantes).</span><span class="sxs-lookup"><span data-stu-id="b9ec3-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="b9ec3-154">Voici un exemple de code pour **CreateDeviceDependentResources**:</span><span class="sxs-lookup"><span data-stu-id="b9ec3-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



<span data-ttu-id="b9ec3-155">Chaque fois que vous chargez des ressources à partir d’un disque, des ressources telles que des fichiers ou des textures d’objets de nuanceur compilés (CSO ou. CSO), le fait de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="b9ec3-156">Cela vous permet de conserver le travail en cours d’exécution en même temps (comme d’autres tâches d’installation) et, comme la boucle principale n’est pas bloquée, vous pouvez continuer à afficher un fichier visuellement intéressant pour l’utilisateur (par exemple, une animation de chargement pour votre jeu).</span><span class="sxs-lookup"><span data-stu-id="b9ec3-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="b9ec3-157">Cet exemple utilise l’API Concurrency :: Tasks disponible à partir de Windows 8 ; Notez la syntaxe lambda utilisée pour encapsuler les tâches de chargement asynchrones.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="b9ec3-158">Ces expressions lambda représentent les fonctions appelées hors thread, donc un pointeur vers l’objet de classe actuel (**This**) est capturé explicitement.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="b9ec3-159">Voici un exemple de la façon dont vous pouvez charger le bytecode du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-159">Here's an example of how you can load shader bytecode:</span></span>


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



<span data-ttu-id="b9ec3-160">Voici un exemple de création de mémoires tampons de vertex et d’index :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-160">Here's an example of how to create vertex and index buffers:</span></span>


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



<span data-ttu-id="b9ec3-161">Cet exemple ne charge pas de maillages ni de textures.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="b9ec3-162">Vous devez créer les méthodes de chargement des types de maillage et de texture spécifiques à votre jeu, et les appeler de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="b9ec3-163">Renseignez également les valeurs initiales de vos mémoires tampons constantes par scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="b9ec3-164">Les indicateurs d’éclairage fixe, ou d’autres données et éléments de scène statiques, sont des exemples de mémoire tampon constante par scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="b9ec3-165">Implémenter la méthode CreateWindowSizeDependentResources</span><span class="sxs-lookup"><span data-stu-id="b9ec3-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="b9ec3-166">Les méthodes **CreateWindowSizeDependentResources** sont appelées chaque fois que la taille, l’orientation ou la résolution de la fenêtre change.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="b9ec3-167">Les ressources de taille de fenêtre sont mises à jour comme suit : la procédure de message statique obtient l’un des différents événements possibles indiquant une modification de l’état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="b9ec3-168">Votre boucle principale est ensuite informée de l’événement et appelle **CreateWindowSizeDependentResources** sur l’instance de classe principale, qui appelle ensuite l’implémentation **CreateWindowSizeDependentResources** sur la classe de convertisseur de scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="b9ec3-169">Le travail principal de cette méthode consiste à s’assurer que les éléments visuels ne sont pas confondus ou non valides en raison d’une modification des propriétés de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="b9ec3-170">Dans cet exemple, nous mettons à jour les matrices du projet avec un nouveau champ de vue (angle de vue) pour la fenêtre redimensionnée ou redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="b9ec3-171">Nous avons déjà vu le code pour créer des ressources de fenêtre dans **DeviceResources** , qui était la chaîne de permutation (avec mémoire tampon d’arrière-plan) et la vue de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="b9ec3-172">Voici comment le convertisseur crée des transformations dépendantes des proportions :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



<span data-ttu-id="b9ec3-173">Si votre scène a une disposition spécifique de composants qui dépend des proportions, il s’agit de l’endroit où les réorganiser en fonction de ces proportions.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="b9ec3-174">Vous pouvez également modifier la configuration du comportement de postérieur au traitement ici.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="b9ec3-175">Implémenter la méthode Update</span><span class="sxs-lookup"><span data-stu-id="b9ec3-175">Implement the Update method</span></span>

<span data-ttu-id="b9ec3-176">La méthode de **mise à jour** est appelée une fois par boucle de jeu : dans cet exemple, elle est appelée par la méthode de la classe principale du même nom.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="b9ec3-177">Il a un objectif simple : mettre à jour la géométrie de la scène et l’état du jeu en fonction de la durée écoulée (ou des étapes de temps écoulées) depuis le cadre précédent.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="b9ec3-178">Dans cet exemple, nous faisons simplement pivoter le cube une fois par frame.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="b9ec3-179">Dans une scène de jeu réelle, cette méthode contient beaucoup plus de code pour vérifier l’état du jeu, mettre à jour les mémoires tampons constantes par image (ou autres), les mémoires tampons de géométrie et d’autres ressources en mémoire en conséquence.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="b9ec3-180">Étant donné que la communication entre le processeur et le GPU est insuffisante, veillez à mettre à jour uniquement les mémoires tampons qui ont été modifiées depuis la dernière trame. vos mémoires tampons constantes peuvent être regroupées ou fractionnées pour rendre cette opération plus efficace.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



<span data-ttu-id="b9ec3-181">Dans ce cas, la fonction **Rotate** met à jour la mémoire tampon constante avec une nouvelle matrice de transformation pour le cube.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="b9ec3-182">La matrice est multipliée par vertex pendant l’étape du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="b9ec3-183">Étant donné que cette méthode est appelée avec chaque frame, il s’agit d’un bon emplacement pour agréger toutes les méthodes qui mettent à jour vos mémoires tampons de constantes et de vertex dynamiques, ou pour effectuer d’autres opérations qui préparent les objets dans la scène pour la transformation par le pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="b9ec3-184">Implémenter la méthode Render</span><span class="sxs-lookup"><span data-stu-id="b9ec3-184">Implement the Render method</span></span>

<span data-ttu-id="b9ec3-185">Cette méthode est appelée une fois par boucle de jeu après l’appel de **Update**.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="b9ec3-186">Comme la **mise à jour**, la méthode **Render** est également appelée à partir de la classe principale.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="b9ec3-187">Il s’agit de la méthode dans laquelle le pipeline Graphics est construit et traité pour le frame à l’aide de méthodes sur l’instance [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="b9ec3-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="b9ec3-188">Cela se termine par un dernier appel à [**ID3D11DeviceContext ::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span><span class="sxs-lookup"><span data-stu-id="b9ec3-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="b9ec3-189">Il est important de comprendre que cet appel (ou d’autres **\* *appels Draw _ similaires définis sur _* ID3D11DeviceContext**) exécute en fait le pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="b9ec3-190">En particulier, cela se produit lorsque Direct3D communique avec le GPU pour définir l’état du dessin, exécute chaque étape de pipeline et écrit les résultats des pixels dans la ressource de mémoire tampon de la cible de rendu pour l’affichage par la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="b9ec3-191">Étant donné que la communication entre l’UC et le GPU est induite, combinez plusieurs appels de dessin en un seul, si vous le pouvez, surtout si votre scène contient un grand nombre d’objets rendus.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



<span data-ttu-id="b9ec3-192">Il est conseillé de définir les différentes étapes de canalisation Graphics sur le contexte dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="b9ec3-193">En règle générale, l’ordre est le suivant :</span><span class="sxs-lookup"><span data-stu-id="b9ec3-193">Typically, the order is:</span></span>

-   <span data-ttu-id="b9ec3-194">Actualisez les ressources de mémoire tampon constantes avec les nouvelles données si nécessaire (à l’aide des données de la **mise à jour**).</span><span class="sxs-lookup"><span data-stu-id="b9ec3-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="b9ec3-195">Assembly d’entrée (IA) : c’est là que nous attachons les tampons de vertex et d’index qui définissent la géométrie de la scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="b9ec3-196">Vous devez attacher chaque vertex et mémoire tampon d’index pour chaque objet de la scène.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="b9ec3-197">Étant donné que cet exemple a juste le cube, c’est assez simple.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="b9ec3-198">Nuanceur de sommets (VS) : Attachez les nuanceurs de vertex qui transforment les données dans les mémoires tampons de vertex et attachez des mémoires tampons constantes pour le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="b9ec3-199">Nuanceur de pixels (PS) : attachez tous les nuanceurs de pixels qui effectuent des opérations par pixel dans la scène pixellisée, puis attachez les ressources de l’appareil pour le nuanceur de pixels (mémoires tampons constantes, textures, etc.).</span><span class="sxs-lookup"><span data-stu-id="b9ec3-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="b9ec3-200">Fusion de sortie (OM) : il s’agit de l’étape dans laquelle les pixels sont fusionnés, une fois les nuanceurs terminés.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="b9ec3-201">Il s’agit d’une exception à la règle, car vous attachez vos stencils de profondeur et les cibles de rendu avant de définir les autres étapes.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="b9ec3-202">Vous pouvez avoir plusieurs stencils et cibles si vous avez des nuanceurs de sommets et de pixels supplémentaires qui génèrent des textures telles que des clichés instantanés, des cartes de hauteur ou d’autres techniques d’échantillonnage. dans ce cas, chaque passe de dessin aura besoin de la ou des cibles appropriées définies avant d’appeler une fonction de dessin.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="b9ec3-203">Ensuite, dans la dernière section ([travailler avec](work-with-shaders-and-shader-resources.md)les nuanceurs et les ressources de nuanceur), nous examinerons les nuanceurs et voyons comment Direct3D les exécute.</span><span class="sxs-lookup"><span data-stu-id="b9ec3-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9ec3-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9ec3-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b9ec3-205">**À suivre**</span><span class="sxs-lookup"><span data-stu-id="b9ec3-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="b9ec3-206">Utiliser des nuanceurs et des ressources de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b9ec3-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
