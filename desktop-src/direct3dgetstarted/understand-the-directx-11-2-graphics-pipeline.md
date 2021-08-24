---
title: Comprendre le pipeline de rendu Direct3D 11
description: Précédemment, vous avez vu comment créer une fenêtre que vous pouvez utiliser pour dessiner dans le travail avec les ressources de l’appareil DirectX. À présent, vous allez apprendre à créer le pipeline graphique et à l’endroit où vous pouvez vous y connecter.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41a3e0fa7e3f7775c5cd51d49f9867864e7a204975fd982565491a63db829aa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727519"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Comprendre le pipeline de rendu Direct3D 11

Précédemment, vous avez vu comment créer une fenêtre que vous pouvez utiliser pour dessiner dans le [travail avec les ressources de l’appareil DirectX](work-with-dxgi.md). À présent, vous allez apprendre à créer le pipeline graphique et à l’endroit où vous pouvez vous y connecter.

Vous vous souviendrez qu’il existe deux interfaces Direct3D qui définissent le pipeline Graphics : [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), qui fournit une représentation virtuelle du GPU et de ses ressources. et [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), qui représente le traitement graphique pour le pipeline. En règle générale, vous utilisez une instance de **ID3D11Device** pour configurer et obtenir les ressources GPU dont vous avez besoin pour commencer à traiter les graphiques dans une scène, et vous utilisez **ID3D11DeviceContext** pour traiter ces ressources à chaque étape de nuanceur appropriée dans le pipeline Graphics. En général, vous appelez rarement des méthodes **ID3D11Device** , c’est-à-dire uniquement lorsque vous configurez une scène ou lorsque l’appareil change. En revanche, vous appelez **ID3D11DeviceContext** chaque fois que vous traitez un frame pour l’affichage.

Cet exemple crée et configure un pipeline graphique minimal adapté à l’affichage d’un cube à rotation simple et à nuance de vertex. Il illustre approximativement le plus petit ensemble de ressources nécessaires à l’affichage. À mesure que vous lisez les informations, notez les limitations de l’exemple donné, dans lesquelles vous devrez peut-être l’étendre pour prendre en charge la scène que vous souhaitez afficher.

Cet exemple couvre deux classes C++ pour Graphics : une classe de gestionnaire de ressources pour appareils et une classe de convertisseur de scène 3D. Cette rubrique se concentre spécifiquement sur le convertisseur de scène 3D.

## <a name="what-does-the-cube-renderer-do"></a>Que fait le convertisseur de cube ?

Le pipeline Graphics est défini par la classe de convertisseur de scène 3D. Le convertisseur de scène est capable d’effectuer les opérations suivantes :

-   Définissez des mémoires tampons constantes pour stocker vos données uniformes.
-   Définissez des mémoires tampons de vertex pour stocker vos données de vertex d’objets et les tampons d’index correspondants pour permettre au nuanceur de sommets de remonter correctement les triangles.
-   Créer des ressources de texture et des affichages de ressources.
-   Chargez vos objets Shader.
-   Mettez à jour les données graphiques pour afficher chaque frame.
-   Rendez (dessinez) les graphiques dans la chaîne de permutation.

Les quatre premiers processus utilisent généralement les méthodes de l’interface [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) pour initialiser et gérer les ressources graphiques, et les deux dernières utilisent les méthodes de l’interface [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) pour gérer et exécuter le pipeline Graphics.

Une instance de la classe de **convertisseur** est créée et gérée en tant que variable membre sur la classe de projet principale. L’instance **DeviceResources** est gérée comme un pointeur partagé entre plusieurs classes, notamment la classe de projet principale, la classe de fournisseur d’affichage d' **application** et le **convertisseur**. Si vous remplacez le **convertisseur** par votre propre classe, vous pouvez également déclarer et assigner l’instance **DeviceResources** en tant que membre d’un pointeur partagé :

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Il vous suffit de passer le pointeur dans le constructeur de classe (ou toute autre méthode d’initialisation) après la création de l’instance **DeviceResources** dans la méthode **Initialize** de la classe **app** . Vous pouvez également passer une **référence \_ ptr faible** si, à la place, vous souhaitez que votre classe principale soit entièrement propriétaire de l’instance **DeviceResources** .

## <a name="create-the-cube-renderer"></a>Créer le convertisseur de cube

Dans cet exemple, nous organisons la classe de convertisseur de scène avec les méthodes suivantes :

-   **CreateDeviceDependentResources**: appelée chaque fois que la scène doit être initialisée ou redémarrée. Cette méthode charge vos données, textures, nuanceurs et autres ressources de vertex initiaux, et construit la constante initiale et les mémoires tampons de vertex. En règle générale, la plupart du travail est effectué à l’aide des méthodes [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , et non des méthodes [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .
-   **CreateWindowSizeDependentResources**: appelée chaque fois que l’état de la fenêtre change, par exemple en cas de redimensionnement ou de modification de l’orientation. Cette méthode reconstruit les matrices de transformation, telles que celles de votre appareil photo.
-   **Mise à jour**: appelée en général à partir de la partie du programme qui gère l’État immédiat du jeu ; dans cet exemple, nous l’appelons simplement à partir de la classe **principale** . Faire en sorte que cette méthode lise les informations d’état de jeu qui affectent le rendu, telles que les mises à jour de la position de l’objet ou les images d’animation, ainsi que les données de jeu globales comme les niveaux d’éclairage ou les modifications de la physique du jeu. Ces entrées sont utilisées pour mettre à jour les mémoires tampons constantes par image et les données d’objet.
-   **Render**: généralement appelé à partir de la partie du programme qui gère la boucle de jeu ; dans ce cas, il est appelé à partir de la classe **principale** . Cette méthode construit le pipeline Graphics : elle lie les nuanceurs, lie les mémoires tampons et les ressources aux étapes du nuanceur et appelle le dessin pour le frame actuel.

Ces méthodes comprennent le corps des comportements pour le rendu d’une scène avec Direct3D à l’aide de vos ressources. Si vous étendez cet exemple avec une nouvelle classe de rendu, déclarez-le sur la classe de projet principale. Ainsi :

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

devient cela :

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Là encore, Notez que cet exemple suppose que les méthodes ont les mêmes signatures dans votre implémentation. Si les signatures ont changé, passez en revue la boucle **principale** et apportez les modifications en conséquence.

Examinons plus en détail les méthodes de rendu de scène.

## <a name="create-device-dependent-resources"></a>Créer des ressources dépendantes de l’appareil

**CreateDeviceDependentResources** consolide toutes les opérations d’initialisation de la scène et de ses ressources à l’aide d’appels [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) . Cette méthode suppose que l’appareil Direct3D vient d’être initialisé (ou a été recréé) pour une scène. Il recrée ou recharge toutes les ressources graphiques propres à la scène, telles que les nuanceurs de vertex et de pixels, les mémoires tampons de vertex et d’index des objets, ainsi que toutes les autres ressources (par exemple, les textures et les vues correspondantes).

Voici un exemple de code pour **CreateDeviceDependentResources**:


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



Chaque fois que vous chargez des ressources à partir d’un disque, des ressources telles que des fichiers ou des textures d’objets de nuanceur compilés (CSO ou. CSO), le fait de façon asynchrone. Cela vous permet de conserver le travail en cours d’exécution en même temps (comme d’autres tâches d’installation) et, comme la boucle principale n’est pas bloquée, vous pouvez continuer à afficher un fichier visuellement intéressant pour l’utilisateur (par exemple, une animation de chargement pour votre jeu). Cet exemple utilise l’API Concurrency :: Tasks qui est disponible à partir de Windows 8 ; Notez la syntaxe lambda utilisée pour encapsuler les tâches de chargement asynchrones. Ces expressions lambda représentent les fonctions appelées hors thread, donc un pointeur vers l’objet de classe actuel (**This**) est capturé explicitement.

Voici un exemple de la façon dont vous pouvez charger le bytecode du nuanceur :


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



Voici un exemple de création de mémoires tampons de vertex et d’index :


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



Cet exemple ne charge pas de maillages ni de textures. Vous devez créer les méthodes de chargement des types de maillage et de texture spécifiques à votre jeu, et les appeler de façon asynchrone.

Renseignez également les valeurs initiales de vos mémoires tampons constantes par scène. Les indicateurs d’éclairage fixe, ou d’autres données et éléments de scène statiques, sont des exemples de mémoire tampon constante par scène.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implémenter la méthode CreateWindowSizeDependentResources

Les méthodes **CreateWindowSizeDependentResources** sont appelées chaque fois que la taille, l’orientation ou la résolution de la fenêtre change.

Les ressources de taille de fenêtre sont mises à jour comme suit : la procédure de message statique obtient l’un des différents événements possibles indiquant une modification de l’état de la fenêtre. Votre boucle principale est ensuite informée de l’événement et appelle **CreateWindowSizeDependentResources** sur l’instance de classe principale, qui appelle ensuite l’implémentation **CreateWindowSizeDependentResources** sur la classe de convertisseur de scène.

Le travail principal de cette méthode consiste à s’assurer que les éléments visuels ne sont pas confondus ou non valides en raison d’une modification des propriétés de la fenêtre. Dans cet exemple, nous mettons à jour les matrices du projet avec un nouveau champ de vue (angle de vue) pour la fenêtre redimensionnée ou redimensionnée.

Nous avons déjà vu le code pour créer des ressources de fenêtre dans **DeviceResources** , qui était la chaîne de permutation (avec mémoire tampon d’arrière-plan) et la vue de la cible de rendu. Voici comment le convertisseur crée des transformations dépendantes des proportions :


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



Si votre scène a une disposition spécifique de composants qui dépend des proportions, il s’agit de l’endroit où les réorganiser en fonction de ces proportions. Vous pouvez également modifier la configuration du comportement de postérieur au traitement ici.

## <a name="implement-the-update-method"></a>Implémenter la méthode Update

La méthode de **mise à jour** est appelée une fois par boucle de jeu : dans cet exemple, elle est appelée par la méthode de la classe principale du même nom. Il a un objectif simple : mettre à jour la géométrie de la scène et l’état du jeu en fonction de la durée écoulée (ou des étapes de temps écoulées) depuis le cadre précédent. Dans cet exemple, nous faisons simplement pivoter le cube une fois par frame. Dans une scène de jeu réelle, cette méthode contient beaucoup plus de code pour vérifier l’état du jeu, mettre à jour les mémoires tampons constantes par image (ou autres), les mémoires tampons de géométrie et d’autres ressources en mémoire en conséquence. Étant donné que la communication entre le processeur et le GPU est insuffisante, veillez à mettre à jour uniquement les mémoires tampons qui ont été modifiées depuis la dernière trame. vos mémoires tampons constantes peuvent être regroupées ou fractionnées pour rendre cette opération plus efficace.


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



Dans ce cas, la fonction **Rotate** met à jour la mémoire tampon constante avec une nouvelle matrice de transformation pour le cube. La matrice est multipliée par vertex pendant l’étape du nuanceur de sommets. Étant donné que cette méthode est appelée avec chaque frame, il s’agit d’un bon emplacement pour agréger toutes les méthodes qui mettent à jour vos mémoires tampons de constantes et de vertex dynamiques, ou pour effectuer d’autres opérations qui préparent les objets dans la scène pour la transformation par le pipeline Graphics.

## <a name="implement-the-render-method"></a>Implémenter la méthode Render

Cette méthode est appelée une fois par boucle de jeu après l’appel de **Update**. Comme la **mise à jour**, la méthode **Render** est également appelée à partir de la classe principale. Il s’agit de la méthode dans laquelle le pipeline Graphics est construit et traité pour le frame à l’aide de méthodes sur l’instance [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) . Cela se termine par un dernier appel à [**ID3D11DeviceContext ::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed). Il est important de comprendre que cet appel (ou d’autres **\* *appels Draw _ similaires définis sur _* ID3D11DeviceContext**) exécute en fait le pipeline. En particulier, cela se produit lorsque Direct3D communique avec le GPU pour définir l’état du dessin, exécute chaque étape de pipeline et écrit les résultats des pixels dans la ressource de mémoire tampon de la cible de rendu pour l’affichage par la chaîne de permutation. Étant donné que la communication entre l’UC et le GPU est induite, combinez plusieurs appels de dessin en un seul, si vous le pouvez, surtout si votre scène contient un grand nombre d’objets rendus.


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



Il est conseillé de définir les différentes étapes de canalisation Graphics sur le contexte dans l’ordre. En règle générale, l’ordre est le suivant :

-   Actualisez les ressources de mémoire tampon constantes avec les nouvelles données si nécessaire (à l’aide des données de la **mise à jour**).
-   Assembly d’entrée (IA) : c’est là que nous attachons les tampons de vertex et d’index qui définissent la géométrie de la scène. Vous devez attacher chaque vertex et mémoire tampon d’index pour chaque objet de la scène. Étant donné que cet exemple a juste le cube, c’est assez simple.
-   Nuanceur de sommets (VS) : Attachez les nuanceurs de vertex qui transforment les données dans les mémoires tampons de vertex et attachez des mémoires tampons constantes pour le nuanceur de sommets.
-   Nuanceur de pixels (PS) : attachez tous les nuanceurs de pixels qui effectuent des opérations par pixel dans la scène pixellisée, puis attachez les ressources de l’appareil pour le nuanceur de pixels (mémoires tampons constantes, textures, etc.).
-   Fusion de sortie (OM) : il s’agit de l’étape dans laquelle les pixels sont fusionnés, une fois les nuanceurs terminés. Il s’agit d’une exception à la règle, car vous attachez vos stencils de profondeur et les cibles de rendu avant de définir les autres étapes. Vous pouvez avoir plusieurs stencils et cibles si vous avez des nuanceurs de sommets et de pixels supplémentaires qui génèrent des textures telles que des clichés instantanés, des cartes de hauteur ou d’autres techniques d’échantillonnage. dans ce cas, chaque passe de dessin aura besoin de la ou des cibles appropriées définies avant d’appeler une fonction de dessin.

Ensuite, dans la dernière section ([travailler avec](work-with-shaders-and-shader-resources.md)les nuanceurs et les ressources de nuanceur), nous examinerons les nuanceurs et voyons comment Direct3D les exécute.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**À suivre**
</dt> <dt>

[Utiliser des nuanceurs et des ressources de nuanceur](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
