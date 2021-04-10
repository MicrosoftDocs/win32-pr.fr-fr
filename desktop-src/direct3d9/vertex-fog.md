---
description: Lorsque le système exécute un sommet, il applique des calculs de brouillard à chaque vertex d’un polygone, puis interpole les résultats sur la face du polygone pendant la pixellisation.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Brouillard du vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108391"
---
# <a name="vertex-fog-direct3d-9"></a>Brouillard du vertex (Direct3D 9)

Lorsque le système exécute un sommet, il applique des calculs de brouillard à chaque vertex d’un polygone, puis interpole les résultats sur la face du polygone pendant la pixellisation. Les effets de brouillard du vertex sont calculés par le moteur de transformation et l’éclairage Direct3D. Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md).

Si votre application n’utilise pas Direct3D pour la transformation et l’éclairage, l’application doit effectuer des calculs de brouillard. Dans ce cas, placez le facteur de brouillard calculé dans le composant alpha de la couleur spéculaire pour chaque vertex. Vous êtes libre d’utiliser les formules que vous souhaitez, volumétriques ou autres. Direct3D utilise le facteur de brouillard fourni pour effectuer une interpolation sur la face de chaque polygone. Les applications qui effectuent leur propre transformation et éclairage doivent également effectuer leurs propres calculs de brouillard de vertex. Par conséquent, une telle application a besoin uniquement d’activer la fusion de brouillard et de définir la couleur du brouillard via les États de rendu associés, comme décrit dans [mélange de brouillards (Direct3D 9)](fog-blending.md) et [couleur de brouillard (Direct3D 9)](fog-color.md).

> [!Note]  
> Quand vous utilisez un nuanceur de sommets, vous devez utiliser le brouillard de vertex. Pour ce faire, utilisez le nuanceur de sommets pour écrire l’intensité de brouillard par vertex dans le registre oFog. Une fois le nuanceur de pixels terminé, les données oFog sont utilisées pour effectuer une interpolation linéaire avec la couleur de brouillard. Cette intensité n’est pas disponible dans un nuanceur de pixels.

 

## <a name="range-based-fog"></a>Brouillard Range-Based

> [!Note]  
> Direct3D utilise des calculs de brouillard basés sur une plage uniquement lors de l’utilisation du brouillard de vertex avec la transformation et le moteur d’éclairage Direct3D. Cela est dû au fait que le brouillard de pixel est implémenté dans le pilote de périphérique et qu’il n’existe pas de matériel pour prendre en charge le brouillard basé sur une plage par pixel. Si votre application effectue sa propre transformation et éclairage, elle doit effectuer ses propres calculs de brouillard, en fonction de la plage ou dans le cas contraire.

 

Parfois, l’utilisation de brouillard peut introduire des artefacts graphiques qui entraînent la fusion des objets avec la couleur de brouillard de manière peu intuitive. Par exemple, Imaginez une scène dans laquelle il y a deux objets visibles : un qui est suffisamment éloigné pour être affecté par le brouillard, et l’autre presque suffisamment pour ne pas être affecté. Si la zone d’affichage pivote sur place, les effets de brouillard apparent peuvent changer, même si les objets sont stationnaires. Le diagramme suivant montre une vue verticale d’une telle situation.

![diagramme de deux points de vue et de la façon dont ils affectent le brouillard pour deux objets](images/artifog.png)

Le brouillard basé sur une plage est un moyen plus précis et plus précis de déterminer les effets de brouillard. Dans le brouillard basé sur une plage, Direct3D utilise la distance réelle entre le point de vue et un vertex pour ses calculs de brouillard. Direct3D augmente l’effet du brouillard au fur et à mesure que la distance entre les deux points augmente, plutôt que la profondeur du vertex dans la scène, évitant ainsi les artefacts de rotation.

Si l’appareil actuel prend en charge le brouillard basé sur une plage, il définit la \_ valeur FOGRANGE D3DPRASTERCAPS dans le membre RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) lorsque vous appelez la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . Pour activer le brouillard basé sur une plage, définissez l' \_ État de rendu D3DRS RANGEFOGENABLE sur **true**.

Le brouillard basé sur une plage est calculé par Direct3D pendant la transformation et l’éclairage. Les applications qui n’utilisent pas la transformation et le moteur d’éclairage Direct3D doivent également effectuer leurs propres calculs de brouillard de vertex. Dans ce cas, fournissez le facteur de brouillard basé sur une plage dans le composant alpha du composant spéculaire pour chaque vertex.

## <a name="using-vertex-fog"></a>Utilisation du brouillard du vertex

Utilisez les étapes suivantes pour activer le brouillard de vertex dans votre application.

1.  Activez la fusion de brouillard en affectant \_ à D3DRS FOGENABLE la **valeur true**.
2.  Définissez la couleur de brouillard dans l' \_ État de rendu D3DRS FOGCOLOR.
3.  Choisissez la formule de brouillard souhaitée en affectant \_ à l’état de rendu D3DRS FOGVERTEXMODE la valeur d’un membre du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Définissez les paramètres de brouillard comme vous le souhaitez pour la formule de brouillard sélectionnée dans les États de rendu.

L’exemple suivant, écrit en C++, illustre ce que ces étapes peuvent ressembler dans le code.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



Certains paramètres de brouillard sont requis comme valeurs à virgule flottante, même si la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte uniquement des valeurs DWORD dans le deuxième paramètre. Cet exemple fournit correctement les valeurs à virgule flottante à ces méthodes sans traduction de données en effectuant un cast des adresses des variables à virgule flottante en tant que pointeurs DWORD, puis en les déréférençant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de brouillard](fog-types.md)
</dt> </dl>

 

 
