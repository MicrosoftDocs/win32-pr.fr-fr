---
description: Les objets de mémoire tampon de vertex permettent aux applications d’accéder directement à la mémoire allouée pour les données de vertex.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Accès au contenu d’une mémoire tampon de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f186a85ae0f025d274c50a62d2a83e943bc3b772b2907b5baa1bcac6e0b3bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987469"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a>Accès au contenu d’une mémoire tampon de vertex (Direct3D 9)

Les objets de mémoire tampon de vertex permettent aux applications d’accéder directement à la mémoire allouée pour les données de vertex. Vous pouvez récupérer un pointeur vers la mémoire tampon de vertex en appelant la méthode [**IDirect3DVertexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) , puis en accédant à la mémoire si nécessaire pour remplir la mémoire tampon avec les nouvelles données de vertex ou pour lire les données qu’elle contient déjà. La méthode **IDirect3DVertexBuffer9 :: Lock** accepte quatre paramètres. Le premier, *OffsetToLock*, est le décalage dans les données de vertex. Le deuxième paramètre est la taille, exprimée en octets, des données de vertex. Le troisième paramètre accepté est l’adresse d’un pointeur qui pointe vers les données de vertex, si l’appel est concluant.

Le dernier paramètre, *Flags*, indique au système la manière dont la mémoire doit être verrouillée. Spécifiez les constantes pour le paramètre *Flags* en fonction de la façon dont les données du vertex sont accessibles. Assurez-vous que la valeur choisie pour [**D3DUSAGE**](d3dusage.md) correspond à la valeur choisie pour [D3DLOCK](d3dlock.md). Par exemple, si vous créez une mémoire tampon de vertex avec accès en écriture uniquement, il n’est pas judicieux d’essayer de lire les données en spécifiant D3DLOCK \_ ReadOnly. En utilisant judicieusement ces indicateurs, le pilote peut verrouiller la mémoire et fournir les meilleures performances, en fonction du type d’accès demandé.

Une fois que vous avez fini de remplir ou de lire les données de vertex, appelez la méthode [**IDirect3DVertexBuffer9 :: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , comme indiqué dans l’exemple de code suivant.


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



Si vous créez une mémoire tampon de vertex avec l' \_ indicateur WRITEONLY D3DUSAGE, n’utilisez pas l' \_ indicateur de verrouillage ReadOnly D3DLOCK. Utilisez l' \_ indicateur D3DLOCK ReadOnly si votre application lit uniquement à partir de la mémoire tampon de vertex. L’inclusion de cet indicateur permet à Direct3D d’optimiser ses procédures internes pour améliorer l’efficacité, étant donné que l’accès à la mémoire est en lecture seule.

Pour [](performance-optimizations.md) plus d’informations sur l’utilisation de D3DLOCK \_ ignore ou D3DLOCK \_ NOOVERWRITE pour le paramètre flags de [**IDirect3DVertexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), consultez Utilisation de mémoires tampons de vertex et d’index dynamiques.

En C++, étant donné que vous accédez directement à la mémoire allouée pour la mémoire tampon de vertex, assurez-vous que votre application accède correctement à la mémoire allouée. Dans le cas contraire, vous risquez de rendre cette mémoire non valide. Utilisez la Stride du format de vertex que votre application utilise pour passer d’un vertex dans la mémoire tampon allouée à une autre. La mémoire tampon de vertex est un tableau simple de vertex spécifié dans le groupe de prix final. Utilisez le Stride de la structure de format de vertex que vous définissez. Vous pouvez calculer le Stride de chaque vertex au moment de l’exécution en examinant le [D3DFVF](d3dfvf.md) contenu dans la description de la mémoire tampon du vertex. Le tableau suivant indique la taille de chaque composant de vertex.



| Indicateur de format de vertex | Taille              |
|--------------------|-------------------|
| \_Diffusion D3DFVF    | sizeof (DWORD)     |
| D3DFVF \_ normal     | sizeof (float) x 3 |
| D3DFVF \_ spéculaire   | sizeof (DWORD)     |
| D3DFVF \_ TEXn       | sizeof (float) x n |
| D3DFVF \_ xyz        | sizeof (float) x 3 |
| D3DFVF \_ XYZRHW     | sizeof (float) x 4 |



 

Le nombre de coordonnées de texture présentes dans le format vertex est décrit par les \_ indicateurs D3DFVF Tex n (où n est une valeur comprise entre 0 et 8). Multipliez le nombre de jeux de coordonnées de texture par la taille d’un jeu de coordonnées de texture, qui peut être comprise entre un et quatre virgules flottantes, pour calculer la mémoire requise pour ce nombre de coordonnées de texture.

Utilisez le Stride de vertex total pour incrémenter et décrémenter le pointeur de mémoire si nécessaire pour accéder à des vertex particuliers.

## <a name="retrieving-vertex-buffer-descriptions"></a>Récupération des descriptions des mémoires tampons de vertex

Vous pouvez récupérer des informations sur une mémoire tampon de vertex en appelant la méthode [**IDirect3DVertexBuffer9 :: GetDesc**](/windows/desktop/api) . Cette méthode remplit les membres de la structure [**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md) avec des informations sur la mémoire tampon de vertex.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> </dl>

 

 
