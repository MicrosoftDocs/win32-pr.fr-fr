---
description: Les matériaux décrivent comment les polygones reflètent la lumière ou apparaissent pour émettre de la lumière dans une scène 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Matériaux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8140de30243c7a0f7290715da3d0720cd15cea769bd78cbf66893c0082062d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092949"
---
# <a name="materials-direct3d-9"></a>Matériaux (Direct3D 9)

Les matériaux décrivent comment les polygones reflètent la lumière ou apparaissent pour émettre de la lumière dans une scène 3D. Les propriétés de matériau détaillent la réflexion diffuse d’un matériau, la réflexion ambiante, les émissions légères et les caractéristiques de surbrillance spéculaire. Direct3D utilise la structure [**D3DMATERIAL9**](d3dmaterial9.md) pour transporter toutes les informations de propriété de matériau. À l’exception de la propriété spéculaire, chaque propriété est décrite comme une couleur RVBA qui représente la proportion des parties rouge, verte et bleue d’un type de lumière donné qu’elle reflète et un facteur de fusion alpha.

## <a name="diffuse-and-ambient-reflection"></a>Réflexion diffuse et ambiante

Les membres diffus et ambiant de la structure [**D3DMATERIAL9**](d3dmaterial9.md) décrivent comment un matériau reflète la lumière ambiante et diffuse dans une scène. Étant donné que la plupart des scènes contiennent bien plus de lumière diffuse que la lumière ambiante, la réflexion diffuse joue la plus grande partie de la détermination de la couleur. En outre, étant donné que la lumière diffuse est directionnelle, l’angle d’incidence pour la lumière diffuse affecte l’intensité globale de la réflexion. La réflexion diffuse est la plus grande lorsque la lumière fait apparaître un sommet parallèlement à la normale du vertex. À mesure que l’angle augmente, l’effet de la réflexion diffuse diminue. La quantité de lumière réfléchie est le cosinus de l’angle entre la lumière entrante et le vertex normal, comme indiqué dans l’illustration suivante.

![illustration de la quantité de lumière réfléchie](images/incident.png)

La réflexion ambiante, comme la lumière ambiante, est non directionnelle. La réflexion ambiante a un impact moindre sur la couleur apparente d’un objet rendu, mais elle affecte la couleur globale et est plus perceptible lorsque la lumière diffuse est minime ou non. La réflexion ambiante d’un matériau est affectée par la lumière ambiante définie pour une scène en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec l' \_ indicateur ambiant D3DRS.

La réflexion diffuse et ambiante fonctionne ensemble pour déterminer la couleur perçue d’un objet et sont généralement des valeurs identiques. Par exemple, pour restituer un objet cristallin bleu, vous créez un matériau qui reflète uniquement le composant bleu de diffusion et de lumière ambiante. Lorsqu’il est placé dans une pièce avec une lumière blanche, le cristal semble être bleu. Toutefois, dans une salle qui a uniquement une lumière rouge, le même cristal semble être noir, car son matériau ne reflète pas la lumière rouge.

## <a name="emission"></a>Émission

Les matériaux peuvent être utilisés pour qu’un objet rendu semble être auto-lumineux. Le membre émissif de la structure [**D3DMATERIAL9**](d3dmaterial9.md) est utilisé pour décrire la couleur et la transparence de la lumière émise. L’émission affecte la couleur d’un objet et peut, par exemple, rendre un matériau sombre plus clair et prendre en partie la couleur émise.

Vous pouvez utiliser la propriété émissif d’un matériau pour ajouter l’illusion qu’un objet émet de la lumière, sans impliquer la surcharge de calcul de l’ajout d’une lumière à la scène. Dans le cas du cristal bleu, la propriété émissif est utile si vous souhaitez que le cristal semble allumé, mais pas pour les autres objets de la scène. N’oubliez pas que les matériaux avec des propriétés émissif n’émettent pas de lumière qui peuvent être reflétées par d’autres objets dans une scène. Pour obtenir cette lumière réfléchie, vous devez placer une lumière supplémentaire dans la scène.

## <a name="specular-reflection"></a>Réflexion spéculaire

La réflexion spéculaire crée des surbrillances sur les objets, ce qui les rend brillants. La structure [**D3DMATERIAL9**](d3dmaterial9.md) contient deux membres qui décrivent la couleur de surbrillance spéculaire ainsi que la brillance globale du matériau. Vous établissez la couleur des surbrillances spéculaires en définissant le membre spéculaire sur la couleur RVBA souhaitée. les couleurs les plus courantes sont blanches ou gris clair. Les valeurs que vous définissez dans le contrôle des membres d’alimentation déterminent la netteté des effets spéculaires.

Les surbrillances spéculaires peuvent créer des effets spectaculaires. Dessin à nouveau sur l’analogie monocristal bleue : une valeur de puissance plus grande crée des surbrillances spéculaires plus nettes, ce qui rend le cristal très brillant. Des valeurs plus petites augmentent la zone de l’effet, créant une réflexion terne qui rend l’apparence cristalline. Pour rendre un objet véritablement mat, définissez le membre d’alimentation sur zéro et la couleur de l’éclairage spéculaire sur noir. Faites des essais avec différents niveaux de réflexion pour produire une apparence réaliste pour vos besoins. L’illustration suivante montre deux modèles identiques. Celui de gauche utilise une puissance de réflexion spéculaire de 10 ; le modèle de droite n’a pas de réflexion spéculaire.

![illustration des modèles de réflexion spéculaire](images/spechigh.png)

## <a name="setting-material-properties"></a>Définition des propriétés d’un matériau

Les appareils de rendu Direct3D peuvent effectuer un rendu avec un ensemble de propriétés de matériau à la fois.

Dans une application C++, vous définissez les propriétés de matériau que le système utilise en préparant une structure [**D3DMATERIAL9**](d3dmaterial9.md) , puis en appelant la méthode [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .

Pour préparer l’utilisation de la structure [**D3DMATERIAL9**](d3dmaterial9.md) , définissez les informations de propriété dans la structure pour créer l’effet souhaité pendant le rendu. L’exemple de code suivant configure la structure **D3DMATERIAL9** pour un matériau violet avec des surbrillances spéculaires blanches nettes.


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



Après la préparation de la structure [**D3DMATERIAL9**](d3dmaterial9.md) , vous appliquez les propriétés en appelant la méthode [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) du périphérique de rendu. Cette méthode accepte l’adresse d’une structure **D3DMATERIAL9** préparée comme son seul paramètre. Vous pouvez appeler **IDirect3DDevice9 :: SetMaterial** avec de nouvelles informations en fonction des besoins pour mettre à jour les propriétés de matériau de l’appareil. L’exemple de code suivant montre comment cela peut s’afficher dans le code.


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



Lorsque vous créez un appareil Direct3D, le matériel actuel est automatiquement défini sur la valeur par défaut indiquée dans le tableau suivant.



| Membre   | Valeur                |
|----------|----------------------|
| Diffus  | (R:0, G:0, B:0, A:0) |
| Spéculaire | (R:0, G:0, B:0, A:0) |
| Ambiant  | (R:0, G:0, B:0, A:0) |
| Émissif | (R:0, G:0, B:0, A:0) |
| Alimentation    | (0,0)                |



 

## <a name="retrieving-material-properties"></a>Récupération des propriétés de matériel

Vous récupérez les propriétés de matériau que l’appareil de rendu utilise actuellement en appelant la méthode [**IDirect3DDevice9 :: GetMaterial**](/windows/desktop/api) pour l’appareil. Contrairement à la méthode [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9 :: GetMaterial** ne requiert pas de préparation. La méthode **IDirect3DDevice9 :: GetMaterial** accepte l’adresse d’une structure [**D3DMATERIAL9**](d3dmaterial9.md) et remplit la structure fournie avec les informations qui décrivent les propriétés de matière actuelles avant de retourner.


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> Si votre application ne spécifie pas de propriétés de matériau pour le rendu, le système utilise un matériau par défaut. La matière par défaut reflète tout le clair diffus, par exemple, sans réflexion ambiante ou spéculaire, et sans couleur émissif.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lumières et matériaux](lights-and-materials.md)
</dt> </dl>

 

 
