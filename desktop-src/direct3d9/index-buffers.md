---
description: Les mémoires tampons d’index, représentées par l’interface IDirect3DIndexBuffer9, sont des mémoires tampons qui contiennent des données d’index.
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: Mémoires tampons d’index (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232692"
---
# <a name="index-buffers-direct3d-9"></a>Mémoires tampons d’index (Direct3D 9)

Les mémoires tampons d’index, représentées par l’interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , sont des mémoires tampons qui contiennent des données d’index. Les données d’index, ou indices, sont des décalages d’entiers dans les tampons de vertex et sont utilisés pour restituer des primitives à l’aide de la méthode [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

Une mémoire tampon de vertex contient des vertex ; par conséquent, vous pouvez dessiner une mémoire tampon de vertex avec ou sans primitives indexées. Toutefois, étant donné qu’un tampon d’index contient des indices, vous ne pouvez pas utiliser un tampon d’index sans une mémoire tampon de vertex correspondante. (À titre d’exemple, [**IDirect3DDevice9 ::D rawindexedprimitiveup**](/windows/desktop/api) et [**IDirect3DDevice9 ::D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) sont les seules méthodes de dessin qui dessinent sans index ou une mémoire tampon de vertex.)

## <a name="index-buffer-description"></a>Description de la mémoire tampon d’index

Une mémoire tampon d’index est décrite en termes de fonctionnalités, telles que son emplacement dans la mémoire, si elle prend en charge la lecture et l’écriture, et le type et le nombre d’index qu’elle peut contenir. Ces caractéristiques sont conservées dans une structure [**D3DINDEXBUFFER \_ desc**](d3dindexbuffer-desc.md) .

Les descriptions de la mémoire tampon d’index indiquent à votre application comment une mémoire tampon existante a été créée. Vous fournissez une structure de description vide pour que le système remplisse les fonctionnalités d’un tampon d’index créé précédemment.

-   Le membre de format décrit le format de surface des données de la mémoire tampon d’index.
-   Le type identifie le type de ressource de la mémoire tampon d’index.
-   Le membre de la structure d’utilisation contient des indicateurs de capacité généraux. L' \_ indicateur D3DUSAGE SOFTWAREPROCESSING indique que le tampon d’index doit être utilisé avec le traitement du vertex logiciel. La présence de l' \_ indicateur WRITEONLY D3DUSAGE dans usage indique que la mémoire tampon d’index est utilisée uniquement pour les opérations d’écriture. Cela libère le pilote pour placer les données d’index dans le meilleur emplacement de mémoire pour permettre un traitement et un rendu rapides. Si l' \_ indicateur WRITEONLY D3DUSAGE n’est pas utilisé, le pilote est moins susceptible de placer les données dans un emplacement qui est inefficace pour les opérations de lecture. Cela sacrifie la vitesse de traitement et de rendu. Si cet indicateur n’est pas spécifié, il est supposé que les applications effectuent des opérations de lecture et d’écriture sur les données de la mémoire tampon d’index.
-   Pool spécifie la classe de mémoire allouée pour le tampon d’index. L' \_ indicateur D3DPOOL SYSTEMMEM indique que le système a créé la mémoire tampon d’index dans la mémoire système.
-   Le membre de taille stocke la taille, en octets, des données de mémoire tampon de vertex.
-   Le dernier paramètre pSharedHandle n’est pas utilisé. Affectez-lui la valeur **null**.

## <a name="index-processing-requirements"></a>Exigences relatives au traitement des index

Les performances des opérations de traitement d’index dépendent en grande partie de l’emplacement de la mémoire tampon d’index dans la mémoire et du type de périphérique de rendu utilisé. Les applications contrôlent l’allocation de mémoire pour les mémoires tampons d’index lorsqu’elles sont créées. Lorsque l' \_ indicateur de mémoire D3DPOOL SYSTEMMEM est défini, la mémoire tampon d’index est créée dans la mémoire système. Lorsque l' \_ indicateur de mémoire par défaut D3DPOOL est utilisé, le pilote de périphérique détermine l’emplacement de la mémoire tampon d’index la plus appropriée, souvent appelée mémoire optimale pour le pilote. La mémoire optimale pour le pilote peut être une mémoire vidéo locale, une mémoire vidéo non locale ou une mémoire système.

La définition de l' \_ indicateur de comportement D3DUSAGE SOFTWAREPROCESSING lors de l’appel de la méthode [**IDirect3DDevice9 :: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) spécifie que la mémoire tampon d’index doit être utilisée avec le traitement du vertex logiciel. Cet indicateur est requis dans le traitement des vertex en mode mixte (D3DCREATE \_ Mixed \_ VERTEXPROCESSING) lorsque le traitement du vertex logiciel est utilisé.

L’application peut écrire directement des index dans un tampon d’index alloué dans la mémoire optimale du pilote. Cette technique empêche ultérieurement une opération de copie redondante. Cette technique ne fonctionne pas correctement si votre application lit les données à partir d’un tampon d’index, car les opérations de lecture effectuées par l’hôte à partir de la mémoire optimale du pilote peuvent être très lentes. Par conséquent, si votre application doit lire au cours du traitement ou écrire des données dans la mémoire tampon de façon erratique, il est préférable de choisir un tampon d’index de mémoire système.

> [!Note]  
> Utilisez toujours la \_ valeur par défaut D3DPOOL, sauf si vous ne souhaitez pas utiliser de mémoire vidéo ou utiliser de grandes quantités de RAM verrouillée en page lorsque le pilote met des tampons de vertex ou d’index dans la mémoire AGP.

 

## <a name="create-an-index-buffer"></a>Créer un tampon d’index

Créez un objet de mémoire tampon d’index en appelant la méthode [**IDirect3DDevice9 :: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) , qui accepte six paramètres.

-   Le premier paramètre spécifie la longueur de la mémoire tampon d’index, en octets.
-   Le deuxième paramètre est un ensemble de contrôles d’utilisation. Entre autres choses, sa valeur détermine si les vertex référencés par les index peuvent contenir des informations de découpage. Pour améliorer les performances, spécifiez D3DUSAGE \_ DONOTCLIP lorsque le découpage n’est pas nécessaire.

    L' \_ indicateur D3DUSAGE SOFTWAREPROCESSING peut être défini lorsque le traitement en mode mixte ou le traitement du vertex logiciel (D3DCREATE \_ Mixed \_ VERTEXPROCESSING/D3DCREATE \_ Software \_ VERTEXPROCESSING) est activé pour cet appareil. D3DUSAGE \_ SOFTWAREPROCESSING doit être défini pour les mémoires tampons à utiliser avec le traitement du vertex logiciel en mode mixte, mais il ne doit pas être défini pour obtenir les meilleures performances possibles lors de l’utilisation du traitement de l’index matériel en mode mixte (D3DCREATE \_ matériel \_ VERTEXPROCESSING). Toutefois, la définition de D3DUSAGE \_ SOFTWAREPROCESSING est la seule option lorsqu’une seule mémoire tampon est utilisée avec le traitement du vertex matériel et logiciel. D3DUSAGE \_ SOFTWAREPROCESSING est autorisé pour les périphériques mixtes et logiciels.

    Il est possible de forcer des tampons de vertex et d’index dans la mémoire système en spécifiant D3DPOOL \_ SYSTEMMEM, même lorsque le traitement de l’index est effectué dans le matériel. Il s’agit d’un moyen d’éviter une trop grande quantité de mémoire verrouillée en mode page lorsqu’un pilote met ces mémoires tampon dans la mémoire AGP.

-   Le troisième paramètre est le membre D3DFMT \_ INDEX16 ou D3DFMT \_ INDEX32 du type énuméré [D3DFORMAT](d3dformat.md) qui spécifie la taille de chaque index.

-   Le quatrième paramètre est un membre du type énuméré [**D3DPOOL**](./d3dpool.md) qui indique au système où placer en mémoire le nouveau tampon d’index.

-   Le dernier paramètre que [**IDirect3DDevice9 :: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) accepte est l’adresse d’une variable qui est remplie avec un pointeur vers la nouvelle interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) de l’objet de mémoire tampon de vertex, si l’appel a échoué.

L’exemple de code C++ suivant montre à quoi peut ressembler la création d’un tampon d’index dans le code.


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a>Accéder à un tampon d’index

Les objets de mémoire tampon d’index permettent aux applications d’accéder directement à la mémoire allouée aux données d’index. Vous pouvez récupérer un pointeur vers la mémoire tampon d’index en appelant la méthode [**IDirect3DIndexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) , puis en accédant à la mémoire si nécessaire pour remplir la mémoire tampon avec les nouvelles données d’index ou pour lire les données qu’elle contient. La méthode Lock accepte quatre paramètres. Le premier, *OffsetToLock*, est le décalage dans les données d’index. Le deuxième paramètre est la taille, exprimée en octets, des données de l’index. Le troisième paramètre accepté par la méthode **IDirect3DIndexBuffer9 :: Lock** , *ppbData*, est l’adresse d’un pointeur d’octet rempli d’un pointeur vers les données d’index, si l’appel est effectué.

Le dernier paramètre, *Flags*, indique au système la manière dont la mémoire doit être verrouillée. Vous pouvez l’utiliser pour indiquer comment l’application accède aux données dans la mémoire tampon. Spécifiez les constantes pour le paramètre *Flags* en fonction de la façon dont votre application accède aux données d’index. Cela permet au pilote de verrouiller la mémoire et de fournir des performances optimales en fonction du type d’accès demandé. Utilisez \_ l’indicateur D3DLOCK ReadOnly si votre application est en lecture seule à partir de la mémoire tampon d’index. L’inclusion de cet indicateur permet à Direct3D d’optimiser ses procédures internes pour améliorer l’efficacité, étant donné que l’accès à la mémoire est en lecture seule.

Après avoir rempli ou lu les données de l’index, appelez la méthode [**IDirect3DIndexBuffer9 :: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) , comme indiqué dans l’exemple de code suivant.


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> Si vous créez un tampon d’index avec l' \_ indicateur WRITEONLY D3DUSAGE, n’utilisez pas l' \_ indicateur de verrouillage ReadOnly D3DLOCK. Utilisez l' \_ indicateur D3DLOCK ReadOnly si votre application lit uniquement à partir de la mémoire tampon d’index. L’inclusion de cet indicateur permet à Direct3D d’optimiser ses procédures internes pour améliorer l’efficacité, étant donné que l’accès à la mémoire est en lecture seule.
>
> Pour plus d’informations sur l’utilisation \_ de D3DLOCK ignore ou D3DLOCK \_ NOOVERWRITE pour le paramètre *Flags* de la méthode [**IDirect3DIndexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) , consultez [optimisation des performances (Direct3D 9)](performance-optimizations.md).

 

En C++, étant donné que vous accédez directement à la mémoire allouée pour le tampon d’index, assurez-vous que votre application accède correctement à la mémoire allouée. Dans le cas contraire, vous risquez de rendre cette mémoire non valide. Utilisez la valeur Stride du format d’index utilisé par votre application pour passer d’un index dans la mémoire tampon allouée à une autre.

Récupérez les informations relatives à une mémoire tampon d’index en appelant la méthode [**IDirect3DIndexBuffer9 :: GetDesc**](/windows/desktop/api) . Cette méthode remplit les membres de la structure [**D3DINDEXBUFFER \_ desc**](d3dindexbuffer-desc.md) avec les informations relatives à la mémoire tampon d’index.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> <dt>

[Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Mémoires tampons de vertex (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
