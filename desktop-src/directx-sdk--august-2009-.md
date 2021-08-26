---
description: à partir de Windows 8, le kit de développement logiciel (SDK) DirectX est inclus dans le SDK Windows.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Où est le Kit de développement logiciel (SDK) DirectX ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46559e839abea9d6e0c89ab7e5940e46b2d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886460"
---
# <a name="where-is-the-directx-sdk"></a>Où est le Kit de développement logiciel (SDK) DirectX ?

à partir de Windows 8, le kit de développement logiciel (SDK) DirectX est inclus dans le SDK Windows.

Nous avons créé initialement le kit de développement logiciel (SDK) DirectX en tant que plateforme hautes performances pour le développement de jeux en plus de Windows. À mesure que les technologies DirectX évoluent, elles sont devenues pertinentes pour un plus grand nombre d’applications. Aujourd’hui, la disponibilité du matériel Direct3D sur les ordinateurs permet même aux applications bureautiques traditionnelles d’utiliser l’accélération matérielle graphique. En parallèle, les technologies DirectX sont plus intégrées avec Windows. DirectX est désormais un composant fondamental de Windows.

Étant donné que le Kit de développement logiciel Windows constitue le principal outil des développeurs sous Windows, DirectX est désormais intégré. Vous pouvez à présent utiliser le Kit de développement logiciel Windows pour concevoir des jeux incroyables sous cette interface. pour télécharger le kit de développement logiciel (sdk) Windows 8. x ou Windows 10 sdk, consultez [SDK Windows et l’archive d’émulateur](https://developer.microsoft.com/windows/downloads/sdk-archive).

les technologies et les outils suivants, autrefois partie du kit de développement logiciel (SDK) DirectX, font désormais partie du SDK Windows.


| Technologie ou outil | Description | 
|--------------------|-------------|
| <span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows Composants graphiques<br /> | les en-têtes et les bibliothèques pour <a href="/windows/desktop/direct3d">Direct3D</a> et d’autres api graphiques Windows, comme <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, sont disponibles dans le SDK Windows. <br /><blockquote>[!Note]<br />les bibliothèques d’utilitaires D3DX9/D3DX10/D3DX11 déconseillées sont disponibles par le biais de <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, mais il existe également un certain nombre d' <a href="https://walbourn.github.io/living-without-d3dx/">alternatives open source</a>. la bibliothèque d’utilitaires D3DCSX DirectCompute et la DLL redistribuable sont disponibles dans la SDK Windows. D3DX12 est disponible sur <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.</blockquote><br /> | 
| <span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilateur HLSL (FXC.EXE)<br /> | le compilateur <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> est un outil du sous-répertoire d’architecture approprié dans le dossier bin du SDK Windows.<br /><blockquote>[!Note]<br />l’API D3DCompiler et la DLL redistribuable sont disponibles dans la SDK Windows.</blockquote><br /><br />pour le développement DirectX 12, utilisez le DXCompiler dans le SDK Windows et hébergé sur [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).<br /> | 
| <span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX pour Windows<br /> | un remplacement de l’outil PIX pour Windows est désormais une fonctionnalité de Microsoft Visual Studio, appelée Visual Studio débogueur graphics. cette fonctionnalité a beaucoup amélioré la convivialité, la prise en charge de Windows 8 et de Direct3D 11,1, ainsi que l’intégration aux fonctionnalités Microsoft Visual Studio traditionnelles, telles que les piles d’appels et le débogage de Windows pour le débogage <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Pour plus d’informations sur cette nouvelle fonctionnalité, consultez <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">débogage DirectX Graphics</a>.<br /><br />Pour le développement DirectX 12, consultez la dernière génération de <a href="https://devblogs.microsoft.com/pix/">pix sur Windows</a><br /> | 
| <span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> pour Windows<br /> | l’API <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> est désormais un composant système dans Windows 8. x et Windows 10. les en-têtes et les bibliothèques pour XAudio2 sont disponibles dans le SDK Windows. pour la prise en charge de Windows 7, consultez <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br /> | 
| <span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> pour Windows<br /> | l’API <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1,4 est désormais un composant système dans Windows 8. x et Windows 10. les en-têtes et les bibliothèques pour XInput sont disponibles dans le SDK Windows.<br /><blockquote>[!Note]<br />XInput héritée 9.1.0 est également disponible dans le cadre de Windows 7 ou version ultérieure.</blockquote><br /> | 
| <span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br /> | La version la plus récente de XNAMATH, qui est mise à jour pour les nouveaux jeux d’instructions et ARM/ARM64, est désormais <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>. les en-têtes pour DirectXMath sont disponibles dans le SDK Windows et sur <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br /> | 
| <span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Visionneuse DirectX et fonctionnalités DirectX<br /> | le panneau de configuration directx et les utilitaires de la visionneuse des fonctionnalités directx sont inclus dans le sous-répertoire d’architecture approprié dans le dossier bin du SDK Windows. La visionneuse des fonctionnalités DirectX est également disponible sur <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br /> | 
| <span id="XACT"></span><span id="xact"></span>XACT<br /> | L’outil de Cross-Platform audio (XACT) Xbox n’est plus pris en charge pour une utilisation sur Windows.<br /> | 
| <span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorateur de jeux</a> et GDFMAKER<br /> | L’API <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Games Explorer</a> présente les jeux aux utilisateurs de Windows. l’API Games Explorer est prise en charge uniquement sur Windows Vista et Windows 7. utilisez l’outil jeux de fichiers de définition de jeux (GDFMAKER.EXE) pour déclarer des évaluations de jeu pour les applications Windows store. <br /> l’outil jeu de fichiers de définition de jeu (GDFMaker.exe) est inclus dans le sous-répertoire x86 du dossier bin du SDK Windows et prend en charge les applications du Windows du windows Store et les applications de bureau Win32.<br /><br /> | 
| <span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Exemples<br /> | vous trouverez des exemples d’applications qui mettent en évidence directx 12 technologies sur Windows dans les <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">exemples DirectX</a> référentiel. La plupart des exemples de versions antérieures de Direct3D sont également disponibles en ligne. Pour plus d’informations sur ces exemples, consultez <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">catalogue des exemples du kit de développement logiciel (SDK) DirectX</a>.<br /> | 
| <span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1,1 géré<br /> | Les assemblys .NET DirectX sont déconseillés et ne sont pas recommandés pour une utilisation par les nouvelles applications. Plusieurs solutions sont disponibles. Consultez <a href="https://walbourn.github.io/directx-and-net/">DirectX et .net</a>. <br /> | 




 

Le kit de développement logiciel (SDK) DirectX hérité est disponible en téléchargement à partir du [Centre de téléchargement Microsoft](https://go.microsoft.com/fwlink/?LinkId=226640) , si nécessaire, mais il n’est pas recommandé d’utiliser pour les nouveaux projets.

> [!Note]  
> L’installation du kit de développement logiciel (SDK) DirectX échoue si vous disposez d’une certaine version du package redistribuable Visual C++ 2010 déjà installé. Pour plus d’informations sur et une solution pour résoudre ce problème, consultez [erreur « S1023 » lors de l’installation du kit de développement logiciel (SDK) DirectX (juin 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Utilisation de projets SDK DirectX avec Visual Studio

les exemples du kit de développement logiciel (SDK) DirectX de juin 2010 sont pris en charge avec les références sku premium Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 ou Microsoft Visual Studio Ultimate 2013) sur Windows 7 et les versions Windows 8 et ultérieures. en raison de la transition des en-têtes et des bibliothèques DirectX dans le SDK Windows, les modifications apportées aux paramètres du projet sont nécessaires à la création correcte de ces exemples avec la façon dont le kit de développement logiciel (SDK) Windows 8 et versions ultérieures sont empaquetés avec les références sku Visual Studio premium.

Ces étapes s’appliquent également à vos propres projets qui dépendent du kit de développement logiciel (SDK) DirectX.

1.  Assurez-vous que la version de juin 2010 du kit de développement logiciel DirectX est installée sur votre ordinateur de développement. si vous installez sur un ordinateur exécutant Windows 8 et versions ultérieures, vous êtes invité à activer .net 3,5 en tant qu’installation préalable au kit de développement logiciel (SDK) DirectX.

    > [!Note]  
    > L’installation du kit de développement logiciel (SDK) DirectX échoue si vous disposez d’une certaine version du package redistribuable Visual C++ 2010 déjà installé. Pour plus d’informations sur et une solution pour résoudre ce problème, consultez [erreur « S1023 » lors de l’installation du kit de développement logiciel (SDK) DirectX (juin 2010)](https://support.microsoft.com/kb/2728613).

     

2.  assurez-vous que vous utilisez l’une des références sku de Visual Studio premium. Microsoft Visual Studio Express 2012 pour Windows 8 ou Microsoft Visual Studio Express 2013 pour Windows ne générera pas d’applications de bureau Windows 8 et ultérieures comme les exemples du kit de développement logiciel (SDK) DirectX. pour installer l’une des références sku de la Visual Studio premium, accédez à : [Visual Studio downloads](https://www.microsoft.com/visualstudio/11/downloads) et suivez les instructions.

3.  Utilisez l’exemple de navigateur du kit de développement logiciel (SDK) DirectX pour installer les fichiers projet de l’exemple souhaité. ouvrez le fichier solution compatible Microsoft Visual Studio 2010 de l’exemple (avec le suffixe **\_ 2010**).

4.  si vous ouvrez l’exemple sur un système qui n’a Microsoft Visual Studio 2012 ou Microsoft Visual Studio 2013 installé, vous recevez le message suivant : «cette solution contient un ou plusieurs projets utilisant une version antérieure du compilateur et des bibliothèques de VC++. chaque projet peut être mis à jour pour utiliser le compilateur et les bibliothèques de VC++ (v110). Choisissez l’option **mettre à jour** dans cette boîte de dialogue pour effectuer la mise à jour avant d’ouvrir le projet.

    sinon, vous pouvez mettre à jour vers le Visual Studio 2012 ou Visual Studio 2013 compilateur et les bibliothèques C++ 11 après leur chargement en cliquant avec le bouton droit sur la solution et en sélectionnant **mettre à jour les projets VC++**.

5.  D3DX n’est pas considéré comme l’API canonique pour l’utilisation de Direct3D dans Windows 8 et versions ultérieures, et n’est donc pas inclus dans les SDK Windows correspondants. Examinez d’autres solutions pour travailler avec l’API Direct3D. pour les projets hérités, tels que les exemples du kit de développement logiciel (sdk) directx Windows 7 (et versions antérieures), les étapes suivantes sont nécessaires pour créer des applications avec D3DX à l’aide du kit de développement logiciel (sdk) directx :

    1.  modifiez les répertoires **VC++** du projet comme suit pour utiliser le bon ordre pour les en-têtes et les bibliothèques du kit de développement logiciel (SDK).

        <dl> i. ouvrez les **propriétés** du projet et sélectionnez la page **VC++ des répertoires** .  
        ii. Sélectionnez **toutes les configurations et toutes les plateformes**.  
        iii. Définissez ces répertoires comme suit :

        -   Répertoires exécutables : **<inherit from parent or project defaults>** (dans la liste déroulante de droite)
        -   Répertoires Include : **$ (INCLUDEPATH); $ (DXSDK \_ Rép) include**
        -   Inclure les répertoires **de bibliothèque : $ (LibraryPath); $ (DXSDK \_ Rép) lib \\ x86**

          
        iv. Cliquez sur **Appliquer**.  
        v. Choisissez la **plateforme x64**.  
        vi. Définissez le **Répertoire de bibliothèque** comme suit :

        -   Répertoires de bibliothèque : **$ (LibraryPath); $ (DXSDK \_ Rép) lib \\ x64**

          
        </dl>

    2.  À chaque fois que « d3dx9. h », « d3dx10. h » ou « d3dx11. h » sont inclus dans votre projet, veillez à inclure de manière explicite « d3d9. h », « d3d10. h » et « DXGI. h », ou « d3d11. h » et « DXGI. h » pour vous assurer que vous choisissez la version la plus récente. Vous pouvez désactiver l' **Avertissement C4005** si nécessaire. Toutefois, cet avertissement indique que vous utilisez la version antérieure de ces en-têtes.
    3.  Supprimez toutes les références à DXGIType. h dans votre projet. cet en-tête n’existe pas dans le SDK Windows, et la version du kit de développement logiciel (SDK) DirectX est en conflit avec le nouveau winerror. h.
    4.  Toutes les dll D3DX sont installées sur votre ordinateur de développement par l’installation du kit SDK DirectX. Assurez-vous que les dépendances D3DX nécessaires sont redistribuées avec n’importe quel exemple ou avec votre application si elle est déplacée vers un autre ordinateur.
    5.  N’oubliez pas que les technologies de remplacement pour les utilisations actuelles de D3DX11 incluent [DirectXTex](https://github.com/Microsoft/DirectXTex), [DirectXTK](https://github.com/Microsoft/DirectXTK), [DirectXMesh](https://github.com/Microsoft/DirectXMesh)et [UVAtlas](https://github.com/Microsoft/UVAtlas). D3DXMath est remplacé par [DirectXMath](./dxmath/directxmath-portal.md).

6.  Vérifiez que vous utilisez la nouvelle version du compilateur du nuanceur HLSL en observant les conditions suivantes :

    1.  la modification du répertoire exécutable à l’étape 5 entraîne l’utilisation par les builds de projet de FXC à partir de l’installation de SDK Windows. Sachez que les fichiers HLSL sont désormais officiellement reconnus par Visual Studio. Vous pouvez les ajouter en tant que fichiers projet et définir les options du compilateur dans le système de projet.

    2.  L’appel de la compilation au moment de l’exécution via la DLL D3DX héritée utilise la version antérieure incorrecte du compilateur HLSL. Remplacez toutes les références aux \* API D3DXCompile, D3DX10Compile \* et D3DX11Compile \* dans votre code par la fonction D3DCompile dans D3DCOMPILER \_46.DLL ou D3DCOMPILER \_47.DLL.

    3.  Les projets qui utilisent la compilation du nuanceur au moment de l’exécution doivent avoir D3DCOMPILER \_xx.DLL copiés dans le chemin d’accès de l’exécutable local pour le projet. cette DLL est disponible dans ce sous-répertoire du SDK Windows installation sous **% programfiles (x86)% \\ Windows kits \\ 8,0 \\ redist \\ d3d \\ &lt; arch &gt;** ou **% programfiles (x86)% \\ Windows kits \\ 8,1 \\ redist \\ d3d \\ &lt; arch &gt;** , où **&lt; arch &gt;** est **x86** et **x64**.

        le \_46.DLL D3DCOMPILER ou \_47.DLL D3DCOMPILER de la SDK Windows n’est pas un composant système et ne doit pas être copié dans le répertoire système de l’Windows. Vous pouvez redistribuer cette DLL à d’autres ordinateurs avec votre application en tant que DLL côte à côte.

7.  tout projet qui utilise l’API XInput et est conçu pour s’exécuter sur Windows 7 ou des versions antérieures de Windows devez utiliser la version héritée (9.1.0) ou doit inclure explicitement les en-têtes et les bibliothèques pour ce composant à partir du kit de développement logiciel (SDK) DirectX. En-tête XInput et XINPUT. LIB inclus dans le SDK Windows cible uniquement la version (1,4) fournie dans le cadre de Windows 8 et versions ultérieures. Le même en-tête peut être utilisé avec XINPUT9 \_ 1 \_ 0. lib pour utiliser la version héritée, qui est incluse dans les versions antérieures de Windows. La version héritée de XInput ne détecte pas les fonctionnalités complètes ou ne prend pas en charge le contrôleur audio intégré. par conséquent, si la prise en charge de ces fonctionnalités est nécessaire, vous devez utiliser la version du kit de développement logiciel (SDK) DirectX (1,3).

    Pour utiliser l’API XInput à l’échelle complète, vous devez utiliser `#include` les en-têtes XInput spécifiques du kit de développement logiciel (SDK) DirectX directement :

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... et dans les options de l’éditeur de liens pour les dépendances supplémentaires, liez directement à la bibliothèque XInput SDK DirectX :

    **% DXSDK \_ Rép% include \\ &lt; arch &gt; \\ XInput. lib**

    le XINPUT1 \_3.DLL binaire est installé dans les répertoires du système Windows par l’installation du kit de développement logiciel (SDK) DirectX sur votre ordinateur de développement. Vous devrez redistribuer ce fichier binaire avec votre application à l’aide de l’installation du programme d’installation de DirectX à partir du SDK DirectX.

8.  tout projet qui utilise l’API XAudio2 et est conçu pour s’exécuter sur Windows 7 ou des versions antérieures de Windows devez utiliser l’ancienne version (9.1.0) ou inclure explicitement les en-têtes et les bibliothèques de ce composant à partir du kit de développement logiciel (SDK) DirectX. les en-têtes et les bibliothèques XAudio2 inclus avec le SDK Windows ciblent uniquement la version (2,8) qui est incluse dans le cadre de Windows 8.

    Par exemple, avec XAudio2, vous devez utiliser `#include` les en-têtes XAudio2 spécifiques du kit de développement logiciel (SDK) DirectX directement :

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... et dans les options de l’éditeur de liens pour les dépendances supplémentaires, liez directement à la bibliothèque XAudio2 SDK DirectX :

    **% DXSDK \_ Rép% include \\ &lt; arch &gt; \\ xaudio2. lib**

    le XAUDIO2 \_7.DLL binaire est installé dans les répertoires du système Windows par l’installation du kit de développement logiciel (SDK) DirectX sur votre ordinateur de développement. Vous devez redistribuer ces bibliothèques avec votre application à l’aide de l’installation du programme d’installation de DirectX à partir du SDK DirectX.

9.  si vous avez utilisé le kit de développement logiciel (sdk) directx avec les versions antérieures de Visual Studio, la mise à niveau Visual Studio 2010 peut avoir migré le chemin d’accès du kit de développement logiciel (sdk) directx dans vos paramètres de projet par défaut. Il est recommandé de supprimer ces paramètres pour éviter les erreurs de génération ultérieures. dans le répertoire **% USERPROFILE% \\ AppData \\ Local \\ microsoft \\ MSBuild \\ v 4.0** , modifiez les fichiers **microsoft. cpp. Win32. user** et **microsoft. cpp. x64. user** pour supprimer toutes les références aux \_ chemins d’accès DXSDK DIR. Vous pouvez également supprimer l’intégralité du &lt; nœud PropertyGroup &gt; qui contient les entrées de chemin d’accès telles que &lt; ExecutablePath &gt; et &lt; INCLUDEPATH &gt; pour rétablir les valeurs par défaut standard. Si vous ne voyez pas de références à DXSDK \_ dir dans ces fichiers, aucune modification n’est nécessaire.

10. si l’application résultante prend en charge Windows Vista avec Service Pack 2 (SP2), ainsi que Windows 7 et Windows 8 et versions ultérieures, définissez la définition de préprocesseur nommée **\_ WIN32 \_ winnt** sur 0x600. s’il prend uniquement en charge Windows 7 et Windows 8 et versions ultérieures, affectez-lui la valeur 0x601.

    Par exemple :

    1.  Ouvrez les **Propriétés** du projet et sélectionnez préprocesseur **C/C++**  >  .
    2.  Sélectionnez **toutes les configurations** et **toutes les plateformes**.
    3.  Accédez à la section **définitions de préprocesseur** et définissez \_ Win32 \_ winnt = 0x600.
    4.  Cliquez sur **Appliquer**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Jeux pour Windows et kit de développement logiciel (SDK) DirectX**
</dt> <dt>

[Où se trouve le kit de développement logiciel (SDK) DirectX (édition 2021) ?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDK DirectX d’une certaine ancienneté](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Vivant sans D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
