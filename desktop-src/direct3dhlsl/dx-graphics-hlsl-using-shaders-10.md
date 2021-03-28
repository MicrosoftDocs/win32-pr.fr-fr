---
title: Utilisation des nuanceurs dans Direct3D 10
description: Utilisation des nuanceurs dans Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315180"
---
# <a name="using-shaders-in-direct3d-10"></a>Utilisation des nuanceurs dans Direct3D 10

Le pipeline a trois étapes de nuanceur et chacune d’entre elles est programmée avec un nuanceur HLSL. Tous les nuanceurs Direct3D 10 sont écrits en HLSL, ciblant le nuanceur modèle 4.



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 10 :<br/> Contrairement aux modèles de nuanceur Direct3D 9 qui peuvent être créés dans un langage assembleur intermédiaire, les nuanceurs de modèle de nuanceur 4,0 sont uniquement créés en HLSL. La compilation hors connexion des nuanceurs dans le bytecode consommable par l’appareil est toujours prise en charge et recommandée pour la plupart des scénarios.<br/> |



 

Cet exemple utilise uniquement un nuanceur de sommets. Étant donné que tous les nuanceurs sont générés à partir du Common Shader Core, l’utilisation d’un nuanceur vertex est très similaire à l’utilisation d’une géométrie ou d’un nuanceur de pixels.

Une fois que vous avez créé un nuanceur HLSL (cet exemple utilise le nuanceur de vertex HLSLWithoutFX. vsh), vous devez le préparer pour l’étape de pipeline qui l’utilisera. Pour ce faire, vous devez :

-   [Compiler un nuanceur](#compile-a-shader)
-   [Créer un objet Shader](#create-a-shader-object)
-   [Définir l’objet Shader](#set-the-shader-object)
-   [Répéter pour les 3 étapes de nuanceur](#repeat-for-all-3-shader-stages)

Ces étapes doivent être répétées pour chaque nuanceur dans le pipeline.

## <a name="compile-a-shader"></a>Compiler un nuanceur

La première étape consiste à compiler le nuanceur, afin de vérifier que vous avez correctement codé les instructions HLSL. Pour ce faire, appelez D3D10CompileShader et fournissez-lui plusieurs paramètres, comme indiqué ci-dessous :


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Cette fonction accepte les paramètres suivants :

-   Nom du fichier (et longueur de la chaîne de nom en octets) qui contient le nuanceur. Cet exemple utilise un nuanceur de sommets uniquement (dans le fichier HLSLWithoutFX. vsh dans lequel l’extension de fichier. vsh est l’abréviation de vertex shader).
-   Nom de la fonction de nuanceur. Cet exemple compile un nuanceur de sommets à partir de la fonction ondulation qui prend une seule entrée et retourne un struct de sortie (la fonction provient de l’exemple HLSLWithoutFX) :
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Pointeur vers toutes les macros utilisées par le nuanceur. Utilisez \_ \_ la macro D3D10 Shader pour faciliter la définition de vos macros. créez simplement une chaîne de nom qui contient tous les noms de macros (chaque nom étant séparé par un espace) et une chaîne de définition (chaque corps de macro étant séparé par un espace). Les deux chaînes doivent se terminer par une valeur NULL.
-   Pointeur vers les autres fichiers dont vous avez besoin pour que vos nuanceurs soient compilés. Utilise l’interface ID3D10Include qui a deux méthodes implémentées par l’utilisateur : Open et Close. Pour que cela fonctionne, vous devez implémenter le corps des méthodes Open et Close. dans la méthode Open, ajoutez le code que vous utiliseriez pour ouvrir les fichiers include de votre choix. dans la fonction Close, ajoutez le code pour fermer les fichiers lorsque vous n’en avez plus besoin.
-   Nom de la fonction de nuanceur à compiler. Ce nuanceur compile la fonction ondulation.
-   Profil de nuanceur à cibler lors de la compilation. Étant donné que vous pouvez compiler une fonction en un vertex, une géométrie ou un nuanceur de pixels, le profil indique au compilateur le type de nuanceur et le modèle de nuanceur à comparer au code.
-   Indicateurs du compilateur du nuanceur. Ces indicateurs indiquent au compilateur les informations à placer dans la sortie compilée et la manière dont vous souhaitez optimiser le code de sortie : pour la vitesse, pour le débogage, etc. Pour obtenir la liste des indicateurs disponibles, consultez [constantes Effect (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) . L’exemple contient du code que vous pouvez utiliser pour définir les valeurs de l’indicateur de compilateur pour votre projet. il s’agit principalement d’une question indiquant si vous souhaitez ou non générer des informations de débogage.
-   Pointeur vers la mémoire tampon qui contient le code de nuanceur compilé. La mémoire tampon contient également les informations de débogage et de table de symboles incorporées demandées par les indicateurs du compilateur.
-   Pointeur vers une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation, qui sont les mêmes messages que ceux que vous pouvez voir dans la sortie de débogage si vous exécutiez le débogueur lors de la compilation du nuanceur. **Null** est une valeur acceptable lorsque vous ne voulez pas que les erreurs soient retournées à une mémoire tampon.

Si le nuanceur se compile correctement, un pointeur vers le code du nuanceur est retourné en tant qu’interface ID3D10Blob. Il s’agit de l’interface d’objet BLOB, car le pointeur se trouve à un emplacement dans la mémoire qui est constitué d’un tableau de DWORD. L’interface est fournie afin que vous puissiez obtenir un pointeur vers le nuanceur compilé dont vous aurez besoin à l’étape suivante.

À partir du kit de développement logiciel (SDK) 2006 du mois de décembre, le compilateur HLSL DirectX 10 est désormais le compilateur par défaut dans DirectX 9 et DirectX 10. Pour plus d’informations [, consultez outil de compilateur Effect](/windows/desktop/direct3dtools/fxc) .

### <a name="get-a-pointer-to-a-compiled-shader"></a>Obtenir un pointeur vers un nuanceur compilé

Plusieurs méthodes d’API requièrent un pointeur vers un nuanceur compilé. Cet argument est généralement appelé *pShaderBytecode* , car il pointe vers un nuanceur compilé représenté sous la forme d’une séquence de codes d’octet. Pour obtenir un pointeur vers un nuanceur compilé, commencez par compiler le nuanceur en appelant [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) ou une fonction similaire. Si la compilation réussit, le nuanceur compilé est retourné dans une interface [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) . Enfin, utilisez la méthode [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) pour retourner le pointeur.

## <a name="create-a-shader-object"></a>Créer un objet Shader

Une fois le nuanceur compilé, appelez CreateVertexShader pour créer l’objet de nuanceur :


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Pour créer l’objet Shader, transmettez le pointeur au nuanceur compilé dans CreateVertexShader. Dans la mesure où vous deviez tout d’abord compiler le nuanceur, cet appel sera presque certainement réussi, sauf si vous rencontrez un problème de mémoire sur votre ordinateur.

Vous pouvez créer autant d’objets de nuanceur que vous le souhaitez et y conserver simplement des pointeurs. Ce même mécanisme fonctionne pour les nuanceurs de géométrie et de pixels, en supposant que vous faites correspondre les profils de nuanceur (lorsque vous appelez la méthode Compile) aux noms d’interface (lorsque vous appelez la méthode Create).

## <a name="set-the-shader-object"></a>Définir l’objet Shader

La dernière étape consiste à définir le nuanceur sur l’étape de pipeline. Comme il existe trois étapes de nuanceur dans le pipeline, vous devrez effectuer trois appels d’API, un pour chaque étape.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



L’appel à VSSetShader prend le pointeur vers le nuanceur de sommets créé à l’étape 1. Cela définit le nuanceur dans l’appareil. L’étape du nuanceur de sommets est maintenant initialisée avec son code de nuanceur vertex, tout ce qui reste est l’initialisation des variables de nuanceur.

## <a name="repeat-for-all-3-shader-stages"></a>Répéter pour les 3 étapes de nuanceur

Répétez ces mêmes étapes pour créer un nuanceur de vertex ou de pixels, voire un nuanceur de géométrie qui génère le nuanceur de pixels.

## <a name="related-topics"></a>Rubriques connexes

[Compilation des nuanceurs](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

