---
description: Chaque développeur qui crée des applications en temps réel qui utilisent des graphiques 3D est préoccupé par l’optimisation des performances. Cette section fournit des instructions pour obtenir les meilleures performances de votre code.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Optimisations des performances (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d42be994522f0d83e36387b1a5866b3eee10df3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480689"
---
# <a name="performance-optimizations-direct3d-9"></a>Optimisations des performances (Direct3D 9)

Chaque développeur qui crée des applications en temps réel qui utilisent des graphiques 3D est préoccupé par l’optimisation des performances. Cette section fournit des instructions pour obtenir les meilleures performances de votre code.

-   [Conseils généraux sur les performances](#general-performance-tips)
-   [Bases de données et élimination](#databases-and-culling)
-   [Primitives de traitement par lot](#batching-primitives)
-   [Conseils d’éclairage](#lighting-tips)
-   [Taille de la texture](#texture-size)
-   [Transformations de matrice](#matrix-transforms)
-   [Utilisation de textures dynamiques](#using-dynamic-textures)
-   [Utilisation de mémoires tampons de vertex et d’index dynamiques](#using-dynamic-vertex-and-index-buffers)
-   [Utilisation de maillages](#using-meshes)
-   [Performances de la mémoire tampon Z](#z-buffer-performance)

## <a name="general-performance-tips"></a>Conseils généraux sur les performances

-   Désactivez uniquement lorsque vous devez.
-   Réduisez les modifications d’État et regroupez les modifications d’État restantes.
-   Utilisez des textures plus petites si vous le pouvez.
-   Dessinez des objets dans votre scène de l’avant vers l’arrière.
-   Utilisez des bandes triangulaires à la place des listes et des ventilateurs. Pour optimiser les performances du cache des vertex, réorganisez les bandes pour réutiliser les sommets de triangle plus tôt et plus tard.
-   Dégradez correctement les effets spéciaux qui nécessitent un partage disproportionné des ressources système.
-   Testez en permanence les performances de votre application.
-   Réduire les commutateurs de mémoire tampon de vertex.
-   Utilisez des mémoires tampons de vertex statiques dans la mesure du possible.
-   Utilisez un grand tampon de vertex statique par Commission pour les objets statiques, plutôt qu’un par objet.
-   Si votre application a besoin d’un accès aléatoire à la mémoire tampon de vertex dans la mémoire AGP, choisissez une taille de format de vertex qui est un multiple de 32 octets. Dans le cas contraire, sélectionnez le plus petit format approprié.
-   Dessinez à l’aide de primitives indexées. Cela peut permettre une mise en cache des vertex plus efficace au sein du matériel.
-   Si le format de mémoire tampon de profondeur contient un canal de stencil, effacez toujours les canaux de profondeur et de stencil en même temps.
-   Combinez l’instruction du nuanceur et la sortie des données dans la mesure du possible. Par exemple :
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Bases de données et élimination

La création d’une base de données fiable des objets dans votre monde est essentielle pour obtenir d’excellentes performances dans Direct3D. Il est plus important que les améliorations apportées à la pixellisation ou au matériel.

Vous devez conserver le nombre de polygones le plus bas que vous pouvez éventuellement gérer. Créez un nombre faible de polygones en générant des modèles à faible polygones à partir du début. Ajoutez des polygones si vous pouvez le faire sans sacrifier les performances plus tard dans le processus de développement. N’oubliez pas que les polygones les plus rapides sont ceux que vous ne dessinez pas.

## <a name="batching-primitives"></a>Primitives de traitement par lot

Pour obtenir les meilleures performances de rendu lors de l’exécution, essayez d’utiliser des primitives dans des lots et gardez le nombre de modifications d’état de rendu aussi faible que possible. Par exemple, si vous avez un objet avec deux textures, regroupez les triangles qui utilisent la première texture et suivez l’état de rendu nécessaire pour modifier la texture. Regroupez ensuite tous les triangles qui utilisent la deuxième texture. La prise en charge matérielle la plus simple pour Direct3D est appelée avec des lots d’États de rendu et des lots de primitives via la couche d’abstraction matérielle (HAL). Plus les instructions sont traitées par lot, moins le nombre d’appels de la couche HAL est élevé pendant l’exécution.

## <a name="lighting-tips"></a>Conseils d’éclairage

Étant donné que les lumières ajoutent un coût par vertex à chaque image rendue, vous pouvez améliorer considérablement les performances en veillant à la façon dont vous les utilisez dans votre application. La plupart des conseils suivants dérivent du maximiser, « le code le plus rapide est le code qui n’est jamais appelé ».

-   Utilisez le moins de sources de lumière possible. Pour augmenter le niveau d’éclairage global, par exemple, utilisez la lumière ambiante au lieu d’ajouter une nouvelle source de lumière.
-   Les lumières directionnelles sont plus efficaces que les lumières de point ou les actualités. Pour les lumières directionnelles, le sens de la lumière est fixe et n’a pas besoin d’être calculé sur la base de chaque vertex.
-   Les lumières peuvent être plus efficaces que les lumières de point, car la zone en dehors du cône est calculée rapidement. Le fait que les lumières soient plus efficaces ou non dépend de la proportion de votre scène qui est éclairée par la lumière.
-   Utilisez le paramètre Range pour limiter vos lumières aux seules parties de la scène que vous devez éclairer. Tous les types de lumière se ferment assez tôt lorsqu’ils sont hors limites.
-   La surbrillance spéculaire revient presque à doubler le coût d’une lumière. Utilisez-les uniquement lorsque vous devez le faire. Définissez l' \_ État de rendu D3DRS SpecularEnable sur 0, la valeur par défaut, dans la mesure du possible. Lors de la définition de matériaux, vous devez définir la valeur de puissance spéculaire sur zéro pour désactiver les surbrillances spéculaires de ce matériel. le fait de définir simplement la couleur spéculaire sur 0, 0, n’est pas suffisant.

## <a name="texture-size"></a>Taille de la texture

Les performances de mappage de texture dépendent fortement de la vitesse de la mémoire. Il existe plusieurs façons d’optimiser les performances du cache des textures de votre application.

-   Conservez les textures de petite taille. Plus les textures sont petites, plus il est probable qu’elles soient gérées dans le cache secondaire de l’UC principale.
-   Ne modifiez pas les textures en fonction de la primitive. Essayez de faire en sorte que les polygones soient regroupés dans l’ordre des textures qu’ils utilisent.
-   Utilisez des textures carrées chaque fois que possible. Les textures dont les dimensions sont 256x256 sont les plus rapides. Si votre application utilise quatre textures 128 x 128, par exemple, essayez de vous assurer qu’elles utilisent la même palette et placez-les toutes dans une texture 256x256. Cette technique réduit également la quantité de permutation de texture. Bien entendu, vous ne devez pas utiliser les textures 256x256, à moins que votre application ne nécessite un grand nombre de textures car, comme mentionné, les textures doivent être conservées le plus petit possible.

## <a name="matrix-transforms"></a>Transformations de matrice

Direct3D utilise les matrices universelles et de vue que vous avez définies pour configurer plusieurs structures de données internes. Chaque fois que vous définissez une nouvelle matrice de monde ou d’affichage, le système recalcule les structures internes associées. La définition fréquente de ces matrices, par exemple, des milliers de fois par trame, prend beaucoup de temps. Vous pouvez réduire le nombre de calculs requis en concaténant votre monde et en vue des matrices dans une matrice de vue universelle que vous définissez comme matrice universelle, puis en définissant la matrice de vue sur l’identité. Conservez les copies mises en cache des matrices de monde et de vue individuelles afin de pouvoir modifier, concaténer et réinitialiser la matrice universelle en fonction des besoins. Par souci de clarté dans cette documentation, les exemples Direct3D utilisent rarement cette optimisation.

## <a name="using-dynamic-textures"></a>Utilisation de textures dynamiques

Pour savoir si le pilote prend en charge les textures dynamiques, consultez l' \_ indicateur D3DCAPS2 DYNAMICTEXTURES de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

Gardez à l’esprit les points suivants lorsque vous travaillez avec des textures dynamiques.

-   Ils ne peuvent pas être gérés. Par exemple, le pool ne peut pas être géré par D3DPOOL \_ .
-   Les textures dynamiques peuvent être verrouillées, même si elles sont créées dans D3DPOOL \_ par défaut.
-   D3DLOCK \_ ignore est un indicateur de verrou valide pour les textures dynamiques.

Il est judicieux de créer une seule texture dynamique par format et éventuellement par taille. Les des mipmaps, cubes et volumes dynamiques ne sont pas recommandés en raison de la surcharge supplémentaire dans le verrouillage de chaque niveau. Pour des mipmaps, D3DLOCK \_ ignore est autorisé uniquement au niveau supérieur. Tous les niveaux sont ignorés en verrouillant uniquement le niveau supérieur. Ce comportement est le même pour les volumes et les cubes. Pour les cubes, le niveau supérieur et le visage 0 sont verrouillés.

Le pseudo-code suivant montre un exemple d’utilisation d’une texture dynamique.


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a>Utilisation de mémoires tampons de vertex et d’index dynamiques

Le verrouillage d’une mémoire tampon de vertex statique pendant que le processeur graphique utilise la mémoire tampon peut avoir une incidence significative sur les performances. L’appel de verrou doit attendre que le processeur graphique ait fini de lire les données du vertex ou de l’index dans la mémoire tampon avant de pouvoir retourner à l’application appelante, ce qui représente un délai important. Le verrouillage, puis le rendu à partir d’une mémoire tampon statique plusieurs fois par trame, empêche également le processeur graphique de mettre en mémoire tampon les commandes de rendu, car il doit terminer les commandes avant de retourner le pointeur de verrou. Sans commandes mises en mémoire tampon, le processeur graphique reste inactif jusqu’à ce que l’application ait fini de remplir la mémoire tampon de vertex ou le tampon d’index et envoie une commande de rendu.

Dans l’idéal, les données de vertex ou d’index ne changeraient jamais, mais ce n’est pas toujours possible. Dans de nombreux cas, l’application doit modifier des données de vertex ou d’index à chaque trame, voire plusieurs fois par frame. Dans ce cas, la mémoire tampon de vertex ou d’index doit être créée avec D3DUSAGE \_ Dynamic. Cet indicateur d’utilisation entraîne l’optimisation de Direct3D pour les opérations de verrouillage fréquentes. D3DUSAGE \_ Dynamic est utile uniquement lorsque la mémoire tampon est verrouillée fréquemment ; les données qui restent constantes doivent être placées dans un sommet statique ou une mémoire tampon d’index.

Pour bénéficier d’une amélioration des performances lors de l’utilisation de mémoires tampons de vertex dynamiques, l’application doit appeler [**IDirect3DVertexBuffer9 :: Lock**](/windows/desktop/api) ou [**IDirect3DIndexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) avec les indicateurs appropriés. D3DLOCK \_ ignore indique que l’application n’a pas besoin de conserver les anciennes données de vertex ou d’index dans la mémoire tampon. Si le processeur graphique utilise toujours le tampon lorsque Lock est appelé avec D3DLOCK \_ Discard, un pointeur vers une nouvelle région de mémoire est retourné à la place des anciennes données de mémoire tampon. Cela permet au processeur graphique de continuer à utiliser les anciennes données pendant que l’application place les données dans la nouvelle mémoire tampon. Aucune gestion de mémoire supplémentaire n’est nécessaire dans l’application. l’ancienne mémoire tampon est réutilisée ou détruite automatiquement lorsque le processeur graphique en a terminé avec celle-ci. Notez que le verrouillage d’une mémoire tampon avec D3DLOCK \_ Discard ignore toujours l’intégralité de la mémoire tampon, la spécification d’un décalage différent de zéro ou d’un champ de taille limitée ne conserve pas les informations dans les zones déverrouillées de la mémoire tampon.

Dans certains cas, la quantité de données que l’application doit stocker par verrou est faible, par exemple l’ajout de quatre sommets pour le rendu d’un sprite. D3DLOCK \_ NOOVERWRITE indique que l’application ne remplacera pas les données déjà en cours d’utilisation dans la mémoire tampon dynamique. L’appel de verrou retourne un pointeur vers les anciennes données, ce qui permet à l’application d’ajouter de nouvelles données dans les régions inutilisées du vertex ou de la mémoire tampon d’index. L’application ne doit pas modifier les vertex ou les index utilisés dans une opération de dessin, car ils peuvent toujours être utilisés par le processeur graphique. L’application doit ensuite utiliser D3DLOCK \_ ignore une fois que la mémoire tampon dynamique est pleine pour recevoir une nouvelle région de mémoire, en ignorant les anciennes données de vertex ou d’index une fois le processeur graphique terminé.

Le mécanisme de requête asynchrone est utile pour déterminer si les vertex sont toujours utilisés par le processeur graphique. Émettez une requête de type \_ événement D3DQUERYTYPE après le dernier appel DrawPrimitive qui utilise les vertex. Les vertex ne sont plus utilisés quand [**IDirect3DQuery9 :: GetData**](/windows/desktop/api) retourne S \_ OK. Le verrouillage d’un tampon avec D3DLOCK \_ Discard ignore ou no Flags garantit toujours que les vertex sont correctement synchronisés avec le processeur graphique, mais l’utilisation de Lock sans Flags entraîne une pénalité de performance décrite plus haut. D’autres appels d’API tels que [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api), [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api)et [**IDirect3DDevice9 ::P renvoyés**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) ne garantissent pas que le processeur graphique est terminé à l’aide de vertex.

Vous trouverez ci-dessous les façons d’utiliser des mémoires tampons dynamiques et les indicateurs de verrou appropriés.


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a>Utilisation de maillages

Vous pouvez optimiser les maillages à l’aide des triangles indexés Direct3D plutôt que des bandes à facettes indexées. Le matériel découvre que 95% des triangles successifs forment en réalité des bandes et s’ajustent en conséquence. De nombreux pilotes le font également pour un matériel plus ancien.

Les objets de maillage D3DX peuvent avoir chaque triangle, ou face, avec une valeur DWORD, appelée l’attribut de cette face. La sémantique de la valeur DWORD est définie par l’utilisateur. Ils sont utilisés par D3DX pour classer le maillage en sous-ensembles. L’application définit des attributs par face à l’aide de l’appel de [**ID3DXMesh :: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) . La méthode [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) a une option permettant de regrouper les vertex et les visages de maillage sur les attributs à l’aide de l' \_ option D3DXMESHOPT ATTRSORT. Une fois cette opération effectuée, l’objet Mesh calcule une table d’attributs qui peut être obtenue par l’application en appelant [**ID3DXBaseMesh :: GetAttributeTable**](id3dxbasemesh--getattributetable.md). Cet appel retourne 0 si le maillage n’est pas trié par attributs. Il n’existe aucun moyen pour une application de définir une table d’attributs, car elle est générée par la méthode **ID3DXMesh :: Optimize** . Le tri d’attribut est sensible aux données. par conséquent, si l’application sait qu’une maille est triée par attribut, elle doit toujours appeler **ID3DXMesh :: Optimize** pour générer la table d’attributs.

Les rubriques suivantes décrivent les différents attributs d’une maille.

### <a name="attribute-id"></a>ID d’attribut

Un ID d’attribut est une valeur qui associe un groupe de faces à un groupe d’attributs. Cet ID décrit le sous-ensemble des visages [**ID3DXBaseMesh ::D rawsubset**](id3dxbasemesh--drawsubset.md) doit dessiner. Les ID d’attribut sont spécifiés pour les visages dans la mémoire tampon d’attribut. Les valeurs réelles des ID d’attribut peuvent correspondre à tout ce qui s’ajuste à 32 bits, mais il est courant d’utiliser 0 à n, où n est le nombre d’attributs.

### <a name="attribute-buffer"></a>Mémoire tampon d’attributs

La mémoire tampon d’attribut est un tableau de DWORDs (un par visage) qui spécifie le groupe d’attributs auquel chaque face appartient. Cette mémoire tampon est initialisée sur zéro à la création d’un maillage, mais est remplie par les routines de chargement ou doit être remplie par l’utilisateur si plusieurs attributs avec l’ID 0 sont souhaités. Cette mémoire tampon contient les informations utilisées pour trier le maillage en fonction des attributs de [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md). Si aucune table d’attributs n’est présente, [**ID3DXBaseMesh ::D rawsubset**](id3dxbasemesh--drawsubset.md) analyse cette mémoire tampon pour sélectionner les faces de l’attribut donné à dessiner.

### <a name="attribute-table"></a>Table d’attributs

La table d’attributs est une structure appartenant et gérée par la maille. La seule façon d’être générée est d’appeler [**ID3DXMesh :: Optimize**](id3dxmesh--optimize.md) avec le tri d’attribut ou une optimisation renforcée activée. La table d’attributs est utilisée pour initialiser rapidement un appel de la primitive de dessin unique à [**ID3DXBaseMesh ::D rawsubset**](id3dxbasemesh--drawsubset.md). La seule autre utilisation est que la progression des maillages conserve également cette structure. il est donc possible de voir quelles faces et quels vertex sont actifs au niveau de détail actuel.

## <a name="z-buffer-performance"></a>Performances de la mémoire tampon Z

Les applications peuvent améliorer les performances lors de l’utilisation de la mise en mémoire tampon z et de la texturation en veillant à ce que les scènes soient rendues de l’avant vers l’arrière. Les primitives de mise en mémoire tampon z texturées sont prétestées par rapport à la mémoire tampon z sur la base d’une ligne d’analyse. Si une ligne de numérisation est masquée par un polygone précédemment rendu, le système la rejette rapidement et efficacement. La mise en mémoire tampon Z peut améliorer les performances, mais la technique est particulièrement utile lorsqu’une scène dessine les mêmes pixels plusieurs fois. Cela est difficile à calculer exactement, mais vous pouvez souvent faire une approximation proche. Si les mêmes pixels sont dessinés en moins de deux fois, vous pouvez obtenir des performances optimales en désactivant la mise en mémoire tampon z et en rendant la scène de l’arrière vers l’avant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils de programmation](programming-tips.md)
</dt> </dl>

 

 
