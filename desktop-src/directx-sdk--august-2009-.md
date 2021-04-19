---
description: À compter de Windows 8, le kit de développement logiciel (SDK) DirectX est inclus dans le SDK Windows.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Où est le Kit de développement logiciel (SDK) DirectX ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c070313c5c7f6105afaf7b629ff1ca2618a469fb
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314622"
---
# <a name="where-is-the-directx-sdk"></a>Où est le Kit de développement logiciel (SDK) DirectX ?

À compter de Windows 8, le kit de développement logiciel (SDK) DirectX est inclus dans le SDK Windows.

Nous avons créé initialement le kit de développement logiciel (SDK) DirectX en tant que plateforme hautes performances pour le développement de jeux en plus de Windows. À mesure que les technologies DirectX évoluent, elles sont devenues pertinentes pour un plus grand nombre d’applications. Aujourd’hui, la disponibilité du matériel Direct3D sur les ordinateurs permet même aux applications bureautiques traditionnelles d’utiliser l’accélération matérielle graphique. En parallèle, les technologies DirectX sont plus intégrées à Windows. DirectX est désormais un composant fondamental de Windows.

Étant donné que le Kit de développement logiciel Windows constitue le principal outil des développeurs sous Windows, DirectX est désormais intégré. Vous pouvez à présent utiliser le Kit de développement logiciel Windows pour concevoir des jeux incroyables sous cette interface. Pour télécharger le kit de développement logiciel (SDK) Windows 8. x ou le SDK Windows 10, consultez [SDK Windows et l’archive d’émulateur](https://developer.microsoft.com/windows/downloads/sdk-archive).

Les technologies et les outils suivants, autrefois partie du kit de développement logiciel (SDK) DirectX, font désormais partie du SDK Windows.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Technologie ou outil</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Composants graphiques Windows<br/></td>
<td>Les en-têtes et les bibliothèques pour <a href="/windows/desktop/direct3d">Direct3D</a> et d’autres API graphiques Windows, comme <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, sont disponibles dans le SDK Windows. <br/>
<blockquote>
[!Note]<br />
Les bibliothèques d’utilitaires D3DX9/D3DX10/D3DX11 déconseillées sont disponibles via <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, mais il existe également un certain nombre d' <a href="https://walbourn.github.io/living-without-d3dx/">alternatives open source</a>. La bibliothèque d’utilitaires D3DCSX DirectCompute et la DLL redistribuable sont disponibles dans la SDK Windows. D3DX12 est disponible sur <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilateur HLSL (FXC.EXE)<br/></td>
<td>Le compilateur <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> est un outil du sous-répertoire d’architecture approprié dans le dossier bin du SDK Windows.<br/>
<blockquote>
[!Note]<br />
L’API D3DCompiler et la DLL redistribuable sont disponibles dans la SDK Windows.
</blockquote>
<br/><br/>Pour le développement DirectX 12, utilisez DXCompiler dans le SDK Windows et hébergé sur [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).
<br/></td>
</tr>
<tr class="odd">
<td><span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX pour Windows<br/></td>
<td>Un remplacement de l’outil PIX pour Windows est désormais une fonctionnalité de Microsoft Visual Studio, appelée débogueur graphique Visual Studio. Cette fonctionnalité a beaucoup amélioré la convivialité, la prise en charge de Windows 8 et de Direct3D 11,1 et l’intégration avec les fonctionnalités de Microsoft Visual Studio traditionnelles, telles que les piles d’appels et le débogage de Windows pour le débogage <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Pour plus d’informations sur cette nouvelle fonctionnalité, consultez <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">débogage DirectX Graphics</a>.<br/><br/>Pour le développement DirectX 12, consultez la dernière génération de <a href="https://devblogs.microsoft.com/pix/">pix sur Windows</a><br/></td>
</tr>
<tr class="even">
<td><span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> pour Windows<br/></td>
<td>L’API <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> est désormais un composant système dans Windows 8. x et Windows 10. Les en-têtes et les bibliothèques pour XAudio2 sont disponibles dans le SDK Windows. Pour la prise en charge de Windows 7, consultez <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> pour Windows<br/></td>
<td>L’API <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1,4 est désormais un composant système dans Windows 8. x et Windows 10. Les en-têtes et les bibliothèques pour XInput sont disponibles dans le SDK Windows.<br/>
<blockquote>
[!Note]<br />
Legacy XInput 9.1.0 est également disponible dans le cadre de Windows 7 ou version ultérieure.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br/></td>
<td>La version la plus récente de XNAMATH, qui est mise à jour pour les nouveaux jeux d’instructions et ARM/ARM64, est désormais <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>. Les en-têtes pour DirectXMath sont disponibles dans le SDK Windows et sur <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Visionneuse DirectX et fonctionnalités DirectX<br/></td>
<td>Le panneau de configuration DirectX et les utilitaires de la visionneuse des fonctionnalités DirectX sont inclus dans le sous-répertoire d’architecture approprié dans le dossier bin du SDK Windows. La visionneuse des fonctionnalités DirectX est également disponible sur <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="XACT"></span><span id="xact"></span>XACT<br/></td>
<td>L’outil de Cross-Platform audio (XACT) Xbox n’est plus pris en charge pour une utilisation sur Windows.<br/></td>
</tr>
<tr class="odd">
<td><span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorateur de jeux</a> et GDFMAKER<br/></td>
<td>L’API <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Games Explorer</a> présente des jeux aux utilisateurs de Windows. L’API Games Explorer est prise en charge uniquement sur Windows Vista et Windows 7. Utilisez l’outil jeux de fichiers de définition de jeux (GDFMAKER.EXE) pour déclarer des évaluations de jeu pour les applications du Windows Store. <br/> L’outil Game Definition File Maker Tool (GDFMaker.exe) est inclus dans le sous-répertoire x86 du dossier bin du SDK Windows et prend en charge les applications du Windows Store et les applications de bureau Win32.<br/>
<br/></td>
</tr>
<tr class="even">
<td><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Exemples<br/></td>
<td>Vous trouverez des exemples d’applications qui mettent en évidence DirectX 12 technologies sur Windows dans les <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">exemples DirectX</a> référentiel. La plupart des exemples de versions antérieures de Direct3D sont également disponibles en ligne. Pour plus d’informations sur ces exemples, consultez <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">catalogue des exemples du kit de développement logiciel (SDK) DirectX</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1,1 géré<br/></td>
<td>Les assemblys .NET DirectX sont déconseillés et ne sont pas recommandés pour une utilisation par les nouvelles applications. Plusieurs solutions sont disponibles. Consultez <a href="https://walbourn.github.io/directx-and-net/">DirectX et .net</a>. <br/></td>
</tr>
</tbody>
</table>



 

Le kit de développement logiciel (SDK) DirectX hérité est disponible en téléchargement à partir du [Centre de téléchargement Microsoft](https://go.microsoft.com/fwlink/?LinkId=226640) , si nécessaire, mais il n’est pas recommandé d’utiliser pour les nouveaux projets.

> [!Note]  
> L’installation du kit de développement logiciel (SDK) DirectX échoue si vous disposez d’une certaine version du package redistribuable Visual C++ 2010 déjà installé. Pour plus d’informations sur et une solution pour résoudre ce problème, consultez [erreur « S1023 » lors de l’installation du kit de développement logiciel (SDK) DirectX (juin 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Utilisation de projets SDK DirectX avec Visual Studio

Les exemples du kit de développement logiciel (SDK) DirectX de juin 2010 sont pris en charge avec les références SKU Visual Studio Premium (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 ou Microsoft Visual Studio Ultimate 2013) sur Windows 7 et Windows 8 et versions ultérieures. En raison de la transition des en-têtes et des bibliothèques DirectX dans le SDK Windows, les modifications apportées aux paramètres du projet sont nécessaires à la création correcte de ces exemples avec les références SKU Visual Studio Premium.

Ces étapes s’appliquent également à vos propres projets qui dépendent du kit de développement logiciel (SDK) DirectX.

1.  Assurez-vous que la version de juin 2010 du kit de développement logiciel DirectX est installée sur votre ordinateur de développement. Si vous installez sur un ordinateur exécutant Windows 8 et versions ultérieures, vous êtes invité à activer .NET 3,5 en tant qu’installation requise pour le kit de développement logiciel (SDK) DirectX.

    > [!Note]  
    > L’installation du kit de développement logiciel (SDK) DirectX échoue si vous disposez d’une certaine version du package redistribuable Visual C++ 2010 déjà installé. Pour plus d’informations sur et une solution pour résoudre ce problème, consultez [erreur « S1023 » lors de l’installation du kit de développement logiciel (SDK) DirectX (juin 2010)](https://support.microsoft.com/kb/2728613).

     

2.  Assurez-vous que vous utilisez l’une des références SKU Visual Studio Premium. Microsoft Visual Studio Express 2012 pour Windows 8 ou Microsoft Visual Studio Express 2013 pour Windows ne générera pas les applications de bureau Windows 8 et versions ultérieures, telles que les exemples du kit de développement logiciel (SDK) DirectX. Pour installer l’une des références SKU Visual Studio Premium, accédez à : [téléchargements Visual Studio](https://www.microsoft.com/visualstudio/11/downloads) et suivez les instructions.

3.  Utilisez l’exemple de navigateur du kit de développement logiciel (SDK) DirectX pour installer les fichiers projet de l’exemple souhaité. Ouvrez le fichier solution compatible Microsoft Visual Studio 2010 de l’exemple (avec le suffixe **\_ 2010**).

4.  Si vous ouvrez l’exemple sur un système qui n’a Microsoft Visual Studio 2012 ou Microsoft Visual Studio 2013 installé, vous recevez le message suivant : «cette solution contient un ou plusieurs projets utilisant une version antérieure du compilateur et des bibliothèques VC + +. Chaque projet peut être mis à jour pour utiliser le compilateur et les bibliothèques VC + + (v110). Choisissez l’option **mettre à jour** dans cette boîte de dialogue pour effectuer la mise à jour avant d’ouvrir le projet.

    Dans le cas contraire, vous pouvez mettre à jour le compilateur Visual Studio 2012 ou Visual Studio 2013 C++ 11 et les bibliothèques après leur chargement en cliquant avec le bouton droit sur la solution et en sélectionnant **mettre à jour les projets VC + +**.

5.  D3DX n’est pas considéré comme l’API canonique pour l’utilisation de Direct3D dans Windows 8 et versions ultérieures et n’est donc pas inclus avec les SDK Windows correspondants. Examinez d’autres solutions pour travailler avec l’API Direct3D. Pour les projets hérités, tels que les exemples du kit de développement logiciel (SDK) DirectX Windows 7 (et versions antérieures), les étapes suivantes sont nécessaires pour créer des applications avec D3DX à l’aide du kit de développement logiciel (SDK) DirectX :

    1.  Modifiez les répertoires **VC + +** du projet comme suit pour utiliser le bon ordre pour les en-têtes et les bibliothèques du kit de développement logiciel (SDK).

        <dl> i. Ouvrez les **Propriétés** du projet, puis sélectionnez la page **Répertoires VC + +** .  
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
    3.  Supprimez toutes les références à DXGIType. h dans votre projet. Cet en-tête n’existe pas dans le SDK Windows, et la version du kit de développement logiciel (SDK) DirectX est en conflit avec le nouveau winerror. h.
    4.  Toutes les dll D3DX sont installées sur votre ordinateur de développement par l’installation du kit SDK DirectX. Assurez-vous que les dépendances D3DX nécessaires sont redistribuées avec n’importe quel exemple ou avec votre application si elle est déplacée vers un autre ordinateur.
    5.  N’oubliez pas que les technologies de remplacement pour les utilisations actuelles de D3DX11 incluent [DirectXTex](https://github.com/Microsoft/DirectXTex), [DirectXTK](https://github.com/Microsoft/DirectXTK), [DirectXMesh](https://github.com/Microsoft/DirectXMesh)et [UVAtlas](https://github.com/Microsoft/UVAtlas). D3DXMath est remplacé par [DirectXMath](./dxmath/directxmath-portal.md).

6.  Vérifiez que vous utilisez la nouvelle version du compilateur du nuanceur HLSL en observant les conditions suivantes :

    1.  La modification du répertoire exécutable à l’étape 5 entraîne l’utilisation par les builds de projet de FXC à partir de l’installation de SDK Windows. Sachez que les fichiers HLSL sont désormais officiellement reconnus par Visual Studio. Vous pouvez les ajouter en tant que fichiers projet et définir les options du compilateur dans le système de projet.

    2.  L’appel de la compilation au moment de l’exécution via la DLL D3DX héritée utilise la version antérieure incorrecte du compilateur HLSL. Remplacez toutes les références aux \* API D3DXCompile, D3DX10Compile \* et D3DX11Compile \* dans votre code par la fonction D3DCompile dans D3DCOMPILER \_46.DLL ou D3DCOMPILER \_47.DLL.

    3.  Les projets qui utilisent la compilation du nuanceur au moment de l’exécution doivent avoir D3DCOMPILER \_xx.DLL copiés dans le chemin d’accès de l’exécutable local pour le projet. Cette dll est disponible dans ce sous-répertoire du SDK Windows installation sous **% ProgramFiles (x86)% \\ Windows kits \\ 8,0 \\ Redist \\ D3D \\ <arch>** ou **% ProgramFiles (x86)% \\ Windows kits \\ 8,1 \\ Redist \\ D3D \\ <arch>** , où **<arch>** est **x86** et **x64**.

        Le \_46.DLL D3DCOMPILER ou \_47.DLL D3DCOMPILER de la SDK Windows n’est pas un composant système et ne doit pas être copié dans le répertoire système de Windows. Vous pouvez redistribuer cette DLL à d’autres ordinateurs avec votre application en tant que DLL côte à côte.

7.  Tout projet qui utilise l’API XInput et qui est destiné à s’exécuter sur Windows 7 ou des versions antérieures de Windows doit utiliser la version héritée (9.1.0) ou doit inclure explicitement les en-têtes et les bibliothèques pour ce composant à partir du kit de développement logiciel (SDK) DirectX. En-tête XInput et XINPUT. LIB inclus dans le SDK Windows cible uniquement la version (1,4) fournie dans le cadre de Windows 8 et versions ultérieures. Le même en-tête peut être utilisé avec XINPUT9 \_ 1 \_ 0. lib pour utiliser la version héritée, qui est incluse dans les versions antérieures de Windows. La version héritée de XInput ne détecte pas les fonctionnalités complètes ou ne prend pas en charge le contrôleur audio intégré. par conséquent, si la prise en charge de ces fonctionnalités est nécessaire, vous devez utiliser la version du kit de développement logiciel (SDK) DirectX (1,3).

    Pour utiliser l’API XInput à l’échelle complète, vous devez utiliser `#include` les en-têtes XInput spécifiques du kit de développement logiciel (SDK) DirectX directement :

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... et dans les options de l’éditeur de liens pour les dépendances supplémentaires, liez directement à la bibliothèque XInput SDK DirectX :

    **% DXSDK \_ Rép% include \\ <arch> \\ XInput. lib**

    Le XINPUT1 \_3.DLL binaire est installé dans les répertoires système Windows par l’installation du kit de développement logiciel (SDK) DirectX sur votre ordinateur de développement. Vous devrez redistribuer ce fichier binaire avec votre application à l’aide de l’installation du programme d’installation de DirectX à partir du SDK DirectX.

8.  Tout projet qui utilise l’API XAudio2 et qui est destiné à s’exécuter sur Windows 7 ou des versions antérieures de Windows doit utiliser l’ancienne version (9.1.0) ou inclure explicitement les en-têtes et les bibliothèques de ce composant à partir du kit de développement logiciel (SDK) DirectX. Les en-têtes et les bibliothèques XAudio2 inclus avec le SDK Windows ciblent uniquement la version (2,8) incluse dans le cadre de Windows 8.

    Par exemple, avec XAudio2, vous devez utiliser `#include` les en-têtes XAudio2 spécifiques du kit de développement logiciel (SDK) DirectX directement :

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... et dans les options de l’éditeur de liens pour les dépendances supplémentaires, liez directement à la bibliothèque XAudio2 SDK DirectX :

    **% DXSDK \_ Rép% include \\ <arch> \\ xaudio2. lib**

    Le XAUDIO2 \_7.DLL binaire est installé dans les répertoires système Windows par l’installation du kit de développement logiciel (SDK) DirectX sur votre ordinateur de développement. Vous devez redistribuer ces bibliothèques avec votre application à l’aide de l’installation du programme d’installation de DirectX à partir du SDK DirectX.

9.  Si vous avez utilisé le kit de développement logiciel (SDK) DirectX avec les versions antérieures de Visual Studio, la mise à niveau de Visual Studio 2010 peut avoir migré le chemin du kit de développement logiciel (SDK) DirectX dans vos paramètres de projet par défaut. Il est recommandé de supprimer ces paramètres pour éviter les erreurs de génération ultérieures. Dans le répertoire **% UserProfile% \\ AppData \\ local \\ Microsoft \\ MSBuild \\ v 4.0** , modifiez les fichiers **Microsoft. cpp. Win32. User** et **Microsoft. cpp. x64. User** pour supprimer toutes les références aux \_ chemins d’accès DXSDK dir. Vous pouvez également supprimer l’intégralité du <PropertyGroup> nœud qui contient les entrées de chemin d’accès telles que <ExecutablePath> et <IncludePath> pour rétablir les valeurs par défaut standard. Si vous ne voyez pas de références à DXSDK \_ dir dans ces fichiers, aucune modification n’est nécessaire.

10. Si l’application résultante prend en charge Windows Vista avec Service Pack 2 (SP2), ainsi que Windows 7 et Windows 8 et versions ultérieures, définissez la définition de préprocesseur nommée **\_ Win32 \_ winnt** sur 0x600. S’il prend uniquement en charge Windows 7 et Windows 8 et versions ultérieures, affectez-lui la valeur 0x601.

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
